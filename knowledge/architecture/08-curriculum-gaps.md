# Huecos del currículo frente al producto objetivo

## Clasificación

**CUBIERTO**, **CUBIERTO INDIRECTAMENTE**, **PARCIALMENTE CUBIERTO** y **NO CUBIERTO** se refieren al nivel de evidencia curricular encontrado; no son juicios de calidad del material.

## Matriz

| Tema | Cobertura | Evidencia | Trabajo específico pendiente |
|---|---|---|---|
| Python/FastAPI productivo | Parcial | M9 + referencia M12 | Adaptación específica del target |
| LangGraph para incident orchestration | Indirecta | M12 + documentación externa | Diseño/implementación del proyecto |
| SLO/SLI/error budgets/on-call | Parcial | Referencia SRE | Track operacional específico |
| Prometheus/Loki/OpenTelemetry | Parcial | M12 + docs oficiales | Labs de integración |
| Slack y aprobación | Parcial | M12 + API Slack | Implementación segura |
| Executor aislado | Parcial | M6 + M12 | Aislamiento/credenciales/allow-list |
| Evals por dataset/trace | Parcial | M11 + M12 | Dataset y harness de regresión |
| Memoria runtime | Parcial | M1 + M12 | Diseño de state/store/retención |
| Modelo de dominio de incidentes | No cubierto explícitamente | M4/M2 genéricos | Trabajo específico |
| Corpus sintético de incidentes | No cubierto explícitamente | QA genérico | Dataset versionado |
| Gobierno de runbooks/on-call | Parcial | M5 + M12 | Ownership/lifecycle/revisión |
| Secrets/RBAC/autorización | Parcial | M6 + M12 | Implementación operacional |
| Rate limiting/cache/workers/colas | Parcial | M12 | Decisión según carga |
| Backups/disaster recovery | Indirecta | M13 + recovery de referencia | Diseño operacional |
| Coste/latencia del agente | Parcial | M1/M11 + M12 | Métricas y umbrales |

## Huecos principales

1. Implementación específica Python/FastAPI/LangGraph.
2. Dataset y evaluación de incidentes.
3. Executor seguro, credenciales y allow-list.
4. Modelo SRE operativo con SLO/SLI/on-call.
5. Labs de Slack, observabilidad, Kubernetes y AWS.
