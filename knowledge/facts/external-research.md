# External Research Register

## Cutoff rule

The executable prompt's cutoff is **2026-09-11**. External claims used as current-state decisions are limited to evidence published/updated on or before that date unless the source is undated and used only for stable architectural capabilities.

## Key verified sources

| ID | Source | Date | What it supports | Cutoff use |
|---|---|---|---|---|
| R01 | OpenAI — Harness engineering | 2026-02-11 | Repository knowledge, agent-first engineering, architecture legibility | valid |
| R02 | OpenAI Cookbook — SRE incident-response agent | 2026-09-10 | Direct SRE-agent architecture corroboration | valid |
| R09 | OWASP GenAI Top 10 | 2025 | Prompt injection, excessive agency, vector/embedding risks, unbounded consumption | valid |
| R10 | NIST SSDF 1.2 IPD | 2025-12-17 | Secure software development integrated into SDLC | valid |
| R14 | Kubernetes Python client 36.0.3 | 2026-07-13 | Official Python client release and support | valid |
| R15 | LangChain 1.4.0 | 2026-09-03 | Cutoff-compatible LangChain release | valid |
| R16 | LangGraph 1.2.11 | 2026-08-11 | Cutoff-compatible LangGraph release | valid |
| R17 | Streamlit 1.63.0 | 2026-09-01 | Cutoff-compatible Streamlit release | valid |
| R07 | AWS Reliability guidance | classic/current docs | Recovery automation controls | stable capability |
| R08 | Google SRE postmortem culture | classic/current docs | Postmortem practice | stable capability |
| R05 | Prometheus Alertmanager | current docs | Dedup/group/routing | stable capability |
| R06 | OpenTelemetry | current docs | metrics/logs/traces | stable capability |
| R11 | GitHub deployment API | current docs | Deployment status/event correlation | stable capability |
| R12 | Slack Socket Mode | current docs | Event/interactive app connectivity | stable capability |
| R13 | Grafana Loki HTTP API | current docs | Log query/tail | stable capability |
| R19 | pgvector | current project docs | Vector search inside Postgres | stable capability |

## Temporal exclusions

The following observations were seen after the cutoff and were therefore excluded from cutoff-current claims:

- LangChain 1.4.1/1.4.2 releases after Sep 11.
- LangGraph 1.2.12 on Sep 21.
- Streamlit 1.64.0 on Sep 15.
- GitHub Spec Kit page showing last update Sep 14.

These are documented as temporal-control evidence only.

## Verificación de Chat 2

El 2026-09-29 se volvió a inspeccionar un subconjunto focalizado de fuentes oficiales manteniendo el corte 2026-09-11 para afirmaciones de estado al corte:

- OpenAI Agents cookbook: `https://developers.openai.com/cookbook/topic/agents` — el índice lista `Build an SRE agent for incident response` con fecha 2026-09-10.
- AGENTS.md: `https://agents.md/` — formato Markdown abierto para contexto dirigido a agentes de coding.
- OpenTelemetry Python: `https://opentelemetry.io/docs/languages/python/` — soporte de Python y estado de señales.
- Prometheus Alertmanager: `https://next.prometheus.io/docs/alerting/latest/alertmanager/` — deduplicación, agrupación, routing, silenciamiento e inhibición.
- Grafana Loki HTTP API: `https://grafana.com/docs/loki/latest/reference/loki-http-api/` — consultas `query`, `query_range` y `tail`, con diferencia entre tail y recuperación histórica completa.
- LangChain: `https://docs.langchain.com/` — documentación actual usada solo como contexto estable de capacidad, no como afirmación de versión al corte.

Ninguna observación posterior al 2026-09-11 se convirtió en una afirmación de “latest” al corte.

## Adenda temporal y de procedencia de Chat 2

Las fuentes anteriores fueron consultadas como verificación puntual actual. No constituyen nuevas decisiones del proyecto.
