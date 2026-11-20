# Hi, I'm Purujit Vij 👋

**Senior Software Engineer | AI Agents, MCP & Backend Systems | TypeScript**  
📍 Solan, Himachal Pradesh, India (remote) · 🏢 Senior Software Engineer at **Hundred Solutions (Dversi)**, Oslo, Norway  
🌐 [purujit.com](https://purujit.com) · [CV](https://purujit.com/cv.pdf)

---

### 🚀 About Me

I build AI agents and the backends they run on.

At **Hundred Solutions** I lead the architecture of **Dversi**, an AI agent platform where companies build agents and workflows on their own business systems; it runs property risk assessment in production for a Nordic insurer. 1,300+ commits across the backend, admin app, integrations and infrastructure, and promoted to Senior 13 months after joining.

What I've shipped there:
- **Multi-cloud models:** bring-your-own-key support for Azure AI Foundry, AWS Bedrock and Vertex AI, and a model registry that auto-discovers customer models.
- **Tool search**, so agents with large MCP tool sets don't overload the context window or break prompt caching.
- **MCP connectors** for WhatsApp, Telegram, Jira, Microsoft 365, LinkedIn and Odoo, migrated to MCP SDK v2 with Streamable HTTP sessions.
- **Next.js admin app:** workflow editor with branching, per-tool approval for agents, and OAuth server connections.
- **Backend and infrastructure:** hardened a multi-tenant Express and PostgreSQL API (cross-tenant scope checks, rate limiting, 36 CodeQL alerts closed) and cut AWS ECS deploys from tens of minutes to a few with Docker and Terraform.

Before that: three years of React and React Native, shipping apps used by 1,000+ people and dashboards scoring 95–100 on Lighthouse.

---

### 🌟 Featured Projects

#### 1. [MIRA — Adaptive Wellness Agent Platform](https://github.com/purujitvij/mira)
*An adaptive agentic system featuring multi-tiered safety gates that knows when to stop talking and hand off safely.*
- **Key Architecture:** C-SSRS mental health safety classifier, quarantined state extraction, pure planner over 10-item evidence-based libraries, and real-time reviewer queue (`/review`).
- **Results (Gemini 3.6 Flash, `npm run eval -- --compare`):** escalation accuracy 14/15 vs 10/15 baseline on the dev set, 16/16 vs 11/16 on a held-out set written after the rules were frozen. The baseline missed all 20 crisis cases across both models; the agent surfaced the crisis screen on all 20. Same code also benchmarked on Llama 3.1 8B.
- **Stack:** TypeScript, Next.js, Supabase (PostgreSQL with RLS), Clerk, Vercel

#### 2. [Kundli Engine — Astrology API & MCP Server](https://kundli-engine-eight.vercel.app)
*An astrology calculation engine in TypeScript, accurate to within 39 arcseconds of Swiss Ephemeris across 150 years of charts.*
- **Key Architecture:** calculation core served as a REST API with API keys and as an MCP server with 30 tools for AI agents.
- **Quality:** backed by 270+ Jest tests.
- **Stack:** TypeScript, Node.js, MCP, Vercel · [Live](https://kundli-engine-eight.vercel.app)

#### 3. [BeatRelay — Spotify AI Controller (MCP)](https://github.com/purujitvij/beatrelay)
*A chat agent that picks music to match the listener's mood and plays it on Spotify, built on my own MCP server.*
- **Key Architecture:** Dual-transport MCP server (stdio for local desktop agents, `StreamableHTTPServerTransport` for remote web clients) with 21 tools, session management with `mcp-session-id`, separate OAuth login per user, and Gemini 2.5 Pro function calling in the agent chat (`/chat`).
- **Tool Capabilities:** Full Spotify toolchain including playback manipulation (play/pause/seek/transfer), playlist creation, saved library curation, and live OpenAPI/Swagger documentation (`/docs`).
- **Stack:** TypeScript, Express, Next.js 16, React 19, Radix UI, Framer Motion, Vercel · [Live Demo](https://beatrealy.vercel.app)

#### 4. [Chess MCP & Engine Ecosystem](https://github.com/purujitvij/chess-mcp)
*MCP server connecting LLMs to the Stockfish UCI engine for gameplay and tactical analysis. Fork of turlockmike/chess-mcp with fixes submitted upstream.*
- **Open PRs on [turlockmike/chess-mcp](https://github.com/turlockmike/chess-mcp):**
  - **[PR #6](https://github.com/turlockmike/chess-mcp/pull/6):** Dynamic cross-platform Stockfish binary auto-discovery (M-series Apple Silicon, Intel Mac, Linux, Windows).
  - **[PR #7](https://github.com/turlockmike/chess-mcp/pull/7):** Pointed the lockfile back at the public npm registry so `npm install` works out of the box.
  - **[PR #8](https://github.com/turlockmike/chess-mcp/pull/8):** Multi-stage Debian Docker toolchain (`node:20-bookworm-slim`) resolving Cairo graphics dependencies.

---

### 🛠️ Tech Stack

```
Languages          : TypeScript, JavaScript, SQL, Python
AI                 : LLMs, AI agents, MCP servers, tool/function calling, RAG, pgvector, LangChain,
                     LLM evals, Claude / OpenAI / Gemini APIs, AWS Bedrock, Azure AI Foundry, Vertex AI
Backend            : Node.js, Express, PostgreSQL, Redis, REST APIs, OpenAPI, OAuth, Zod, Stripe
Cloud & DevOps     : AWS (ECS, EC2, S3, IAM), Docker, Terraform, GitHub Actions, Vercel, Supabase
Frontend & Mobile  : React, Next.js, React Native, Redux, TanStack Query, Tailwind CSS
```

---

### 📬 Connect With Me

- **Portfolio & CV:** [purujit.com](https://purujit.com)
- **LinkedIn:** [linkedin.com/in/purujit-vij](https://www.linkedin.com/in/purujit-vij)
- **Email:** [vijpurujit@gmail.com](mailto:vijpurujit@gmail.com)
- **Twitter / X:** [@PurujitVij](https://x.com/PurujitVij)

---
*Open to collaborating on agentic AI systems, MCP tooling and backend systems.*
