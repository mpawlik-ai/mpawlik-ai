## Michał Pawlik

**AI Product engineer — agentic systems & RAG.** I design and ship production LLM systems end to end: architecture,
code, deployment, and the product decisions behind them. Gdańsk, Poland (CET/CEST).

### Selected systems I've built

- **Legal AI platform — production.** Multi-tenant legal research and drafting over a corpus of 350,000+
  legal documents. The model is never trusted with facts: it answers only through search over that corpus,
  and every citation it produces is checked against the source database by deterministic code — no second
  model in the loop — so a provision that was repealed, or never existed, cannot reach a lawyer unmarked.
  Drafting runs as a multi-stage pipeline with parallel research passes and a review stage that can reject
  a draft and send it back for revision.
- **AI voice agent for healthcare scheduling — MVP.** Inbound calls that end in a real booked appointment in
  **Epic**, the EHR most large US health systems run on — not a note for someone to type in later. Slot search
  and booking go over FHIR, every write is gated behind explicit spoken confirmation, and a crisis check runs
  deterministically as the first step of every turn. Built against Epic's public sandbox with synthetic
  patients; not deployed in a hospital.
- **Durable agentic task engine.** Agent runs that survive a crash, a restart or a killed process and resume
  exactly where they stopped, instead of repeating expensive model calls. Failed runs retry, poisoned ones are
  quarantined, orphans are recovered on startup, and every step is traced with cost and latency.
- **Utility settlement engine for a commercial property — production.** Splitting electricity, water and
  heating costs across the tenants of a commercial building: supplier invoices in a dozen formats, sub-meter
  readings per unit, rates that change mid-period, advances to reconcile against actual consumption. The model
  reads the documents; allocation, aggregation and arithmetic are deterministic code and SQL, so every number
  traces back to a specific invoice line or meter reading and a re-run produces an identical result.
- **Retail analytics and compensation engine.** Per-store profitability that drives staff bonuses and the rent
  threshold the business can afford on a new location.

### Stack

Python (async, FastAPI, pytest) · TypeScript, Next.js · LangGraph, pydantic-graph, MCP servers ·
OpenAI / Anthropic / Gemini APIs, multi-provider routing · RAG — chunking, embeddings, reranking, citation
verification, evaluation suites · PostgreSQL, Supabase, pgvector · Temporal, Docker, OpenTelemetry, CI/CD

The systems above live in private repositories — client and product work.

📫 michal@nectoa.com
