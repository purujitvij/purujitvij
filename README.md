# Hi, I'm Purujit Vij 👋

**Senior Software Engineer | AI Agents & Infrastructure | MCP | Distributed Systems**  
📍 India (Operating Globally / Remote) · 🏢 Senior Software Engineer at **Dversi** (Oslo, Norway)

---

### 🚀 About Me

I am a Senior Software Engineer specializing in **autonomous AI agent architectures**, **Model Context Protocol (MCP) ecosystems**, and **distributed multi-tenant backends**. My engineering journey spans the entire stack — from mobile applications (React Native) and high-performance web interfaces to cloud infrastructure (AWS ECS, Docker) and agentic tool-calling systems.

At **Dversi**, I lead the architecture of enterprise AI agent platforms:
- Building production **MCP servers** that give AI models secure tool-calling access to enterprise ERP software.
- Architecting **entity-centric knowledge graphs** that unify ERP records, APIs, and unstructured context into single queryable intelligence layers.
- Designing **multi-tenant backends (NestJS/TypeScript)** with strict per-customer isolation and cloud deployments.

---

### 🧠 Core Architectural Pillars

- **🤖 AI Agents & Tool Calling:** Safety gates that can only raise the risk level, quarantined state extraction, deterministic memory pipelines, and LLM eval harnesses (Gemini, Claude, Llama).
- **🔌 Model Context Protocol (MCP):** Designing resilient, headless MCP server runtimes, stdio/SSE transports, and cross-platform native engine integrations.
- **☁️ Cloud & Distributed Infrastructure:** Multi-tenant NestJS, PostgreSQL with Row-Level Security (RLS), Supabase, AWS ECS deployment optimization, Docker multi-stage builds, and CI/CD pipelines.

---

### 🌟 Featured Repositories

#### 1. [MIRA — Adaptive Wellness Agent Platform](https://github.com/purujitvij/mira)
*An adaptive agentic system featuring multi-tiered safety gates that knows when to stop talking and hand off safely.*
- **Key Architecture:** C-SSRS mental health safety classifier, quarantined state extraction, pure planner over 10-item evidence-based libraries, and real-time reviewer queue (`/review`).
- **Results (Gemini 3.6 Flash, `npm run eval -- --compare`):** escalation accuracy 14/15 vs 10/15 baseline on the dev set, 16/16 vs 11/16 on a held-out set written after the rules were frozen. The baseline missed all 20 crisis cases across both models; the agent surfaced the crisis screen on all 20. Same code also benchmarked on Llama 3.1 8B.
- **Stack:** TypeScript, Next.js, Supabase (PostgreSQL with RLS), Clerk, Vercel · [Live Demo](https://mira.slayertunnel.xyz)

#### 2. [BeatRelay — Spotify AI Controller (MCP)](https://github.com/purujitvij/beatrealy)
*Full-stack Spotify integration and AI agent controller powered by Model Context Protocol (MCP) HTTP streaming and Next.js 16.*
- **Key Architecture:** Dual-transport MCP server (stdio for local desktop agents, `StreamableHTTPServerTransport` for remote web clients), session management with `mcp-session-id`, and interactive agent chat interface (`/chat`).
- **Tool Capabilities:** Full Spotify toolchain including playback manipulation (play/pause/seek/transfer), playlist creation, saved library curation, and live OpenAPI/Swagger documentation (`/docs`).
- **Stack:** TypeScript, Express, Next.js 16, React 19, Radix UI, Framer Motion, Vercel · [Live Demo](https://beatrealy.vercel.app)

#### 3. [Chess MCP & Engine Ecosystem](https://github.com/purujitvij/chess-mcp)
*MCP server connecting LLMs to the Stockfish UCI engine for gameplay and tactical analysis. Fork of turlockmike/chess-mcp with fixes submitted upstream.*
- **Open PRs on [turlockmike/chess-mcp](https://github.com/turlockmike/chess-mcp):**
  - **[PR #6](https://github.com/turlockmike/chess-mcp/pull/6):** Dynamic cross-platform Stockfish binary auto-discovery (M-series Apple Silicon, Intel Mac, Linux, Windows).
  - **[PR #7](https://github.com/turlockmike/chess-mcp/pull/7):** Pointed the lockfile back at the public npm registry so `npm install` works out of the box.
  - **[PR #8](https://github.com/turlockmike/chess-mcp/pull/8):** Multi-stage Debian Docker toolchain (`node:20-bookworm-slim`) resolving Cairo graphics dependencies.

---

### 🛠️ Tech Stack & Tooling

```
Core Languages       : TypeScript, JavaScript, Python, SQL, C++ (UCI tools)
Backend & Cloud      : Node.js, NestJS, Next.js, Express, PostgreSQL, Supabase, Redis
DevOps & Infra       : AWS (ECS, S3), Docker (Multi-stage), GitHub Actions, CI/CD
AI & Protocols       : Model Context Protocol (MCP), Claude API, Gemini API, LLM Evals
Mobile & Frontend    : React, React Native, TailwindCSS, Lighthouse Optimization
```

---

### 📬 Connect With Me

- **LinkedIn:** [linkedin.com/in/purujit-vij](https://www.linkedin.com/in/purujit-vij)
- **Email:** [vijpurujit@gmail.com](mailto:vijpurujit@gmail.com)
- **Twitter / X:** [@PurujitVij](https://x.com/PurujitVij)
- **GitHub:** [github.com/purujitvij](https://github.com/purujitvij)
- **Portfolio & Live Demos:** [MIRA](https://mira.slayertunnel.xyz) · [BeatRelay](https://beatrealy.vercel.app)

---
*Open to collaborating on agentic AI systems, MCP tooling, and distributed backends.*
