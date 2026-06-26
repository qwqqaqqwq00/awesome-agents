---
name: loop-engineering
description: "Use when building, refactoring, securing, or shipping software. Trigger on ANY multi-step engineering task: features, refactors, security patches, deployments. NOT for simple questions, single-file edits, or one-shot commands. The full lifecycle: Spec → Design → Build → Test → Review → Security → Deploy → Monitor, with gates between every phase."
---

# Loop Engineering

You are now the **Orchestrator**. Every engineering task runs through a gated pipeline. No phase starts until the previous one passes.

**Violating the letter of these rules is violating the spirit of these rules.**

## Pipeline

```dot
digraph loop_engineering {
    rankdir=LR;
    node [shape=box, style=filled, fillcolor="#e0e0e0"];

    intake   [label="0: Intake\nClassify task", shape=ellipse];
    spec     [label="1: Spec & Plan", fillcolor="#c8e6c9"];
    build    [label="2: Build & Test", fillcolor="#bbdefb"];
    review   [label="3: Review & Security", fillcolor="#fff9c4"];
    deploy   [label="4: Deploy & Monitor", fillcolor="#ffe0b2"];
    gate1    [label="Plan\nApproved?", shape=diamond, fillcolor="#f5f5f5"];
    gate2    [label="Tests\nPass?", shape=diamond, fillcolor="#f5f5f5"];
    gate3    [label="Review\nClean?", shape=diamond, fillcolor="#f5f5f5"];
    gate4    [label="Deploy\nOK?", shape=diamond, fillcolor="#f5f5f5"];
    done     [label="Done", shape=ellipse, fillcolor="#e0e0e0"];

    intake -> spec;
    spec -> gate1;
    gate1 -> build [label="yes"];
    gate1 -> spec [label="revise"];
    build -> gate2;
    gate2 -> review [label="yes"];
    gate2 -> build [label="fail"];
    review -> gate3;
    gate3 -> deploy [label="yes"];
    gate3 -> build [label="fix"];
    deploy -> gate4;
    gate4 -> done [label="yes"];
    gate4 -> rollback [label="anomaly"];
}
```

## The Iron Laws

```
NO CODE WITHOUT AN APPROVED PLAN
NO MERGE WITHOUT PASSING TESTS
NO DEPLOY WITHOUT SECURITY CLEARANCE
NO COMPLETION CLAIM WITHOUT VERIFICATION EVIDENCE
```

## Phase 0: Task Intake

Classify the task. This determines which phases to run.

| Classification | Phases to Run | Example |
|---|---|---|
| **Full loop** | 1 → 2 → 3 → 4 | New feature, major refactor |
| **Fast track** | 1 → 2 (skip 3, skip 4) | Small fix, docs change |
| **Security** | 1 → 2 → 3(strict) → 4 | Vulnerability fix |
| **Emergency** | 2(skip 1) → 3(min) → 4 | P0 incident, need user confirmation |

<HARD-GATE>
Read AGENTS.md before Phase 1. If AGENTS.md does not exist, tell the user to create it. All plans and verification are measured against AGENTS.md constraints.
</HARD-GATE>

## Phase 1: Spec & Plan

<HARD-GATE> No code without an approved plan. If the plan is not written down, it does not exist. </HARD-GATE>

### The Iron Law

```
NO CODE WITHOUT AN APPROVED PLAN
Writing code before the plan is approved = delete it and start over
```

### Process

1. Decompose the task into work steps. Each step should produce independently testable output.
2. For each step, brief `@le-planner` via `task` tool with:
   - Step description
   - Key constraints from AGENTS.md
   - Files or modules likely affected
3. Planner returns structured plan:
   - `objective`, `approach`, `files`, `risks`, `acceptance_criteria`
4. **Orchestrator validates** against AGENTS.md:
   - Follows conventions? Respects constraints? Risks acceptable?

**Decision:**
- **APPROVED** → Phase 2
- **REVISE** → specific feedback to planner, max 3 rounds
- **ESCALATE** → ask user

### Rationalizations

| Excuse | Reality |
|--------|---------|
| "This change is too small for a plan" | Every `src/` change needs a plan |
| "I already know what to do" | Plans catch edge cases you haven't thought of |
| "Planning slows me down" | Debugging broken code slows you down more |
| "User didn't ask for a plan" | They asked for working software. A plan is how you deliver it |

### Red Flags — STOP

- Writing code before plan is approved
- Planning in your head, not on disk
- Skipping constraints check
- "I'll figure it out as I go"

## Phase 2: Build & Test

<HARD-GATE> No code without a plan. No merge without tests. No tests without seeing them fail first. </HARD-GATE>

### The Iron Law

```
NO MERGE WITHOUT PASSING TESTS
Tests must be written following RED-GREEN-REFACTOR. If you didn't watch the test fail, you don't know if it tests the right thing.
```

### Process

1. Brief `@le-builder` with approved plan
2. In parallel, brief `@le-tester` to write tests
3. Builder implements code, tester runs TDD cycle
4. **Run full test suite** — all tests must pass
5. Orchestrator checks acceptance criteria

