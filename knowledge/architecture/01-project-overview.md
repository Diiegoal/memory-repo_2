# Descripción del proyecto — Agente SRE/DevOps para respuesta a incidentes

## Propósito

Este documento registra el contexto de proyecto derivado por Chat 2 para aplicar M1 al producto objetivo. La evidencia RAW de Chat 1 permanece en `chats/chat-001/transcript.md`.

## Proyecto objetivo

`DiiegoA/Agente_SRE_DevOps_para_respuesta_a_incidentes`

El repositorio objetivo fue consultado en modo de solo lectura durante Chat 2. El endpoint de contenidos de GitHub informó que el repositorio estaba vacío en el momento de la observación. Por ello no se afirma la existencia previa de archivos fuente, configuración de frameworks, infraestructura o implementación observable.

## Resumen profesional del producto

El producto objetivo es un agente SRE/DevOps conversacional y reflexivo para respuesta a incidentes. Su ciclo operacional de referencia es:

`incident intake → triage → recopilación de evidencia → formulación de hipótesis → verificación de hipótesis → propuesta de remediación → aprobación humana cuando las consecuencias lo exijan → ejecución controlada → verificación de recuperación → resolución → postmortem → conocimiento operativo durable`

“Reflexivo” se entiende operacionalmente: el agente debe mantener un ciclo de evidencia, hipótesis y verificación. Esto no implica exponer el razonamiento privado del modelo.

## Arquitectura de referencia

M12 es reference-only. Describe entrada por alertas/webhooks, deduplicación/correlación, agente con LangChain/LangGraph, herramientas de evidencia operacional, historial y runbooks, aprobación humana, executor seguro separado, recuperación/verificación y postmortems.

## Inventario del stack y postura

| Capa | Tecnología | Papel en la fuente | Tratamiento para el proyecto |
|---|---|---|---|
| Runtime | Python | Runtime de aplicación/agente | Adoptar |
| Tooling | `uv` | Entorno/gestión Python | Adoptar al implementar |
| Agente | LangChain | Herramientas y abstracciones | Adoptar |
| Orquestación | LangGraph | Estado, checkpoints e interrupciones | Adoptar; implementación posterior |
| Backend | FastAPI | Webhooks, API y frontera de servicio | Adoptar |
| Servidor | Uvicorn | ASGI para FastAPI | Adoptar |
| Datos | Pydantic | Validación y contratos tipados | Adoptar |
| Persistencia | PostgreSQL | Dominio, incidentes y auditoría | Aceptado por DEC-0005 |
| Vector | pgvector | Retrieval dentro de PostgreSQL | Evaluar antes de BD vectorial separada |
| Coordinación | Redis | Cola/caché/locks/coordinación | Opcional; OQ-0003 abierta |
| UI | Streamlit | Control center | Opcional; DEC-0006 |
| Canal | Slack / Slack API | Conversación y aprobación | Opción operacional |
| Métricas | Prometheus | Métricas/evidencia | Integración operacional |
| Alertas | Alertmanager | Grouping/dedup/routing/silence/inhibition | Integración de alertas |
| Logs | Loki | Consulta de logs | Evidencia operacional |
| Visualización | Grafana | Vista humana de observabilidad | Complementaria |
| Telemetría | OpenTelemetry / OTLP | Logs, métricas y trazas | Adopción incremental |
| Trazabilidad/evaluación | LangSmith | Trazas/evaluación/feedback | Etapa de evaluación |
| Cambios | GitHub API | PR/commit/deployment evidence | Solo lectura inicialmente |
| Cloud | AWS APIs | Evidencia y posibles destinos | Etapa posterior |
| Runtime | Kubernetes Python Client | Pods/deployments/events | Etapa posterior |
| Servicios AWS | CloudWatch, ECS, EKS, EC2, Lambda, RDS, ElastiCache, ALB, CloudTrail | Servicios citados | Integración posterior |
| Contenedores | Docker | Ejecución reproducible | Adopción progresiva |
| Entrega | CI/CD | Build/test/security/release | Principalmente M13 |
| Infraestructura | IaC | Infraestructura reproducible | Principalmente M13 |
| Incidentes | PagerDuty / incident.io | Sistemas posibles | Opcional |
| Delivery | ArgoCD | Reconciliación/despliegue posible | Futuro |
| Mutación | Executor seguro aislado | Frontera con credenciales acotadas | Requisito antes de mutaciones |
| Conocimiento | RAG / recuperación vectorial | Runbooks/postmortems/historial | Futuro; evaluar escala |
| Frontend | React / Next.js | Evolución de UI | Posterior |
| Alternativas | Bedrock Agents Classic / AgentCore | Referencias tecnológicas | No decidido |

## Agentic SDLC

El orden heredado y verificado es:

`M1 → M3 → M4 → M2 → M6 → M5 → M7 → M8 → M9 → M10 → M11 → M13`

M1 establece la forma de trabajo con IA; M3 el harness; M4 planificación; M2 especificación; M6 seguridad/privacidad; M5 arquitectura/documentación; M7 calidad unitaria; M8 datos; M9 backend; M10 frontend; M11 integración/QA; M13 entrega/operación. M12 no pertenece al ciclo y solo aporta referencia del dominio y del stack.

## Aplicación de M1

M1 establece la cadena operacional:

`caracterizar tarea → decidir modo → seleccionar/evaluar herramienta → conservar contexto persistente → gestionar contexto operativo → construir prompt → elegir patrón de coding → ejecutar/revisar/validar`

No se justifica en Chat 2 la implementación de FastAPI, LangGraph, RAG, bases de datos, UI, observabilidad ni acciones de producción.

## Seguridad y memoria

La frontera heredada es:

`herramientas read-only → política → aprobación humana cuando corresponda → executor aislado → verificación de recuperación`

Además, se mantienen separados: `memory-repo` de Chat 1; estado runtime del producto; y conocimiento operacional duradero del producto.

## Límite de ejecución actual

No se ejecutó el Paso 1 del proyecto ni se modificó el repositorio objetivo. Los artefactos de Chat 2 existen únicamente en la copia de staging independiente.
