<!-- Header -->
<div align="center">

```
███████╗██████╗ ██╗   ██╗██████╗ ███████╗
██╔════╝██╔══██╗██║   ██║██╔══██╗██╔════╝
█████╗  ██████╔╝██║   ██║██████╔╝█████╗  
██╔══╝  ██╔══██╗██║   ██║██╔══██╗██╔══╝  
███████╗██████╔╝╚██████╔╝██████╔╝███████╗
╚══════╝╚═════╝  ╚═════╝ ╚═════╝ ╚══════╝
```

### Hi, I'm Ebube Ireneaus 👋
**Fullstack Engineer — Vue/Nuxt/Next + Python/FastAPI**

*I build production-grade web systems, end to end — frontend, backend, infra, and the AI layer when it's needed.*

[![X](https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/EbubeIreneaus)
[![Portfolio](https://img.shields.io/badge/Portfolio-FF4500?style=for-the-badge&logo=firefox&logoColor=white)](https://ebube-dev.netlify.app)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ireneaus.ebube@gmail.com)

</div>

---

## 🧠 What I Do

I design and ship **full production systems** — not tutorials, not CRUD demos. Auth with refresh tokens, background workers, rate limiting, CI/CD, real payment integrations, and tests that actually run in a pipeline.

- 🖥️ **Fullstack web apps** — Vue/Nuxt & Next on the frontend, FastAPI on the backend, wired together properly
- 💳 **Payments & multi-tenant logic** — Stripe/Paystack integrations, per-vendor order splitting, scoped data access
- ⚙️ **Infrastructure that survives production** — Docker, background job queues (ARQ/Redis), CI/CD via GitHub Actions, rate limiting, caching
- 🤖 **AI/LLM integration where it earns its place** — LangChain agents, retrieval pipelines, and automation — built as a feature of a real product, not the whole pitch

---

## 🛠️ Tech Stack

**Frontend**

![Vue.js](https://img.shields.io/badge/Vue.js-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)
![Nuxt](https://img.shields.io/badge/Nuxt-00DC82?style=flat-square&logo=nuxtdotjs&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

**Backend & Data**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=python&logoColor=white)

**AI / Automation**

![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![CrewAI](https://img.shields.io/badge/CrewAI-6E40C9?style=flat-square&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)

**Infra & Tooling**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)

---

## 🚀 Featured Projects

### 🛒 16vmart — Multivendor E-commerce Platform
> A production-style multivendor marketplace where a single order spanning several stores automatically splits per store, so each vendor only ever sees their own products and sales.

**What it does:**
- 🔐 JWT auth with refresh tokens, scoped so each store can only manage its own products (not a full multi-tenant system, but properly access-controlled)
- 💳 Stripe payments with per-vendor order splitting on multi-store checkouts
- ⚙️ Background job processing via ARQ, rate limiting via SlowAPI, Pydantic validation on every route
- ✅ Tested with pytest (backend) and Playwright (frontend), deployed via GitHub Actions CI/CD

**Stack:** Nuxt.js · FastAPI · Docker · Redis · ARQ · PostgreSQL  
**Links:** [Repo](https://github.com/ebubeireneaus/16vmart) · [Live](https://16vmart.name.ng)

---

### 🔗 Onyx — SaaS URL Shortener
> Not a weekend clone — a shortener built like a real SaaS product, with custom domain support, visitor analytics, and tiered subscriptions.

**What it does:**
- 🌐 Custom subdomain and custom domain/subdomain support with DNS TXT verification + CNAME
- 📊 Visitor tracking by country, device, and IP
- 💳 Paystack subscription billing with tiered permission access
- ⚡ Redis caching and a background worker for async processing

**Stack:** Python · FastAPI · PostgreSQL · Redis · Docker  
**Repo:** [github.com/EbubeIreneaus/onyx](https://github.com/EbubeIreneaus/onyx)

---


### 🤖 Lumio — Autonomous AI Lead Qualification & Dispatch Platform
> A production-grade B2B lead qualification system: inbound leads are auto-qualified and answered using a RAG pipeline grounded in a company's own documents, with real-time dashboard updates and human review for low-confidence responses.

**What it does:**
- 📚 RAG engine on native PostgreSQL `pgvector` — ingests PDF/DOCX/TXT/MD, chunks with paragraph-aware splitting (1000 chars, 200-char overlap), grounds every AI response in retrieved context
- ⚡ Redis Pub/Sub event bridge pushing real-time WebSocket updates (<10ms) from background workers to the Nuxt dashboard
- 🛡️ Human-in-the-loop review queue — low-confidence or sensitive AI replies are staged as `PENDING` for operator approval before dispatch via Resend
- 🐳 Fully containerized: 5 services (API, worker, Postgres, Redis, dashboard) via Docker Compose

**Stack:** FastAPI · Nuxt 3 (SSR) · PostgreSQL (pgvector) · Redis Pub/Sub · Arq · Google Gemini  
**Repo:** [github.com/EbubeIreneaus/lumio](https://github.com/EbubeIreneaus/lumio)  
**Note:** no live hosted demo — the AI pipeline runs on a rate-limited free-tier key, so the repo is built to be cloned and run locally with your own API key. The dashboard's analytics section is a known work-in-progress.

---

---

## 📈 GitHub Stats

<div align="center">

![Ebube's GitHub Stats](https://github-readme-stats.vercel.app/api?username=EbubeIreneaus&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=EbubeIreneaus&layout=compact&theme=tokyonight&hide_border=true&langs_count=6)

![GitHub Streak](https://streak-stats.demolab.com?user=EbubeIreneaus&theme=tokyonight&hide_border=true)

</div>

---

## 💼 Open to Work

I'm looking for a **remote fullstack role** — startups, product teams, or companies that need someone who can own a feature from database schema to deployed UI.

📬 **ireneaus.ebube@gmail.com** · [Portfolio](https://ebube-dev.netlify.app)

---

<div align="center">

*Six years freelancing taught me to ship things that actually work in production — not just in a demo.*

</div>
