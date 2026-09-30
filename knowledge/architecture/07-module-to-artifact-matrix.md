# Matriz módulo → fase → componente → artefacto → evidencia

| Módulo | Fase | Componente | Artefacto principal | Evidencia |
|---|---|---|---|---|
| M1 | Fundamento | Workflow IA | Política de trabajo, contexto y prompting | 5 archivos M1 |
| M3 | Harness | Operación copiloto | EPE, gates, permisos, hooks/subagents | Archivos de M3 |
| M4 | Planificación | Producto | Backlog, AC, DoD, non-goals, roadmap | Archivos de M4 |
| M2 | Spec | Contratos | Specs/OpenSpec y escenarios | Archivos de M2 |
| M6 | Seguridad | Trust boundaries | Threat model/políticas | Archivos M6 + fuentes externas registradas |
| M5 | Arquitectura | Conocimiento/contratos | ADR, C4, OpenAPI, runbooks | Archivos M5 |
| M7 | Calidad | Dominio/políticas | Unit tests y estrategia | Archivos M7 |
| M8 | Datos | Persistencia/retrieval | Schema, migrations, índices | Archivos M8 |
| M9 | Backend | API/dominio/tools | Backend y adapters | Archivos M9 + referencia M12 |
| M10 | Frontend | Operador | UI/control center | Archivos M10 + referencia M12 |
| M11 | QA | Límites sistémicos | Integration/E2E/BDD | Archivos M11 |
| M13 | Entrega | Infra/CI/CD | Pipelines, IaC y release controls | Archivos M13 |
| M12 | Reference-only | Arquitectura SRE | Ningún artefacto de etapa | Documento SRE completo |

## Cadena

`problema → objetivos → backlog/AC → spec → seguridad → arquitectura → tests → datos → backend/UI → integración/E2E → entrega/operación`

Los artefactos conservan trazabilidad upstream y pueden reabrirse cuando downstream aporte nueva evidencia.
