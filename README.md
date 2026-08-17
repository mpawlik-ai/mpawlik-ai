## Michał Pawlik

**AI engineer — agentic systems & RAG.** I design and ship production LLM systems end to end: architecture,
code, deployment, and the product decisions behind them. Gdańsk, Poland (CET/CEST).

### Systems I've built

- **Legal AI platform — production.** A multi-tenant research and drafting system where the model is never
  trusted with facts: it answers only through search over a legal corpus, and every reference it returns is
  verified in code before a lawyer can rely on it.
- **Durable agentic task engine.** Agent runs that survive a crash, a restart or a killed process and resume
  exactly where they stopped, instead of repeating expensive model calls. Failed runs retry, poisoned ones are
  quarantined, every step is traced with cost and latency.
- **Voice agent for healthcare scheduling — MVP.** Inbound calls that end in a persisted appointment record
  rather than a note for someone to type in later, with every write gated behind explicit spoken confirmation.
  Built against a sandbox with synthetic patients, never deployed in a hospital.
- **Document-parsing settlement engine — production.** Messy supplier invoices in, reproducible per-tenant
  settlements out. The model reads documents; deterministic code and SQL do the arithmetic, so the same inputs
  always produce the same numbers.
- **Retail analytics and compensation engine.** Per-store profitability that drives staff bonuses and the rent
  threshold for new locations.

### Stack

Python (async, FastAPI, pytest) · TypeScript, Next.js · LangGraph, pydantic-graph, MCP servers ·
OpenAI / Anthropic / Gemini APIs, multi-provider routing · RAG — chunking, embeddings, reranking, citation
verification, evaluation suites · PostgreSQL, Supabase, pgvector · Temporal, Docker, OpenTelemetry, CI/CD

### About this profile

Most of my work is client and product code under NDA, so this profile hosts extracted, self-contained pieces
rather than the systems above.

📫 michal@nectoa.com
