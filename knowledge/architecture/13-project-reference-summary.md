# SRE/DevOps Project Reference Summary

## Source

`Diiegoal/CursoIA/Módulo_12_Lab_1_Crea_tu_propio_chatbot_de_documentación_técnica_con_Langchain_y_Streamlit/6. Agente SRE DevOps Respuesta Incidentes.md`

The file was read completely during Chat 2. M12 is reference-only.

## Purpose and operating model

The reference describes an AI-assisted SRE incident-response system that receives an alert, creates or updates an incident, gathers operational evidence, forms and checks hypotheses, proposes remediation, obtains human approval for consequential actions, executes through a separated mechanism, verifies recovery and produces postmortem knowledge.

## High-level flow

```text
Alert/Webhook
    ↓
Incident Manager
    ↓
Deduplication / Correlation
    ↓
AI Agent (LangChain/LangGraph)
    ↓
Prometheus / Loki / GitHub / AWS / Kubernetes / history / runbooks
    ↓
Evidence
    ↓
Diagnosis / Hypotheses / Verification
    ↓
Remediation Proposal
    ↓
Human Approval
    ↓
Secure Executor
    ↓
Recovery Verification
    ↓
Resolution
    ↓
Postmortem / Knowledge
```

## Conversational and reflective behavior

The agent is not merely a retrieval chatbot. The reference expects the agent to choose tools, interpret results, create hypotheses, seek further evidence, and revisit the investigation after new evidence appears. Reflection is represented as an operational hypothesis/verification loop rather than hidden chain-of-thought disclosure.

## Core components

### Incident intake and management

Inputs may include Alertmanager, PagerDuty or incident.io. The incident layer normalizes alerts, authenticates sources, computes fingerprints and deduplicates repeated alerts into one incident.

### Agent layer

LangChain supplies agent/tool abstractions; LangGraph manages stateful and long-running flows, persistence/checkpoints and human interrupts.

### Evidence tools

- Prometheus for metric queries.
- Loki for LogQL log queries.
- GitHub for commits, pull requests and deployment/change evidence.
- AWS APIs for operational cloud evidence.
- Kubernetes Python client for runtime state and diagnostics.

### Knowledge and retrieval

Runbooks, postmortems, architecture documentation and historical incidents can be retrieved to answer questions such as whether the service has experienced a similar failure before.

### Persistence

PostgreSQL is proposed for incident/audit/domain records. Redis is a possible queue/cache/coordination layer. Product runtime state and long-term historical knowledge are conceptually separated.

### Human-in-the-loop

The reference rejects a direct `LLM → unrestricted production command` pattern. Consequential actions pass through policy/approval and a separate executor with narrower credentials.

### Recovery verification

A remediation is not considered successful merely because an action completed. The agent should verify metrics/logs/runtime state and decide whether recovery succeeded. Failure can reopen investigation.

### Observability

Prometheus/Grafana/Loki/OpenTelemetry are reference observability pieces. The agent itself also needs instrumentation for model/tool latency, failures, retries, iterations, tokens/cost proxies, approval waits and recovery outcomes.

### Operator surfaces

Slack is the operational conversation/approval surface in the reference pattern. Streamlit is a useful control-center option. React/Next.js is a later UI evolution rather than a requirement for the agent runtime.

### Delivery

The reference includes Docker, workers/asynchronous processing, CI/CD and possible Kubernetes/AWS operations. These are staged capabilities, not M1 implementation work.

## Safety levels described by the reference

1. Observation: metrics/logs/status/change queries.
2. Diagnosis: descriptive inspection and comparison.
3. Reversible actions: restart/scale/mute when explicitly authorized.
4. Higher-impact actions: rollback/configuration/infrastructure changes.

The inherited Chat 1 decision is to keep the initial agent read-only and require authorization, human approval and a separated executor before mutation.

## Technology inventory

The reference explicitly names Python, `uv`, FastAPI, Uvicorn, Pydantic, LangChain, LangGraph, PostgreSQL, Redis, RAG, vector retrieval, Streamlit, Slack/Slack API, Prometheus, Alertmanager, Loki, Grafana, OpenTelemetry/OTLP, Tempo, GitHub API, AWS APIs and services, Kubernetes and its Python client, Docker, workers, runbooks, postmortems, LangSmith/evaluation, CI/CD, IaC, PagerDuty/incident.io and possible ArgoCD/React/Next.js evolution.

## Classification for this project

| Element | Role |
|---|---|
| Python/FastAPI/LangChain/LangGraph/PostgreSQL | core target architecture |
| pgvector | evaluated retrieval consolidation option, not unconditional requirement |
| Redis | optional queue/cache/coordination layer |
| Streamlit | optional initial control center |
| Slack | operational conversation/approval surface |
| Prometheus/Alertmanager/Loki/OpenTelemetry | operational evidence/observability path |
| GitHub | deployment/change correlation |
| Kubernetes/AWS/Docker | staged operational/production-like environment capabilities |
| Secure executor | prerequisite before real mutation |
| RAG/runbooks/postmortems/history | operational knowledge capability |
| LangSmith/evals | agent quality/traceability capability |
| React/Next.js | future UI evolution |
| Bedrock Agents Classic / AgentCore | reference alternatives; not a mandatory decision |

## M12 boundary

This summary is context for applying M1. It is not permission to execute any M12-derived implementation during Chat 2 and does not change the construction order.
