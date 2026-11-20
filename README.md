# Hi, I'm Purujit Vij 👋

**Senior Software Engineer | AI Agents, MCP & Backend Systems | TypeScript**  
📍 Solan, Himachal Pradesh, India (remote) · 🏢 Senior Software Engineer at **Hundred Solutions (Dversi)**, Oslo, Norway  
🌐 [purujit.com](https://purujit.com) · [About](https://purujit.com/about/) · [Work notes](https://purujit.com/work/) · [CV](https://purujit.com/cv.pdf)

---

### 🚀 About Me

I build AI agents and the backends they run on. I like the ambiguous 0→1 part: turning a fuzzy problem into a clear system design, then shipping software that behaves safely in production.

At **Hundred Solutions** I lead the architecture of **Dversi**, an AI agent platform where companies build agents and workflows on their own business systems; it runs property risk assessment in production for a Nordic insurer. 1,300+ commits across the backend, admin app, integrations and infrastructure, and promoted to Senior 13 months after joining.

What I've shipped there:
- **Multi-cloud models:** bring-your-own-key support for Azure AI Foundry, AWS Bedrock and Vertex AI, and a model registry that auto-discovers customer models.
- **Tool search**, so agents with large MCP tool sets don't overload the context window or break prompt caching.
- **MCP connectors** for WhatsApp, Telegram, Jira, Microsoft 365, LinkedIn and Odoo, migrated to MCP SDK v2 with Streamable HTTP sessions.
- **Next.js admin app:** workflow editor with branching, per-tool approval for agents, and OAuth server connections.
- **Backend and infrastructure:** hardened a multi-tenant Express and PostgreSQL API (cross-tenant scope checks, rate limiting, 36 CodeQL alerts closed) and cut AWS ECS deploys from tens of minutes to a few with Docker and Terraform.

Before that: three years of React and React Native, shipping apps used by 1,000+ people and dashboards scoring 95–100 on Lighthouse.

More about me, how I work and the path so far: [purujit.com/about](https://purujit.com/about/)

---

### 📝 Latest Case Study

#### [From $75+ to ~$15 a month: moving a live news CMS off Strapi Cloud with zero downtime](https://purujit.com/work/strapi-cloud-to-aws-zero-downtime/)
*A news publisher's Strapi CMS cost $75+ a month on Strapi Cloud, plus API overage charges. I moved it to their own AWS account, on one 1 GB server.*
- **💸 Cost:** $75+ a month plus overages → about $15 a month on AWS, roughly 80% less.
- **⏱️ Zero downtime:** 2,100 articles and 39,000 media files moved while the site stayed live, tested on a parallel hostname before the switch.
- **🔒 Security:** closed 44 public permissions and took Strapi from 13 critical vulnerabilities to 0, after testing the upgrade against a production snapshot.
- **🐛 Bugs found on the way:** a wrong-images bug caused by unordered queries, and a PDF reader that broke on S3 because of CORS.
- **Stack:** Strapi 5, AWS EC2 · S3 · IAM, SQLite, Caddy, systemd, GitHub Actions

More case studies and notes from the job: [purujit.com/work](https://purujit.com/work/)

---

### 🌟 Featured Projects

#### 1. [MIRA — Adaptive Wellness Agent Platform](https://github.com/purujitvij/mira)
*An adaptive agentic system featuring multi-tiered safety gates that knows when to stop talking and hand off safely.*
- **Key Architecture:** C-SSRS mental health safety classifier, quarantined state extraction, pure planner over 10-item evidence-based libraries, and real-time reviewer queue (`/review`).
- **Results (Gemini 3.6 Flash, `npm run eval -- --compare`):** escalation accuracy 14/15 vs 10/15 baseline on the dev set, 16/16 vs 11/16 on a held-out set written after the rules were frozen. The baseline missed all 20 crisis cases across both models; the agent surfaced the crisis screen on all 20. Same code also benchmarked on Llama 3.1 8B.
- **Stack:** TypeScript, Next.js, Supabase (PostgreSQL with RLS), Clerk, Vercel · [Live Demo](https://mira.slayertunnel.xyz)

#### 2. [Kundli Engine — Astrology API & MCP Server](https://kundli-engine-eight.vercel.app)
*An astrology calculation engine in TypeScript, accurate to within 39 arcseconds of Swiss Ephemeris across 150 years of charts.*
- **Key Architecture:** calculation core served as a REST API with API keys and as an MCP server with 30 tools for AI agents.
- **Quality:** 526 Jest tests, run on every pull request, including a benchmark against Swiss Ephemeris.
- **Hallucination control:** the model explains but never calculates; each tool returns one small block of the chart (146 KB → 3–8 KB), and unimplemented parts say "unavailable" instead of guessing.
- **Stack:** TypeScript, Node.js, MCP, Vercel · [Live](https://kundli-engine-eight.vercel.app) · [Case study](https://purujit.com/work/kundli-mcp-hallucination-control/)

#### 3. [BeatRelay — Mood-based Spotify agent on MCP](https://github.com/purujitvij/beatrelay)
*A chat agent that picks music for your mood and plays it on Spotify. Shipped in January 2026, four months before [Spotify launched mood playlists in Claude](https://newsroom.spotify.com/2026-04-23/claude-integration/).*
- **Built on:** [Marcel Marais's spotify-mcp-server](https://github.com/marcelmarais/spotify-mcp-server) (MIT), which provides the 21 Spotify tools for a single local user.
- **What I added:** a Streamable HTTP transport with a session per client (`mcp-session-id`), tools that run with each signed-in user's own Spotify token, a REST `/execute` endpoint with Swagger docs, and the Next.js chat where Gemini 2.5 Pro calls the tools in a capped loop and replies in English or Hinglish.
- **What was hard:** not the agent, but Spotify's rules. A new app stays in development mode, so until it has a privacy policy every user has to be added by hand to an allowlist in the Spotify developer dashboard, and playback control needed a Spotify Premium account.
- **Stack:** TypeScript, Express, Next.js 16, React 19, Gemini 2.5 Pro, Vercel · [Live Demo](https://beatrealy.vercel.app) · [Case study](https://purujit.com/work/beatrelay-mood-agent/)

#### 4. [Chess MCP & Engine Ecosystem](https://github.com/purujitvij/chess-mcp)
*MCP server connecting LLMs to the Stockfish UCI engine for gameplay and tactical analysis. Fork of turlockmike/chess-mcp with fixes submitted upstream.*
- **Open PRs on [turlockmike/chess-mcp](https://github.com/turlockmike/chess-mcp):**
  - **[PR #6](https://github.com/turlockmike/chess-mcp/pull/6):** Dynamic cross-platform Stockfish binary auto-discovery (M-series Apple Silicon, Intel Mac, Linux, Windows).
  - **[PR #7](https://github.com/turlockmike/chess-mcp/pull/7):** Pointed the lockfile back at the public npm registry so `npm install` works out of the box.
  - **[PR #8](https://github.com/turlockmike/chess-mcp/pull/8):** Multi-stage Debian Docker toolchain (`node:20-bookworm-slim`) resolving Cairo graphics dependencies.

---

### 🛠️ Tech Stack

**Languages**<br>
<img src="https://skillicons.dev/icons?i=ts,js,py" alt="TypeScript, JavaScript, Python" /><br>
<sub>+ SQL</sub>

**AI**<br>
<img src="https://img.shields.io/badge/MCP-000000?style=for-the-badge&logo=modelcontextprotocol&logoColor=white" alt="MCP" />
<img src="https://img.shields.io/badge/Claude-D97757?style=for-the-badge&logo=claude&logoColor=white" alt="Claude" />
<img src="https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white" alt="Gemini" />
<img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="LangChain" />
<img src="https://img.shields.io/badge/Vertex_AI-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white" alt="Vertex AI" /><br>
<sub>+ LLMs, AI agents, tool/function calling, RAG, pgvector, LLM evals, OpenAI API, AWS Bedrock, Azure AI Foundry</sub>

**Backend**<br>
<img src="https://skillicons.dev/icons?i=nodejs,express,postgres,redis" alt="Node.js, Express, PostgreSQL, Redis" />
<img src="https://img.shields.io/badge/Stripe-635BFF?style=for-the-badge&logo=stripe&logoColor=white" alt="Stripe" />
<img src="https://img.shields.io/badge/Zod-3E67B1?style=for-the-badge&logo=zod&logoColor=white" alt="Zod" />
<img src="https://img.shields.io/badge/OpenAPI-6BA539?style=for-the-badge&logo=openapiinitiative&logoColor=white" alt="OpenAPI" /><br>
<sub>+ REST APIs, OAuth</sub>

**Cloud & DevOps**<br>
<img src="https://skillicons.dev/icons?i=aws,docker,terraform,githubactions,vercel,supabase" alt="AWS, Docker, Terraform, GitHub Actions, Vercel, Supabase" /><br>
<sub>AWS: ECS, EC2, S3, IAM</sub>

**Frontend & Mobile**<br>
<img src="https://skillicons.dev/icons?i=react,nextjs,redux,tailwind" alt="React, Next.js, Redux, Tailwind CSS" />
<img src="https://img.shields.io/badge/TanStack_Query-FF4154?style=for-the-badge&logo=reactquery&logoColor=white" alt="TanStack Query" /><br>
<sub>+ React Native</sub>

---

### 🎧 Off the Clock

- 🎛️ **Behind the decks:** I DJ and mix songs. Finding tracks with the right BPM and key, then ordering them so each one flows into the next, is basically a sorting problem with taste as the comparator.
- 🍳 **In the kitchen:** cooking is what I do with free time.
- 🏔️ **Up in the mountains:** offbeat treks and long drives through the mountains are how I calm my head and reset.
- 🖥️ **Home lab:** a 2014 Dell laptop rebuilt as a home server: new SSD, SSH locked to key + password + TOTP with post-quantum key exchange, reached over Tailscale.

---

### 📬 Connect With Me

- **Portfolio & CV:** [purujit.com](https://purujit.com) · [About](https://purujit.com/about/)
- **Case studies & notes from the job:** [purujit.com/work](https://purujit.com/work/)
- **LinkedIn:** [linkedin.com/in/purujit-vij](https://www.linkedin.com/in/purujit-vij)
- **Email:** [vijpurujit@gmail.com](mailto:vijpurujit@gmail.com)
- **Twitter / X:** [@PurujitVij](https://x.com/PurujitVij)

---
*Open to collaborating on agentic AI systems, MCP tooling and backend systems.*
