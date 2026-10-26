# System Design Bank

Framework (use every time, 45 min): 1) clarify requirements & scale (5) → 2) APIs/data model (8) → 3) high-level design (10) → 4) deep-dive 1–2 components (12) → 5) failure modes, security, cost, observability (7) → 6) trade-offs & evolution (3).

## A. Your-domain designs (strongest stories)
1. **EV charging platform** — sessions, OCPP gateway, billing, roaming; spikes, offline chargers, idempotent billing.
2. **Real-time dynamic pricing engine** — features, model serving, fallbacks, price-change audit, A/B.
3. **Energy marketplace** — offers, matching, settlement/ledger, fairness, regulatory audit.
4. **Multi-tenant CIAM** — SSO, tokens, tenant isolation, migration from legacy.
5. **Event backbone migration (Redis → Kafka)** — zero-downtime cutover, dual-write, ordering, replay, rollback.
6. **Vendor/OEM integration hub** — webhooks, retries, signature verification, schema versioning.

## B. AI-system designs
7. **Enterprise RAG assistant (10k users)** — ACL-aware retrieval, freshness, citations, evals, cost.
8. **Multi-agent SDLC assistant** — PR review, test generation; HITL, sandboxing, cost control.
9. **Log-investigation agent** (Datadog-style) — scale, tool safety, remediation approvals.
10. **LLM gateway** — routing, caching, quotas, PII redaction, fallbacks, observability.
11. **Document-processing pipeline** (invoices/contracts) — OCR, extraction, validation, review queue.
12. **Customer-support copilot** — handoff, escalation, feedback loop, evals.
13. **Recommendation/ranking system** — features, offline/online eval, cold start.
14. **AI agent platform ("agent factory")** — registry, versioning, tool permissions, tenancy, audit — your CV's "Agent Factory" topic.

## C. Classic designs (warm-up)
URL shortener · rate limiter · notification service · chat system · news feed · job scheduler · distributed cache · file storage · API gateway · search autocomplete.

## For each design, prepare
- Back-of-envelope numbers (QPS, storage, tokens/day, cost).
- Data model and API sketch.
- 3 failure scenarios and mitigations.
- Security & privacy concerns.
- What you'd measure (SLIs/SLOs, quality metrics for AI).
- Build-vs-buy and vendor risk.

## Weekly use
Week 1: 4 classic · Week 5: 1–6 · Week 8: 7, 10 · Week 9: 3 timed mocks (pick 7/14/1) · Weeks 11–12: re-run weakest 3.
