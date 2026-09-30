# Roadmap profesional de ejecución

## Principio

El orden de módulos es el backbone de construcción. La entrega real debe usar slices verticales y loops de planificación, seguridad, documentación, testing, QA y evaluación; terminar un módulo no elimina esas capacidades.

## R0 — Fundación de IA

**Módulos:** M1 + M3.  
**Resultado:** política de trabajo, harness, contexto, prompting, permisos y gates.  
**Límite:** solo preparación; no producto ejecutado.

## R1 — Descubrimiento

**Módulo:** M4.  
**Resultado:** MVP, actores, backlog, AC, DoD, non-goals y roadmap.  
**Criterio:** capacidades prioritarias delimitadas para especificación.

## R2 — Especificación

**Módulo:** M2.  
**Resultado:** specs/deltas y escenarios de aceptación para las primeras capacidades.  
**Criterio:** cada slice implementable tiene comportamiento verificable.

## R3 — Seguridad

**Módulo:** M6.  
**Resultado:** threat model, clasificación de datos, límites de herramientas, autorización y mínimo privilegio.  
**Criterio:** restricciones críticas incorporables a arquitectura, tests, datos y backend.

## R4 — Arquitectura y conocimiento

**Módulo:** M5.  
**Resultado:** ADRs, C4, OpenAPI, runbooks y documentación para agentes.  
**Criterio:** arquitectura comprensible y recuperable.

## R5 — Calidad local

**Módulo:** M7.  
**Resultado:** estrategia unit testing, fixtures/fakes y pruebas de políticas/dominio.  
**Criterio:** comportamiento crítico con evidencia local.

## R6 — Datos

**Módulo:** M8.  
**Resultado:** schema, migrations, índices y evaluación de pgvector.  
**Criterio:** persistencia de la primera slice definida y migrable.

## R7 — Backend/agente

**Módulo:** M9.  
**Resultado:** FastAPI, dominio, adapters y runtime de agente según specs.  
**Seguridad:** primera slice read-only; ninguna mutación irrestricta.

## R8 — Operador

**Módulo:** M10.  
**Resultado:** estado, evidencia, hipótesis, propuestas, aprobación y recuperación visibles.  
**UI:** Streamlit como opción inicial; React/Next.js como evolución.

## R9 — Integración/evaluación

**Módulo:** M11.  
**Resultado:** integration/E2E/BDD y evaluación de tool-use, grounding, estado, aprobación, recovery, latencia, coste y regresión.  
**Criterio:** acceptance evidence suficiente para release.

## R10 — Entrega/operación

**Módulo:** M13.  
**Resultado:** Docker, CI/CD, IaC, DevSecOps, despliegue, rollback y runbooks operativos según alcance.  
**Criterio:** entrega reproducible con gates.

## Loops transversales

| Capacidad | Inicio principal | Reaparición |
|---|---|---|
| Planificación | M4 | M2–M13 |
| Seguridad | M6 | M5, M7, M8, M9, M10, M11, M13 |
| Documentación | M5 | Cada cambio material |
| Testing | M7 | M8–M13 |
| QA | M11 | Release/operación |
| IA-assisted development | M1/M3 | Todo el ciclo |
| Arquitectura | M5 | Datos/backend/UI/QA/entrega |
| Contexto/memoria | M1/M3 | Agente, docs, evaluación |
| Observabilidad | Referencia M12 | Integración/operación |

## Evolución

`R0/R1 → MVP read-only → RAG/history → Slack/approval → executor controlado → recovery verification → Kubernetes/AWS → CI/CD/IaC/evaluación continua`