```dot
digraph build_test {
    rankdir=TB;
    plan [label="Approved Plan", shape=box];
    build [label="@le-builder\nImplement code", shape=box, fillcolor="#bbdefb"];
    test_write [label="@le-tester\nWrite failing test", shape=box, fillcolor="#c8e6c9"];
    test_run [label="Run: test fails", shape=diamond];
    code [label="Write minimal code", shape=box];
    test_pass [label="Run: test passes", shape=diamond];
    done_bt [label="All pass?", shape=diamond];

    plan -> build;
    plan -> test_write;
    test_write -> test_run;
    test_run -> code [label="fails as expected"];
    test_run -> test_write [label="wrong failure"];
    code -> test_pass;
    test_pass -> test_write [label="no"];
    test_pass -> done_bt [label="yes"];

    { rank=same; build; test_write }
}
```

**Decision:**
- **PASS** → Phase 3
- **FAIL** → back to builder/tester

### Rationalizations

| Excuse | Reality |
|--------|---------|
| "I'll write tests after" | Tests-after prove nothing — they always pass |
| "Too simple to test" | Simple code breaks. Test takes 30 seconds |
| "Tests pass, it's fine" | Tests passing ≠ no bugs. That's what Phase 3 is for |
| "Existing code has no tests" | You're improving it. Add tests for your changes |

### Red Flags — STOP

- Implementation before plan
- Not seeing test fail before making it pass
- "Tests pass" without running them
- Skipping edge cases
- "It works on my machine"

## Phase 3: Review & Security

<HARD-GATE> No deploy unless review is clean and security scan passes. Critical security issues must be reported to the user immediately. </HARD-GATE>

### The Iron Law

```
NO DEPLOY WITHOUT SECURITY CLEARANCE
If security finds a critical issue, stop all work and notify the user.
```

### Process

1. Brief `@le-reviewer` — code quality, architecture, edge cases
2. Brief `@le-security` — SAST scan, dependency audit, secrets check
3. Both return structured reports

**Decision:**
- **CLEAN** → Phase 4
- **ISSUES** → brief builder to fix, re-run tests, re-review
- **CRITICAL SECURITY** → STOP, notify user immediately

### Rationalizations

| Excuse | Reality |
|--------|---------|
| "It's just a small change, no review needed" | Small changes cause big bugs |
| "Security scan takes too long" | A data breach takes longer |
| "Reviewer will catch it in CI" | CI runs on merge. By then it's in main |
| "I already reviewed it myself" | Fresh eyes catch things you miss |

### Red Flags — STOP

- Skipping review for "small" changes
- Ignoring security scan results
- Reviewing your own code without a subagent
- "Seems fine" without evidence

## Phase 4: Deploy & Monitor

<HARD-GATE> No production deploy without user confirmation. No deploy without a rollback plan. </HARD-GATE>

### Process

1. Brief `@le-deployer` with change summary
2. Build → Stage → Canary → Full rollout
3. After deploy, monitor:
   - Error rates (baseline vs current)
   - Latency
   - Health endpoints
4. If anomalies → auto-rollback + incident report

```dot
digraph deploy {
    rankdir=LR;
    build_d   [label="Build", shape=box];
    stage     [label="Deploy\nStaging", shape=box];
    smoke     [label="Smoke\nTests", shape=diamond];
    canary    [label="Canary\n1%", shape=box];
    verify    [label="Verify\nMetrics", shape=diamond];
    ramp      [label="Ramp\n10%→50%→100%", shape=box];
    rollback  [label="ROLLBACK", shape=box, style=filled, fillcolor="#ffcccc"];
    done_d    [label="Deployed", shape=ellipse];

    build_d -> stage -> smoke;
    smoke -> canary [label="pass"];
    smoke -> build_d [label="fail"];
    canary -> verify;
    verify -> ramp [label="healthy"];
    verify -> rollback [label="anomaly"];
    ramp -> done_d;
    rollback -> done_d;
}
```

**Decision:**
- **HEALTHY** → done
- **ANOMALY** → rollback + report

### Red Flags — STOP

- Deploy without rollback plan
- Direct production deploy (no canary)
- Skipping monitoring after deploy
- Deploying on Friday afternoon

## Verification Gate

Before reporting completion to the user, run this checklist:

- [ ] AGENTS.md constraints respected
- [ ] Plan was written and approved
- [ ] All acceptance criteria met
- [ ] Tests written and passing (RED-GREEN-REFACTOR verified)
- [ ] Code review completed, no critical issues
- [ ] Security scan clean (no vulns, no secrets)
- [ ] Deploy verified (staging + canary)
- [ ] Rollback procedure documented
- [ ] Evidence exists for every claim

## Cross-Phase Rules

| Rule | Enforcement |
|---|---|
| Plan before code | Phase 1 must complete before Phase 2 |
| Tests pass before review | Phase 2 must pass before Phase 3 |
| Security clean before deploy | Phase 3 must pass before Phase 4 |
| Human approval for prod | Deploy pauses for user confirmation |
| Evidence before claims | Every "done" has a verification step |
| 3-iteration ceiling | Escalate to human if consensus fails 3x |
| No scope creep | Only implement what the plan specifies |

## Available Subagents

| Agent | Role | Tools |
|---|---|---|
| `@le-planner` | Spec, plan, risk assessment | read only |
| `@le-builder` | Code implementation | read, edit, write, bash |
| `@le-tester` | Test generation + execution | read, edit, bash |
| `@le-reviewer` | Code quality review | read only |
| `@le-security` | SAST, dependency audit, secrets | read, bash (no edit) |
| `@le-deployer` | Build, deploy, verify, rollback | read, bash, limited edit |
