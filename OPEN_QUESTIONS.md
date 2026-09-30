# Open Questions

## OQ-0001 — Exact SRE operating model
Status: open

Which SLO/SLI/error-budget model, on-call structure and escalation policy should the target adopt? The current evidence supports the importance of SRE alerting/postmortems but does not specify the project’s exact operating model.

## OQ-0002 — Exact LLM provider/model
Status: open

Which model/provider should be used for the agent, and what portability/fallback policy is required? No single provider is made mandatory by Chat 1.

## OQ-0003 — Runtime queue/worker technology
Status: open

Whether Redis is required for the initial asynchronous execution path or whether a simpler worker/persistence approach is sufficient should be validated by workload characteristics.

## OQ-0004 — Vector retrieval scale
Status: open

Validate whether pgvector is sufficient for runbooks/incident history or whether scale/retrieval requirements justify a dedicated vector engine.

## OQ-0005 — Executor isolation
Status: open

Choose the exact sandbox/isolation mechanism, credential boundary and action allow-list before any mutation capability is enabled.

## OQ-0006 — UI choice beyond MVP
Status: open

Determine whether Streamlit remains sufficient or a React/Next.js operator console is required for multi-user/RBAC/enterprise workflows.

## OQ-0007 — Agent evaluation rubric
Status: open

Define numeric/threshold metrics for tool-use correctness, evidence grounding, action safety, recovery verification, latency, cost and regression.

## OQ-0008 — Incident corpus
Status: open

Create and version a synthetic incident dataset representative of the target operating environment.

## Límite de aclaración de Chat 2

Chat 2 no resolvió ni transformó `OQ-0001` a `OQ-0008` en decisiones del proyecto. Permanecen abiertas porque M1 aporta metodología de ingeniería asistida por IA, pero no aporta por sí solo los contratos operativos SRE, elecciones de runtime, aislamiento del executor, escala de recuperación o corpus de evaluación necesarios para cerrarlas.
