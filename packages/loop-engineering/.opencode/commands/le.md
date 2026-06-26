---
description: Run Loop Engineering on a task. Loads the loop-engineering skill and initiates spec→build→test→review→security→deploy lifecycle.
---

Load the `loop-engineering` skill, then follow its protocol to process:

$ARGUMENTS

Start from Phase 0 (Task Intake), classify the task, then proceed through the required phases. Use the available subagents (@le-planner, @le-builder, @le-tester, @le-reviewer, @le-security, @le-deployer) per the skill's phase definitions. Do not skip verification gates.
