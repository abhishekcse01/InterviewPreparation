# Portfolio Projects (public, real-world)

Rules: public GitHub, synthetic/public data only (no employer code or data), README with architecture diagram, tests, `docker compose up` run, and a "Trade-offs & what I'd do next" section. Each project maps to a topic you'll be asked about.

## Project 1 — Production RAG with Evaluation (Weeks 2–3, 8)
**Real-world scenario:** support/knowledge assistant over product docs (e.g. open EV-charging / solar standards and public docs).
- Ingestion: PDF/HTML → chunking strategies compared; metadata.
- Retrieval: hybrid BM25 + vectors (pgvector or Chroma), reranker, query rewriting, citations.
- Evals: 50-Q golden set, retrieval recall@k, faithfulness (LLM-judge + spot human check), CI regression gate.
- Ops: tracing, cost and latency dashboard, caching.
- **Proves:** RAG depth, evals, observability. **Interview line:** "I improved recall@5 from X to Y by hybrid search + reranking; evals run in CI."

## Project 2 — Multi-Agent Incident Investigator (Weeks 4, 7)
**Scenario:** analyze application logs (synthetic Datadog-style), form hypotheses, propose remediation, require human approval before any action.
- Agents: triage, log analyst, hypothesis/RCA, remediation planner, reviewer.
- LangGraph (or plain tool-calling) with explicit state; MCP tool server for log search.
- Safety: tool allow-list, HITL approval gate, injection tests, audit log.
- **Proves:** multi-agent design, guardrails, your Datadog story (told generically).

## Project 3 — Event-Driven Energy Marketplace (Week 5)
**Scenario:** EV charging sessions and energy offers flowing through Kafka/Redpanda.
- Services: session ingest, pricing consumer, ledger, notification; outbox pattern; idempotent consumers; DLQ; replay.
- Load test with k6; show consumer lag, failure injection, exactly-once-effect.
- **Proves:** Kafka/event-driven architecture (your 10x throughput story, reproduced publicly).

## Project 4 — Dynamic Pricing Model + Serving (Week 6)
**Scenario:** time-of-use pricing for charging/energy (public datasets).
- LightGBM model, feature pipeline, model card, FastAPI serving, drift monitor, A/B toggle.
- **Proves:** ML fundamentals, serving, MLOps basics.

## Project 5 — Career/Freelance Agent Platform (Week 10, flagship; this repo `jobagent`)
Public subset: orchestration, verification agent, approval state machine with tests, security docs.
- **Proves:** architect-level thinking: agents + governance + human approval + security + tests.

## Cross-cutting checklist per project
- [ ] README: problem, diagram, decisions, trade-offs, results
- [ ] Tests + CI badge
- [ ] 2–5 min demo video/GIF
- [ ] Blog/LinkedIn post (1 per project)
- [ ] Pinned on GitHub; linked from portfolio and CV
