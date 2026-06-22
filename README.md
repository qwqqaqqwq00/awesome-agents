# Awesome Agents

A curated list of innovative **Agent Skills**, **MCP servers**, and **Agent tooling** for AI coding agents.

## MCP Servers

### Official Servers

- [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) — ⭐ 87k+ Canonical reference servers from Anthropic: Filesystem, GitHub, Slack, PostgreSQL, Playwright, Puppeteer, Memory, Brave Search, Google Drive, and more.
- [github/github-mcp-server](https://github.com/github/github-mcp-server) — ⭐ 31k Official GitHub MCP server by GitHub (Go). Repos, issues, PRs, search, merges.
- [microsoft/playwright-mcp](https://github.com/microsoft/playwright-mcp) — ⭐ 37k Browser automation MCP by Microsoft. Web scraping, interaction, screenshots via Playwright.
- [cloudflare/mcp-server-cloudflare](https://github.com/cloudflare/mcp-server-cloudflare) — Official Cloudflare MCP. Workers, KV, R2, D1, Durable Objects management.
- [stripe/mcp-server-stripe](https://github.com/stripe/mcp-server-stripe) — Official Stripe integration for AI agents. Payments, customers, subscriptions.
- [figma/mcp-server-figma](https://github.com/figma/mcp-server-figma) — Official Figma MCP. Read Figma files, frames, components from AI agents.

### Community Standouts

- [PrefectHQ/fastmcp](https://github.com/PrefectHQ/fastmcp) — ⭐ 26k Pythonic framework to build MCP servers fast. Type-safe, with async support and built-in validation.
- [ChromeDevTools/chrome-devtools-mcp](https://github.com/ChromeDevTools/chrome-devtools-mcp) — ⭐ 44k Chrome DevTools integration. Debug, inspect, profile from your agent.
- [firecrawl/firecrawl-mcp-server](https://github.com/firecrawl/firecrawl-mcp-server) — ⭐ 7k Web scraping & search optimized for AI agents. JS rendering, anti-bot bypass.
- [DeusData/codebase-memory-mcp](https://github.com/DeusData/codebase-memory-mcp) — ⭐ 10k Ultra-fast code intelligence with knowledge graph. Cross-session codebase memory for agents.
- [lastmile-ai/mcp-agent](https://github.com/lastmile-ai/mcp-agent) — ⭐ 8k Build agents using MCP with workflow patterns (read-ask-analyze, loop, sequential).
- [CoplayDev/unity-mcp](https://github.com/CoplayDev/unity-mcp) — ⭐ 11k AI ↔ Unity Editor bridge. Create, modify GameObjects, run play mode from agent.
- [mcp-use/mcp-use](https://github.com/mcp-use/mcp-use) — ⭐ 10k Fullstack framework for building MCP apps and servers. Streaming, SSE, transport-agnostic.
- [grab/cursor-talk-to-figma-mcp](https://github.com/grab/cursor-talk-to-figma-mcp) — ⭐ 7k Talk to Figma from AI agents. Read layers, export SVGs, inspect designs.

### Category Picks

| Category | Project | Description |
|---|---|---|
| Database | **neondatabase/mcp-server-neon** | Serverless Postgres — create branches, run queries from agent |
| Search | **Brave Search** (in official servers) | Privacy-first web search via Brave API |
| Memory | **Memory** (in official servers) | Knowledge graph for cross-session persistent memory |
| Sandbox | **E2B** (in official servers) | Cloud sandbox for secure code execution |
| Analytics | **DuckDB** (in official servers) | OLAP-style in-process analytics queries |
| Infra | **vercel/mcp-server** | Vercel deployments, projects, environment management |

## Agent Skills

### Skill Collections

- [anthropics/skills](https://github.com/anthropics/skills) — ⭐ 153k Official Anthropic agent skills repo. The canonical Agent Skills standard. Skills for document editing, creative, development, enterprise. Install via `plugin marketplace add anthropics/skills`.
- [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) — ⭐ 65k Production-grade engineering skills. 24 skills across Define → Plan → Build → Verify → Review → Ship lifecycle. 8 slash commands, 4 specialist personas, 5 reference checklists. Works with Claude Code, Cursor, OpenCode, Windsurf, Gemini CLI, Copilot.
- [nexu-io/open-design](https://github.com/nexu-io/open-design) — ⭐ 69k 259+ design skills, 142+ design systems. Figma/CSS/UI patterns for AI agents.
- [CherryHQ/cherry-studio](https://github.com/CherryHQ/cherry-studio) — ⭐ 48k Desktop AI studio with 300+ built-in assistant skills and multi-provider support.
- [DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail) — ⭐ 45k "Laziest senior dev" skill. Enforces YAGNI — reduces code generation by 40-60% by aggressively pruning unnecessary code.
- [wshobson/agents](https://github.com/wshobson/agents) — ⭐ 37k Multi-harness agentic plugin marketplace. Skills that work across Claude Code, Cursor, Windsurf, and Gemini CLI.

### Agent Loop & Orchestration

- [Upsonic/upsonic](https://github.com/Upsonic/Upsonic) — ⭐ 8k Autonomous AI agents framework with multi-agent collaboration, MCP integration, and reliability layers.
- [Pythagora-io/gpt-pilot](https://github.com/Pythagora-io/gpt-pilot) — ⭐ 32k AI developer companion that plans, codes, debugs, and tests — a complete agent loop for software projects.
- [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) — ⭐ 27k Lightweight agent loop with tool calling, handoffs, guardrails, and tracing.

### Specialized Skills

- **restriction-ensure** — Consensus agent loop (Orchestrator ↔ Designer ↔ Executor) with constraint-based verification. See [qwqqaqqwq00/RestrictionEnsure](https://github.com/qwqqaqqwq00/RestrictionEnsure).
- **code-reviewer** (from addyosmani/agent-skills) — Automated PR review with security, performance, and style checks.
- **webperf-auditor** (from addyosmani/agent-skills) — Lighthouse-based web performance auditing skill.
- **test-engineer** (from addyosmani/agent-skills) — Automated test generation with coverage analysis.

## Awesome Lists

- [appcypher/awesome-mcp-servers](https://github.com/appcypher/awesome-mcp-servers) — ⭐ 6k Comprehensive categorized MCP server directory.
- [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) — ⭐ 65k Curated Claude skills, hooks, MCPs, and resources.
- [hesreallyhim/awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) — ⭐ 47k Skills, hooks, slash-commands, workflows for Claude Code.
- [sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) — ⭐ 41k 1,600+ agentic skills for Claude Code, Cursor, Windsurf, Gemini CLI.
- [VoltAgent/awesome-openclaw-skills](https://github.com/VoltAgent/awesome-openclaw-skills) — ⭐ 51k Filtered registry of 5,400+ OpenClaw skills.
- [e2b-dev/awesome-ai-agents](https://github.com/e2b-dev/awesome-ai-agents) — ⭐ 5k+ AI agent frameworks, tools, and platforms.

## MCP Registries

- [Smithery](https://smithery.ai) — Largest MCP registry (11k+ servers). Handles auth, OAuth, credential management.
- [Glama](https://glama.ai/mcp) — MCP server directory with compatibility testing.
- [MCPHub](https://mcp-hub.com) — Curated MCP server directory.

## Agent Frameworks with Skill/Tool Systems

| Framework | Stars | Language | Skill System |
|---|---|---|---|
| [Claude Code](https://github.com/anthropics/claude-code) | — | TypeScript | Native `.claude/skills/`, plugins, MCP |
| [OpenCode](https://github.com/anomalyco/opencode) | 160k | TypeScript | `.opencode/skills/`, subagents, plugins, MCP |
| [LangChain](https://github.com/langchain-ai/langchain) | 100k+ | Python | Tools, toolkits, custom functions |
| [smolagents](https://github.com/huggingface/smolagents) | 28k | Python | Code Agent (Python-as-action), Hub-integrated tools |
| [CrewAI](https://github.com/crewAIInc/crewAI) | 54k | Python | Role-based tools, crew-specific tool sets |
| [AutoGen](https://github.com/microsoft/autogen) | 38k+ | Python | Tool registration, multi-agent function tools |
| [Semantic Kernel](https://github.com/microsoft/semantic-kernel) | 28k | C#/Python | Plugins, functions, connectors, MCP/A2A |
| [Mastra](https://github.com/mastra-ai/mastra) | 25k | TypeScript | Graph workflows + agents, MCP authoring |
| [Vercel AI SDK](https://github.com/vercel/ai) | 25k | TypeScript | Tool calling, generative UI, streaming |
| [Dify](https://github.com/langgenius/dify) | 60k+ | Python/TS | Visual agent builder, tool plugins, marketplace |

## Game Development

MCP servers and skills for working with game engines, 3D modeling, pixel art, and audio.

### Game Engines

#### Unity

- [CoplayDev/unity-mcp](https://github.com/CoplayDev/unity-mcp) — ⭐ 11k Bridge between AI assistants and Unity Editor. Manage assets, control scenes, edit scripts.
- [IvanMurzak/Unity-MCP](https://github.com/IvanMurzak/Unity-MCP) — ⭐ 3.2k AI Skills, MCP Tools & CLI for Unity. Any C# method → tool with one line.
- [CoderGamester/mcp-unity](https://github.com/CoderGamester/mcp-unity) — ⭐ 1.8k MCP plugin connecting Unity Editor with Cursor, Claude Code, Codex, Windsurf.
- [AnkleBreaker-Studio/unity-mcp-server](https://github.com/AnkleBreaker-Studio/unity-mcp-server) — ⭐ 284 268 tools: scene, GameObjects, Shader Graph, terrain, physics, NavMesh, animation, MPPM multiplayer.
- [hatayama/unity-cli-loop](https://github.com/hatayama/unity-cli-loop) — ⭐ 406 CLI-driven AI loop for Unity: Editor → Play Mode automation.

#### Godot

- [Coding-Solo/godot-mcp](https://github.com/Coding-Solo/godot-mcp) — ⭐ 4.3k MCP for Godot engine. Launch editor, run projects, capture debug output.
- [hi-godot/godot-ai](https://github.com/hi-godot/godot-ai) — ⭐ 657 Production-grade MCP + AI tools. Snap install, free.
- [youichi-uda/godot-mcp-pro](https://github.com/youichi-uda/godot-mcp-pro) — ⭐ 448 162 tools: scene, animation, 3D, physics, particles, audio, shader, input sim, navigation, testing.
- [tugcantopaloglu/godot-mcp](https://github.com/tugcantopaloglu/godot-mcp) — ⭐ 287 149 tools for full Godot 4.x engine control.
- [yurineko73/Godot-MCP-Native](https://github.com/yurineko73/Godot-MCP-Native) — ⭐ 322 Native Godot MCP via HTTP — no dependency installation needed.

#### Unreal Engine

- [chongdashu/unreal-mcp](https://github.com/chongdashu/unreal-mcp) — ⭐ 2k Control Unreal Engine via natural language through MCP.
- [flopperam/unreal-engine-mcp](https://github.com/flopperam/unreal-engine-mcp) — ⭐ 1k Create entire towns, castles, mansions, mazes with AI in UE 5.5+.
- [Natfii/UnrealClaude](https://github.com/Natfii/UnrealClaude) — ⭐ 799 Claude Code CLI integration for UE 5.7 with built-in UE documentation context.
- [tumourlove/monolith](https://github.com/tumourlove/monolith) — ⭐ ~500 1,400+ actions across Blueprints, Materials, Niagara, Animation, Mesh, AI, GAS, UI, Audio.
- [ChiR24/Unreal_mcp](https://github.com/ChiR24/Unreal_mcp) — ⭐ 736 Native C++ Automation Bridge plugin for comprehensive MCP.

#### Roblox Studio

- [Roblox/studio-rust-mcp-server](https://github.com/Roblox/studio-rust-mcp-server) — ⭐ 471 Official Roblox MCP Server (standalone). By Roblox Inc.
- [boshyxd/robloxstudio-mcp](https://github.com/boshyxd/robloxstudio-mcp) — ⭐ 471 Create agentic AI workflows in ROBLOX Studio.
- **[@weppy/roblox-mcp](https://www.npmjs.com/package/@weppy/roblox-mcp)** — Real-time Roblox Studio integration for AI coding agents.

#### Minecraft

- [yuniko-software/minecraft-mcp-server](https://github.com/yuniko-software/minecraft-mcp-server) — ⭐ 627 Control Minecraft character in real-time — build, explore, interact via natural language.

### 3D Modeling & Blender

- [ahujasid/blender-mcp](https://github.com/ahujasid/blender-mcp) — ⭐ 23k **The #1 game-dev-adjacent MCP.** Open-source Blender control with any LLM.
- [3DSceneAgent/Vibe3DScene](https://github.com/3DSceneAgent/Vibe3DScene) — ⭐ 87 Create 3D scenes from words via Blender MCP + LangGraph.

### Pixel Art & Sprite

- [willibrandon/pixel-plugin](https://github.com/willibrandon/pixel-plugin) — ⭐ 226 Claude Code plugin for Aseprite pixel art — animation, retro palettes, dithering.
- [willibrandon/pixel-mcp](https://github.com/willibrandon/pixel-mcp) — ⭐ 89 MCP server for Aseprite pixel art creation via AI.
- [youichi-uda/aseprite-mcp-pro](https://github.com/youichi-uda/aseprite-mcp-pro) — ⭐ 18 121 tools for sprites, drawing, animation, palettes, export, + Godot integration.
- **PixelLab** (Smithery) — Generate animated pixel art characters, tilesets, and objects.
- **Spritesheet Forge** (Smithery) — PNG→spritesheet, GIF→frames, split spritesheets, trim PNG.

### Audio & Music

- [pasie15/mcp-server-musicgpt](https://github.com/pasie15/mcp-server-musicgpt) — MCP for MusicGPT AI audio API — music generation, voice conversion, 24 tools.
- [frankxai/suno-mcp-server](https://github.com/frankxai/suno-mcp-server) — MCP for Suno AI music generation.
- [wynandw87/claude-code-elevenlabs-mcp](https://github.com/wynandw87/claude-code-elevenlabs-mcp) — ElevenLabs TTS, sound effects, music, voice cloning for Claude Code.

### Procedural Generation & World Building

- [MushroomFleet/zero-vector-MCP](https://github.com/MushroomFleet/zero-vector-MCP) — Deterministic procedural generation — seed-based world building, terrain & content systems.
- [DangerBlack/fantasy-world-mcp](https://github.com/DangerBlack/fantasy-world-mcp) — Procedural fantasy world generation and evolution simulation.
- [shawn0326/texture-mcp](https://github.com/shawn0326/texture-mcp) — Procedural texture generation via semantic presets.

### Game Modding & Emulation

- [Gennadiyev/STS2MCP](https://github.com/Gennadiyev/STS2MCP) — ⭐ 416 Full agentic runs for Slay the Spire 2. Exposes in-game state via MCP.
- [drhelius/Gearboy](https://github.com/drhelius/Gearboy) — ⭐ 1.2k Game Boy / GBC emulator with embedded MCP server for AI debugging.
- [drhelius/Gearsystem](https://github.com/drhelius/Gearsystem) — ⭐ 374 Sega Master System / Game Gear emulator with embedded MCP server.
- **ROMulus** (Smithery, 19.7k uses) — Retro gaming ROM search engine for 28 consoles.
- **HytaleModder** (Smithery) — Access Hytale API docs for modding via MCP.

### Multi-Engine Tools

- [tykisgod/quick-question](https://github.com/tykisgod/quick-question) — ⭐ 10 Control plane for game-dev agents. Compile/test/review loop across Unity, Godot, Unreal, S&box. 26 slash commands.

## Harness Best Practices

Best practices for authoring cross-platform agent skills and managing agent harnesses.

### What Is a Harness?

A **harness** is the runtime that hosts agent skills — e.g. Claude Code, OpenCode, Cursor, Gemini CLI. It differs from a *framework* (build-time toolkit like LangChain) or an *agent* (a single LLM instance with prompt + tools).

| Concept | Role | Example |
|---|---|---|
| **Harness** | Runtime that hosts + orchestrates agents | Claude Code CLI, OpenCode, Cursor |
| **Framework** | Library for constructing agents | LangChain, CrewAI, Mastra |
| **Agent** | Single LLM instance with prompt + tools | Build, Plan, a subagent |
| **Skill** | Portable instruction package (`SKILL.md`) | code-review, restriction-ensure |
| **MCP Server** | External tool via Model Context Protocol | Filesystem, GitHub, Playwright |

### Skill Standard

The **[Agent Skills Standard](https://agentskills.io)** ([agentskills/agentskills](https://github.com/agentskills/agentskills) — ⭐ 21k) is the universal format, adopted by 25+ products:

```
my-skill/
├── SKILL.md          # YAML frontmatter + Markdown body
├── scripts/          # Executable code (optional)
├── references/       # Deep docs loaded on demand
└── assets/           # Templates, resources
```

**Required frontmatter:** `name` (1-64 chars, lowercase-hyphenated), `description` (1-1024 chars, front-load trigger keywords).

### Cross-Harness Compatibility

#### The `.agents/skills/` Interop Path

All major harnesses recognize `.agents/skills/` as a universal alias, alongside their native paths:

| Harness | Native Path | Interop Path |
|---|---|---|
| Claude Code | `.claude/skills/` | `.agents/skills/` |
| OpenCode | `.opencode/skills/` | `.agents/skills/` |
| Cursor | `.cursor/skills/` | `.agents/skills/` |
| Gemini CLI | `.gemini/skills/` | `.agents/skills/` |
| Copilot | `.github/skills/` | `.agents/skills/` |

#### DOs and DON'Ts

| DON'T (tool-specific) | DO (action-oriented) |
|---|---|
| "Use the `Read` tool to open the file" | "Open the file" |
| "Use `Bash` to run `npm test`" | "Run `npm test`" |
| "Call `Grep` with pattern X" | "Search for pattern X" |
| "Spawn a subagent via `Task`" | "Delegate to a subagent" |

**Why:** Codex has no `Read`/`Edit`/`Bash` vocabulary — the model picks tools from the action described. OpenCode uses lowercase names. Cursor has its own vocabulary. **Describe the action, not the tool.**

#### Skill Body Size

- Keep under **8 KB** for Codex CLI compatibility
- Move detailed reference material to `references/` subfolder
- Keep `SKILL.md` under **500 lines**

### Major Harness Comparison

| Harness | Source | Skill Discovery | Permissions | Context File | Subagents |
|---|---|---|---|---|---|
| **[Claude Code](https://code.claude.com)** | Proprietary | `.claude/skills/`, marketplace | `allowed-tools` per skill | `CLAUDE.md` | `Task` tool |
| **[OpenCode](https://opencode.ai)** | Open (160k⭐) | `.opencode/skills/`, `.agents/skills/`, `.claude/skills/` | Per-command globs (`allow/ask/deny`) | `AGENTS.md` | `task` tool |
| **[Cursor](https://cursor.com)** | Proprietary | `.cursor/skills/`, marketplace | Toggle (read-only) | `AGENTS.md`, `.cursorrules` | Via delegation |
| **[Gemini CLI](https://geminicli.com)** | Open | `.gemini/skills/`, extensions | Trusted folders, sandboxing | `GEMINI.md` | `@agent` syntax |
| **[Codex CLI](https://codex.cli)** | Open | `.codex/skills/` | Sandbox only | `AGENTS.md` (32KB cap) | Prose |
| **[GitHub Copilot](https://github.com/features/copilot)** | Proprietary | `.github/skills/`, `gh skill` | Via VS Code | `.github/copilot-instructions.md` | Cloud agent |
| **[Kiro](https://kiro.dev)** | Proprietary | `.kiro/skills/` | — | — | — |

### Notable Cross-Harness Collections

- [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) — ⭐ 65k Production-grade engineering skills. 24 skills across Define→Plan→Build→Verify→Review→Ship lifecycle. Each harness gets native artifacts — not lowest-common-denominator translations.
- [wshobson/agents](https://github.com/wshobson/agents) — ⭐ 37k Multi-harness plugin marketplace. 84 plugins shipping to 6 harnesses via adapter-driven architecture (single Markdown source → per-harness artifacts).

### Skill Authoring Practices

From addyosmani/agent-skills: **anti-rationalization table** — common excuses agents use to skip steps, with documented counter-arguments. Verification is non-negotiable ("seems right" is never sufficient). `SKILL.md` is an entry point; references load on demand.

From wshobson/agents: **plugin-eval framework** with three tiers — static analysis (<2s), LLM Judge across 4 dimensions (~30s), Monte Carlo simulation of 50-100 runs (~2-5min). Portability linters catch tool-specific references, size cap violations, and name collisions.

### Skill vs Plugin vs MCP vs Command

| Mechanism | Best For | Portable |
|---|---|---|
| **Skill** | Knowledge + instructions + optional scripts | Yes (Agent Skills standard) |
| **Plugin** | Bundled skills + agents + hooks + MCP | Varies (harness-specific) |
| **MCP Server** | External tool integration (APIs, databases) | Yes (open protocol) |
| **Command** | One-shot slash action | Detached from skill standard |

### Emerging Trends

- **`.agents/skills/`** as the universal interop path across all major harnesses
- **Adapter-based multi-harness shipping** (single source → per-harness artifacts) as production pattern
- **MCP** as the cross-harness standard for external tool integration
- **Progressive disclosure** loading: metadata → instructions → resources
- **OpenCode's permission model** leading in granularity (per-command glob patterns)
- **Skill evaluation** moving from static linters to LLM Judge to Monte Carlo simulation

## Contribute

PRs welcome! Submit additions via pull request.
