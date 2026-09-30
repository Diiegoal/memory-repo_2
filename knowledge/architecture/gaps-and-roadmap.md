# Gaps and Roadmap

## High-priority gaps

1. Python/FastAPI-specific implementation guidance.
2. LangGraph incident state/tool design.
3. SRE-specific SLO/SLI/on-call operating model.
4. Secure executor/sandbox design.
5. Agent evaluation dataset and metrics.
6. Slack approval integration.
7. Observability integration labs.

## Roadmap

### R0 — Read-only investigation

FastAPI + LangGraph + PostgreSQL + one metrics/log source.

### R1 — Persistent incident management

Incident state, evidence, hypotheses, audit log, history.

### R2 — Retrieval and operational knowledge

Runbooks + postmortems + history retrieval; evaluate pgvector.

### R3 — Operational conversation

Slack events, threads and approval interaction.

### R4 — Controlled remediation

Separate executor, least-privilege credentials, allow-list, approval gate.

### R5 — Recovery verification

Metrics/logs/state checks after action; explicit success/failure outcome.

### R6 — Production-like operations

Kubernetes/AWS integration, OpenTelemetry, Alertmanager, Docker, CI/CD/IaC.

### R7 — Evaluation and continuous improvement

Incident dataset, regression runs, trace review, tool-use evaluation, cost/latency monitoring, postmortem-derived runbook updates.

---

# CHAT 2 — CONTENIDO NUEVO

## M1 boundary

M1 establishes the AI-engineering foundation only. Exact SRE operating model, executor isolation details, incident corpus, production channels, full observability and deployment remain future work/open questions.

# CHAT 2 — CUMULATIVE UPDATE

M1 does not close target-specific gaps such as exact SRE operating model, incident corpus, secure executor isolation, Slack approval mechanics, runtime agent memory policy, full observability, deployment and LangGraph incident orchestration. Those remain future project work or open questions.

