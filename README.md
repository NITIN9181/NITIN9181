<div align="center">

<h1>Nitin Savio Bada</h1>

<p>
<strong>Full-Stack Engineer &nbsp;·&nbsp; Production AI Systems &nbsp;·&nbsp; M.Sc Mathematics & Computing</strong>
</p>

<p>
I ship complete systems end-to-end — React / Next.js frontends, FastAPI backends,<br>
async Rust workers, Scala 3 / ZIO microservices, and AI pipelines with real correctness guarantees.
</p>

<p><b>40 repos · ~63,000 LOC · Python · TypeScript · Rust · Scala 3</b></p>

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nitinsaviobada/)
&nbsp;
[![LeetCode Knight](https://img.shields.io/badge/LeetCode-Knight_%C2%B7_Top_3%25-FFA116?logo=leetcode&logoColor=white)](https://leetcode.com/u/savio0000000000)

</div>

---

## → What I Build, End-to-End

| Layer | Technologies |
|-------|-------------|
| **Frontend** | React 18/19 · Next.js 16 App Router · TypeScript · Tailwind CSS · Vite · Astro 6 · Plasmo (Chrome Extension) |
| **Backend** | FastAPI (async + Pydantic v2) · Scala 3 / ZIO 2 (pure functional) · Rust (Tokio async) · Python asyncio |
| **AI / LLM** | CrewAI Flows · LangGraph StateGraph · custom goal-driven graph engines · NVIDIA NIM · OpenAI · DeepSeek · Claude · HuggingFace |
| **AI Patterns** | 3-tier model routing · circuit breakers · 5-stage JSON recovery · Redis-cached fallback chains · confidence floors |
| **Databases** | PostgreSQL · Redis · ClickHouse · BigQuery · FAISS (vector) · SQLite |
| **Event-Driven** | GCP Pub/Sub · Apache Kafka · Redis Streams · WebSocket · SSE |
| **Security** | AES-256-GCM zero-knowledge (client-only) · JWT · Redis rate limiting · PostgreSQL RLS multi-tenancy · immutable audit logs |
| **DevOps** | Docker Compose (11 repos) · Kubernetes + Helm (3 repos) · Vercel · Render · GitHub Actions |
| **Testing** | Hypothesis property-based · Playwright E2E · ZIO Test + Testcontainers · Cargo unit/integration · adversarial red-team suites |

---

## ◎ Featured Projects

### 1. 🧾 Receipt → Journal Entry Generator &nbsp; *(Flagship)*
**Multimodal AI that converts receipts and invoices into balanced double-entry journal entries — or quarantines them.**

[![Live Demo](https://img.shields.io/badge/Live_Demo-000?logo=vercel&logoColor=white)](https://artificial-intelligence-receipt-to.vercel.app)&nbsp;&nbsp;[![Code](https://img.shields.io/badge/Code-181717?logo=github&logoColor=white)](https://github.com/NITIN9181/Artificial-Intelligence-Receipt-to-Journal-Entry-Generator)

`Next.js 16` `React 19` `FastAPI` `PostgreSQL` `NVIDIA NIM` `Ollama` `Supabase`

> **Why it's hard:** The LLM is treated as untrusted input — no entry posts unless `sum(debits) == sum(credits)`. Failures quarantine; they never silently correct. A **5-stage JSON recovery pipeline** (strip → parse → json-repair → regex → human review) handles non-determinism. GnuCash chart-of-accounts import/export. Preparer / Reviewer / Admin approval workflow. Posted ledger is **immutable by DB trigger** — corrections via reversing entries only.

---

### 2. 🏢 Accounts-Payable Workflow AI Agent
**Full-stack AP automation: OCR → three-way match → vendor-relative anomaly scoring → SLA-tiered approval workflow.**

[![Live Demo](https://img.shields.io/badge/Live_Demo-000?logo=vercel&logoColor=white)](https://ap-workflow-frontend.vercel.app)&nbsp;&nbsp;[![Code](https://img.shields.io/badge/Code-181717?logo=github&logoColor=white)](https://github.com/NITIN9181/Accounts-Payable-Workflow-AI-Agent)

`React 18` `TypeScript` `FastAPI` `PostgreSQL` `Redis` `scikit-learn` `NVIDIA NIM` `WebSocket`

> **Why it's hard:** A $50k invoice is routine for one vendor and fraud for another. Z-score + Isolation Forest scores each invoice against **that vendor's own historical baseline** — not a global mean. SHA-256 + fuzzy dedup stops double-pays. Real-time WebSocket approvals with SLA timers. **18 Hypothesis property-based tests** covering audit invariants, ensemble anomaly math, and three-way matching idempotency.

---

### 3. 🔐 CipherDrop — Zero-Knowledge Encrypted File Sharing
**The server never sees the decryption key — by construction, not by policy.**

[![Code](https://img.shields.io/badge/Code-181717?logo=github&logoColor=white)](https://github.com/NITIN9181/CipherDrop)

`Next.js 16` `TypeScript` `Web Crypto API (AES-256-GCM)` `PostgreSQL` `Redis`

> **Why it's hard:** AES-256-GCM encryption / decryption runs entirely in the browser via the Web Crypto API. The key lives in the URL `#fragment` (RFC 3986) — never transmitted to the server, never logged, never stored. A **`zero-knowledge.spec.ts` Playwright test intercepts every HTTP request** in the share flow and fails the suite if the key appears anywhere on the wire.

---

### 4. 🔍 Distributed Technographic Discovery Engine
**Rust crawler → Python fingerprinter → TypeScript dashboard: three runtimes, one pipeline, row-level multi-tenancy.**

[![Code](https://img.shields.io/badge/Code-181717?logo=github&logoColor=white)](https://github.com/NITIN9181/Distributed-Technographic-Discovery-Engine)

`Rust (Tokio)` `Python` `TypeScript / React` `Redis Streams` `PostgreSQL RLS` `Kubernetes`

> **Why it's hard:** Each runtime was chosen for what it's best at — Rust for raw crawl throughput, Python for fingerprinting ecosystem breadth, TypeScript for UI. They coordinate via Redis Streams with backpressure. **PostgreSQL Row-Level Security** enforces per-tenant isolation at the database layer, not the application layer. Deployed on Kubernetes with independent horizontal scaling per service.

---

### 5. ✈️ Flight Watch — Event-Driven Aviation Analytics (Scala 3 / ZIO)
**5-microservice pipeline: live ADS-B ingest → anomaly detection → BigQuery analytics — pure functional, all the way down.**

[![Code](https://img.shields.io/badge/Code-181717?logo=github&logoColor=white)](https://github.com/NITIN9181/flightwatch)

`Scala 3` `ZIO 2` `GCP Pub/Sub` `BigQuery` `PostgreSQL` `ZIO Test` `Testcontainers`

> **Why it's hard:** Pure functional Scala 3 with ZIO 2 — no mutable state, no exceptions, errors are values. Each microservice is independently testable via **ZIO Test with Testcontainers** spinning up real PostgreSQL and emulated Pub/Sub. Correctness is a proof, not a hope.

---

### 6. 🤖 hive — Self-Evolving Multi-Agent Operating System
**Generates its own workflow graph topology at runtime and rewires itself on failure — not a hardcoded DAG.**

[![Code](https://img.shields.io/badge/Code-181717?logo=github&logoColor=white)](https://github.com/NITIN9181/hive)

`Python` `Claude API (Anthropic)` `FastAPI` `Custom Graph Engine` `Kubernetes`

> **Why it's hard:** Unlike CrewAI (static flows) or LangGraph (predefined graph), hive's entire topology is **generated by the coding agent at runtime**. Each node has a local reasoning model; edges are LLM-generated routing conditions. On failure, the graph re-evolves. Deployed on Kubernetes with per-node resource isolation and shared memory across nodes.

---

## ⚡ Engineering Principles I Always Apply

- **AI output is untrusted input** — validate invariants (balance equations, schema contracts, confidence floors) before any state mutation
- **3-tier model routing** — expensive reasoning models for complex planning only; route classification and retrieval to fast, cheap models  
- **Defense-in-depth for autonomous agents** — rate limits, confidence floors, cooldowns, protected flags, full audit trails before any irreversible action
- **Immutable audit logging** — every state transition captured before/after; posted records locked at the DB layer, corrected by reversal entries, never edits
- **Zero-knowledge by architecture** — key material stays in the browser; the server stores only ciphertext

---

## 🛠 Tech Stack

**Frontend**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000?logo=nextdotjs&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?logo=tailwindcss&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white)
![Astro](https://img.shields.io/badge/Astro-FF5D01?logo=astro&logoColor=white)

**Backend & Systems**

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?logo=rust&logoColor=white)
![Scala 3](https://img.shields.io/badge/Scala_3-DC322F?logo=scala&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?logo=sqlalchemy&logoColor=white)

**AI / LLM**

![NVIDIA NIM](https://img.shields.io/badge/NVIDIA_NIM-76B900?logo=nvidia&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?logo=openai&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?logo=langchain&logoColor=white)
![CrewAI](https://img.shields.io/badge/CrewAI-FF0000?logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?logo=huggingface&logoColor=000)

**Databases & Events**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white)
![ClickHouse](https://img.shields.io/badge/ClickHouse-FFCC01?logo=clickhouse&logoColor=000)
![Apache Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?logo=apachekafka&logoColor=white)
![BigQuery](https://img.shields.io/badge/BigQuery-4285F4?logo=googlebigquery&logoColor=white)

**Infrastructure**

![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?logo=googlecloud&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000?logo=vercel&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white)

---

## ▪ GitHub

[![Nitin's GitHub stats](https://github-readme-stats.vercel.app/api?username=NITIN9181&show_icons=true&hide_border=true&hide=prs,issues&card_width=450)](https://github.com/NITIN9181)

---

📫 **Open to full-stack and AI engineering roles** &nbsp;·&nbsp; [LinkedIn](https://www.linkedin.com/in/nitinsaviobada/) &nbsp;·&nbsp; [LeetCode — Knight · Top 3%](https://leetcode.com/u/savio0000000000)
