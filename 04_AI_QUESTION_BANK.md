# AI / LLM / Agents Question Bank (with answer outlines)

Practice by answering aloud in ≤2 min, then check outline. Add your own project evidence to each.

## RAG
1. **Why does RAG fail?** Bad chunking, embedding mismatch, missing metadata filters, stale index, retrieval returns right doc but model ignores it, no citations. Fix: hybrid search, rerank, query rewriting, eval per stage.
2. **Chunking strategy?** Semantic/structure-aware (headings, tables), overlap, size trade-off (recall vs context cost); evaluate empirically.
3. **How do you evaluate RAG?** Retrieval (recall@k, MRR) separate from generation (faithfulness, answer relevance); golden set + LLM-judge calibrated with human labels; CI gate.
4. **Vector DB choice?** Scale, filtering, hybrid support, ops burden; pgvector until proven otherwise.
5. **Access control in RAG?** Filter at retrieval with ACL metadata; never rely on prompt.

## Agents
6. **When NOT to use an agent?** Deterministic workflows, latency/cost sensitive, high-risk actions; prefer workflows + LLM steps.
7. **Single vs multi-agent?** Multi adds coordination cost; use for separable roles, parallelism, specialist tools/prompts.
8. **How do you make agents reliable?** Structured outputs, tool schemas, retries/bounds, step limits, state checkpoints, evals on trajectories, HITL on risky tools.
9. **CrewAI vs LangGraph vs custom?** Abstraction vs control; explicit state, observability, determinism; your experience: CrewAI for speed, graph/state machines for production control.
10. **MCP — what and why?** Standard protocol for tools/resources; reduces integration glue; still needs auth, permissions, treat responses as untrusted.
11. **Human-in-the-loop design?** Risk-tiered approvals, immutable proposals, audit; approval bound to exact payload.

## Evals & quality
12. **How do you know an LLM feature works?** Task-specific golden sets, regression runs, online metrics, human review sampling, drift monitoring.
13. **LLM-as-judge pitfalls?** Bias, verbosity preference, position bias; calibrate vs humans, use rubric and pairwise.
14. **Hallucination mitigation?** Grounding, citations, abstain behavior, verification step, constrained decoding/schemas.

## Security
15. **Prompt injection defenses?** Treat external text as data, least-privilege tools, output validation, separate verifier, no secrets in context, allow-lists, test corpus.
16. **PII/compliance?** Redaction, data residency, retention, vendor DPAs, audit logs, on-prem/private endpoints where required.

## Serving & cost
17. **Reduce LLM cost/latency?** Prompt caching, smaller model routing, batching, streaming, shorter context, async, distillation.
18. **Fine-tune vs RAG vs prompt?** Prompt first, RAG for knowledge, fine-tune for style/format/latency; LoRA overview.
19. **Inference serving?** Batching, KV cache, quantization, vLLM; managed API vs self-host trade-offs.

## ML fundamentals (for AI/ML Engineer screens)
20. Precision/recall/F1/AUC and metric choice under imbalance.
21. Overfitting, regularization, cross-validation, leakage.
22. Gradient boosting vs deep learning for tabular data; LightGBM tuning basics.
23. Drift types and monitoring; retraining triggers.
24. Pricing model: features, elasticity, constraints, fairness, rollback safety.

## Architecture
25. **Design governance for enterprise AI** — model registry, approval flows, audit, evals, cost centers.
26. **Build vs buy for AI platform** — differentiation, lock-in, security, talent, TCO.
27. **How would you introduce AI into a legacy PHP/Laravel system?** Strangler pattern, API facade, event bridge, pilot with measurable KPI.
28. **Explain your Kafka migration** — dual write, ordering, consumer groups, replay, rollback, measuring the 10x throughput gain.
