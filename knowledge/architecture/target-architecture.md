# Target Architecture

## Logical architecture

```text
Alertmanager / PagerDuty / incident.io
              ↓
           FastAPI
     (webhooks + API + auth)
              ↓
     Incident Orchestrator / Worker
              ↓
         LangGraph Agent
              ↓
      ┌───────┼────────┐
      ↓       ↓        ↓
Prometheus  Loki    GitHub/AWS/K8s
      └───────┼────────┘
              ↓
        Evidence Model
              ↓
      Hypothesis / Verify
              ↓
     Remediation Proposal
              ↓
        Human Approval
              ↓
     Isolated Secure Executor
              ↓
       Recovery Verification
              ↓
          Resolution
              ↓
         Postmortem
              ↓
    PostgreSQL + Retrieval
```

## Data/persistence

PostgreSQL is authoritative for incident and audit records. pgvector is the first evaluated semantic retrieval option when runbooks and incident history require semantic search. Redis is optional for queue/cache/coordination.

## Operator surfaces

- Slack: operational interaction and approval.
- Streamlit: initial control center.
- React/Next.js: future enterprise UI if needed.

## Security boundary

Read-only tools are separated from mutation tools. Consequential mutation requires explicit authorization and a separate executor with scoped credentials.

## Observability

Instrument both the target system and the agent itself. Capture service telemetry plus agent latency, tool latency, failures, retries, tokens/cost, approvals, and recovery outcomes.

## Runtime memory

- short-term/current execution state: LangGraph checkpoints;
- long-term incident history/runbooks: PostgreSQL + retrieval;
- external Chat 1 memory: separate `memory-repo`.

## Deployment maturity

Local Docker first → CI test environment → containerized staging → optional Kubernetes/AWS production-like environment → IaC + deployment gates.
