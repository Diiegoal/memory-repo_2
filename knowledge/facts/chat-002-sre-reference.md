# Chat 002 — SRE Reference Summary

## Scope and boundary

The source file `Diiegoal/CursoIA/Módulo_12_Lab_1_Crea_tu_propio_chatbot_de_documentación_técnica_con_Langchain_y_Streamlit/6. Agente SRE DevOps Respuesta Incidentes.md` was read completely. It is the target-product reference, not a construction module.

## Product and operational flow

The source describes a conversational/reflexive SRE/DevOps incident-response agent that receives alerts, creates or correlates incidents, gathers evidence, reasons over hypotheses, proposes remediation, requests human approval for consequential actions, executes through a separated controlled executor when authorized, verifies recovery, resolves the incident, and produces a postmortem and durable knowledge.

```text
Alert/Webhook
→ deduplication/correlation
→ incident session/state
→ evidence gathering
→ hypothesis / verification
→ diagnosis
→ remediation proposal
→ human approval when consequential
→ separated executor
→ recovery verification
→ resolution
→ postmortem / incident knowledge
```

## Components and responsibilities named by the source

- **FastAPI**: webhook/API boundary, authentication and HTTP service concerns.
- **LangChain/LangGraph**: agent engineering; tool use, stateful/long-running workflow, checkpoints and human-in-the-loop interruptions.
- **Prometheus / Alertmanager**: metrics and alert intake, grouping/dedup/routing/silencing/inhibition.
- **Loki / Grafana**: logs and visualization; LogQL and HTTP query APIs.
- **GitHub**: commits, pull requests, changed files, deployments/statuses and branch context.
- **AWS**: CloudWatch, ECS, EKS, EC2, Lambda, RDS, ElastiCache, ALB and CloudTrail as possible evidence sources.
- **Kubernetes**: pods, deployments, ReplicaSets, Services, Events, Nodes, containers, resource use, conditions and restart counts.
- **PostgreSQL / pgvector**: durable incident/audit data and evaluated semantic retrieval in the adopted architecture.
- **Redis**: queue/coordination/cache/locks/rate limits/temporary state; not the sole incident store.
- **Runbooks / RAG / incident history**: operational knowledge.
- **Slack**: operational conversation and approval surface.
- **Streamlit**: optional initial control center; separate React/Next.js is a possible future UI.
- **Workers**: asynchronous execution for long investigations.
- **OpenTelemetry / Tempo / Grafana**: observability of system traces, metrics and logs.
- **LangSmith / evaluation**: agent traces, datasets/evaluation and quality monitoring.
- **Docker / Kubernetes / IaC / CI-CD / ArgoCD**: delivery and operations.
- **Secure executor**: isolated mutation path with scoped credentials.

## Evidence and diagnosis model

The source explicitly uses contextual evidence: request rate, error rate, latency, CPU, memory, restarts, queue depth, database connections, logs, cluster state, recent deployments, GitHub changes and historical incidents. The agent is expected to construct and verify hypotheses rather than state an unsupported root cause.

## Safety model

Read-only evidence tools are separated from mutation tools. Higher-impact actions should require authorization and a separate executor. The initial product architecture is therefore compatible with a read-only-first starting point.

## Persistence model

The source proposes durable incident records, events, evidence, hypotheses, actions, approvals, postmortems, runbooks, embeddings, users and audit logs, with current execution state distinct from historical knowledge.

## Observability and evaluation

The source includes service observability plus agent observability such as tool latency/failures, retries, timeouts, tokens/cost, approvals and recovery outcomes. It calls for synthetic incident datasets and evaluation of tool choice, evidence use, hallucination, diagnosis, approval behavior and closure.

## Postmortem

The source's postmortem data includes incident identity/severity/service, start/detection times, customer impact, timeline, evidence, root cause, contributing factors, mitigation, resolution, what worked/failed and follow-up/preventive actions.

## Technology inventory

The source explicitly names Python 3.14+, `uv`, FastAPI, LangChain, LangGraph, Streamlit, Slack/Slack API, RAG, vector retrieval/vector database options, PostgreSQL, pgvector, Redis, Pydantic, SQLAlchemy, Alembic, Uvicorn, HTTPX, Kubernetes Python Client, Prometheus, Alertmanager, Grafana, Loki, OpenTelemetry, OTLP, Tempo, GitHub API, AWS APIs, CloudWatch, ECS, EKS, EC2, Lambda, RDS, ElastiCache, ALB, CloudTrail, Docker, Kubernetes, PagerDuty/incident.io, ArgoCD, workers, runbooks, incident history, human-in-the-loop, separated executor, postmortems, LangSmith/evaluation, CI/CD, IaC, optional React/Next.js, and AWS Bedrock Agents Classic/AgentCore as reference alternatives where discussed.

## M1 boundary

M1 may prepare the AI-assisted engineering method, persistent context, context-operations discipline, prompting and coding workflow. Full implementation of the above SRE capabilities belongs to later project work/modules and is not executed in Chat 2.
