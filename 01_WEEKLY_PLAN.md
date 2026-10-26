# 12-Week Plan (starts 2026-11-02)

Daily constants: **30 min coding practice** (LeetCode medium/NeetCode, Python) · **1 behavioral/system-design item** per week day-slot · log in `06_TRACKER.md`.
Project numbers refer to `02_PROJECTS.md`.

## Phase A — Foundations & proof (Weeks 1–4)

### Week 1 (Nov 2) — System design core + portfolio setup
- Learn: system-design framework (requirements → capacity → API → data → scale → trade-offs); CAP/consistency, caching, queues, idempotency, rate limiting.
- Practice: 4 designs from the bank: URL shortener, rate limiter, notification system, job queue.
- Build: create public GitHub org/repo template, README standard, CI. Start **Project 1** repo skeleton.
- Deliverable: portfolio README + 2 design write-ups (Markdown, diagrams).

### Week 2 (Nov 9) — RAG done properly
- Learn: chunking, embeddings, hybrid search (BM25 + vectors), reranking, query rewriting, citations, RAG failure modes.
- Build: **Project 1 (Production RAG with evals)** — ingestion, pgvector/Chroma, hybrid retrieval, reranker, citations.
- Questions: bank §RAG (10 Qs).
- Deliverable: working RAG + 30-question eval set.

### Week 3 (Nov 16) — LLM evaluation & observability
- Learn: eval types (unit, LLM-as-judge, human), golden sets, regression gating, tracing (Langfuse/OpenTelemetry), cost/latency budgets.
- Build: add eval harness + CI gate + tracing to Project 1; dashboard of cost/latency/quality.
- **Start applying** (Tier 1–2) using the jobagent pipeline or manually; track in tracker.
- Deliverable: eval report with before/after retrieval improvements.

### Week 4 (Nov 23) — Agents & tool use (beyond CrewAI)
- Learn: ReAct/plan-execute, tool schemas, LangGraph state machines, Claude/OpenAI tool calling, MCP servers, human-in-the-loop, agent failure modes (loops, tool misuse).
- Build: **Project 2 (Multi-agent incident investigator)** — logs → hypothesis → remediation proposal, HITL approval. Mirrors your Datadog work with synthetic public data.
- Deliverable: Project 2 demo (GIF/video) + comparison note CrewAI vs LangGraph vs plain tool-calling.

## Phase B — Depth (Weeks 5–8)

### Week 5 (Nov 30) — Distributed/event-driven architecture
- Learn: Kafka internals (partitions, consumer groups, exactly-once vs at-least-once), outbox pattern, saga, CQRS, DLQ, backpressure, schema evolution.
- Build: **Project 3 (Event-driven energy marketplace)** — EV charging sessions → Kafka (Redpanda locally) → pricing consumer → ledger; outbox + idempotent consumers.
- Practice designs: EV charging platform, real-time pricing, payments ledger.
- Deliverable: architecture doc with failure-mode table, load test result.

### Week 6 (Dec 7) — ML fundamentals + serving
- Learn: metrics (precision/recall/AUC/PR), leakage, cross-validation, gradient boosting (LightGBM), feature stores, drift monitoring; serving (batch vs online), SageMaker endpoints, vLLM basics, quantization, LoRA overview.
- Build: **Project 4 (Dynamic pricing model + API)** — LightGBM demand/price model, FastAPI serving, drift check, A/B hook.
- Deliverable: model card + API + monitoring notebook.

### Week 7 (Dec 14) — AI security, governance, guardrails
- Learn: prompt injection (direct/indirect), data exfiltration, PII redaction, output validation, guardrail layers, red-teaming, OWASP LLM Top 10, EU AI Act basics, audit trails.
- Build: harden Project 2: injection test suite, PII filter, policy engine, audit log.
- Deliverable: threat model document (STRIDE for an agent system).

### Week 8 (Dec 21) — Cost, scale, and multi-tenant AI architecture
- Learn: prompt caching, model routing (small/large), batching, async, token budgeting, rate limits, multi-tenant isolation, vendor lock-in strategy, build-vs-buy.
- Build: add model router + cost dashboard to Project 1/2.
- Practice: case study "Design an enterprise AI assistant for 10k employees".
- Deliverable: reference architecture diagram + cost model spreadsheet.

## Phase C — Interview mode (Weeks 9–12)

### Week 9 (Dec 28) — Architect loop practice
- Learn: cloud well-architected pillars, Kubernetes essentials (deployments, HPA, ingress), IaC (Terraform basics), observability (metrics/logs/traces), DR/RTO/RPO, security (IAM, secrets).
- Practice: 3 full mock system designs (45 min each, timed, recorded) from the bank.
- Deliverable: 3 recorded mocks + self-review notes.

### Week 10 (Jan 4) — Flagship: **Project 5 (jobagent platform, public subset)**
- Build/polish the public parts: agent orchestration, verification agent, approval state machine, tests. Redact private data.
- Write a 1,500-word case study: problem, architecture, trade-offs, results.
- Deliverable: public repo + case study + 5-min demo video. This is your best portfolio piece.

### Week 11 (Jan 11) — Behavioral & leadership
- Prepare 8 STAR stories (`05_STORIES_AND_BEHAVIORAL.md`), salary negotiation script (INR ≥30 LPA floor; USD 15–20/hr freelance), "why leave / why this role", conflict, failure, mentoring, stakeholder pushback.
- Practice: 4 mock behavioral rounds (with a friend or recorded).
- Deliverable: finalized stories with real numbers + one-page "pitch".

### Week 12 (Jan 18) — Mocks, polish, applications sprint
- Full-loop mocks: coding (45) + system design (45) + AI deep-dive (45) + behavioral (30).
- Update CV (correct dates to LinkedIn timeline), LinkedIn headline, GitHub pins, portfolio site.
- Deliverable: 2 full-loop mocks, final CV, ≥ 20 targeted applications logged.

## After Week 12
Maintenance: 5 h/week — one new design, one coding set, one blog post. Keep applying; review the tracker weekly for pipeline conversion (apply → screen → loop → offer) and adjust tiers (move down one level only if Tier 1 conversion stays low after ~6 weeks, per your strategy).

## Real-world topics checklist (tick in tracker)
RAG · evals · agents/MCP · LangGraph · Kafka/outbox · pricing models · LLM security · cost/routing · serving · K8s/Terraform basics · observability · system design · DSA · behavioral · negotiation.
