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

## Chat 2 scope note

M1 is preparatory methodology for all roadmap stages. Chat 2 does not implement any roadmap stage and does not advance the project into execution.

## Adenda de regresión de Chat 2

El plan de M1 prepara el modo de trabajo para abordar los huecos ya documentados, pero no afirma cerrar FastAPI, LangGraph, SRE operativo, executor seguro, Slack, evaluación u observabilidad.
