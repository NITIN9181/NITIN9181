# Nitin Savio Bada

### AI engineer building finance/accounting systems that must be correct.

I build production AI for finance & accounting — multimodal document understanding, double-entry
correctness, anomaly/fraud detection, and audit-grade ledgers. Full-stack on **FastAPI + Next.js**,
where being *approximately right* is a bug.

`M.Sc Mathematics & Computing` · India ·
[![LeetCode Knight](https://img.shields.io/badge/LeetCode-Knight%20·%20top%203%25%20·%201971%20·%20500%2B-FFA116?logo=leetcode&logoColor=white)](https://leetcode.com/u/savio0000000000)

---

## → Featured Projects

### · 1. Receipt → Journal Entry Generator — *flagship*
**Turns receipts/invoices into balanced double-entry journal entries — or quarantines them.**

[![Live Demo](https://img.shields.io/badge/Live_Demo-000?logo=vercel&logoColor=white)](https://artificial-intelligence-receipt-to.vercel.app)
[![Code](https://img.shields.io/badge/Code-181717?logo=github&logoColor=white)](https://github.com/NITIN9181/Artificial-Intelligence-Receipt-to-Journal-Entry-Generator)

- **Hardest engineering decision — untrusted-AI validation + the balance invariant:** the LLM is treated
  as untrusted. No entry posts unless `sum(debits) == sum(credits)`; failures are **quarantined**, never
  silently corrected. The posted ledger is **immutable** — you fix mistakes with a reversing entry, not an edit.
- **Stack:** Next.js 16 / React 19, FastAPI, SQLAlchemy (async), Pydantic, NVIDIA NIM + Ollama, Supabase/Postgres.
  Preparer / Reviewer / Admin approval. GnuCash chart-of-accounts import/export.

### 2. Accounts-Payable Workflow AI Agent
**End-to-end AP: OCR → three-way match → anomaly check → tiered approval, with an immutable audit log.**

[![Live Demo](https://img.shields.io/badge/Live_Demo-000?logo=vercel&logoColor=white)](https://ap-workflow-frontend.vercel.app)
[![Code](https://img.shields.io/badge/Code-181717?logo=github&logoColor=white)](https://github.com/NITIN9181/Accounts-Payable-Workflow-AI-Agent)

- **Hardest engineering decision — vendor-relative anomalies:** a $50k invoice is routine for one vendor and
  fraud for another. Z-score + Isolation Forest score each invoice against **that vendor's own baseline**, not a
  global mean. SHA-256 + fuzzy dedupe stops double-pays; LLM exception explanations fall back to templates.
- **Stack:** FastAPI, React/TypeScript, PostgreSQL, Redis, scikit-learn. WebSocket real-time, SLA-tiered
  approvals, circuit breakers.

### 3. Bank Anomaly Detection Engine
**Real-time transaction fraud detection with fraud-ring graphs and explainable, what-if scoring.**

[![Live Demo](https://img.shields.io/badge/Live_Demo-000?logo=vercel&logoColor=white)](https://bank-anomaly-detection-engine.vercel.app)
[![Code](https://img.shields.io/badge/Code-181717?logo=github&logoColor=white)](https://github.com/NITIN9181/Bank-Anomaly-Detection-Engine)

- **Hardest engineering decision — make fraud scores defensible:** every Isolation Forest score is paired with a
  statistical layer, an explanation, a what-if simulator, and an **adversarial red-team suite** — so analysts can
  triage, not just trust a black box. Cross-account fraud rings are surfaced as a D3 graph.
- **Stack:** FastAPI, React, scikit-learn, NVIDIA NIM, Plaid.

<!-- [4th — only if Finance-Copilot qualifies]
### 4. Finance Copilot (Chrome Extension)
**[FILL: one-line value prop]**
[![Code](https://img.shields.io/badge/Code-181717?logo=github&logoColor=white)](https://github.com/NITIN9181/Finance-Copilot-Chrome-Extension)
[![Demo](https://img.shields.io/badge/Walkthrough-Loom-625df5?logo=loom&logoColor=white)]([FILL: Loom URL])
- **Hardest engineering decision:** [FILL]
- **Stack:** TypeScript, [FILL]
- **Built in:** [FILL: timeframe]
-->

---

## 🎯 Why correctness

I come from an **M.Sc in Mathematics & Computing**, so I treat financial software like a proof — the
invariants are non-negotiable:

- **Debits must equal credits.** Unbalanced entries don't post; they quarantine.
- **Posted ledgers are immutable.** Corrections are reversing entries, never edits.
- **Every state change leaves an audit trail.**
- **AI output is a claim to be validated, not a result to be trusted.**

---

## 🛠 Tech stack

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000?logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?logo=sqlalchemy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![NVIDIA NIM](https://img.shields.io/badge/NVIDIA_NIM-76B900?logo=nvidia&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?logo=supabase&logoColor=white)

---

## ▪ GitHub

![Nitin's GitHub stats](https://github-readme-stats.vercel.app/api?username=NITIN9181&show_icons=true&hide_border=true&hide=prs,issues&card_width=450)

📫 **[LinkedIn](https://www.linkedin.com/in/nitinsaviobada/)** · open to AI-native finance/accounting roles.
