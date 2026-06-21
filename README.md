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

## Contribute

PRs welcome! Submit additions via pull request.
