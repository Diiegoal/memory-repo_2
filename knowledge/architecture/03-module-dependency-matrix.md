# Matriz de dependencias de módulos

## Dependencias críticas

| Origen | Destino | Tipo | Fuerza | Razón |
|---|---|---|---|---|
| M1 | M3 | Método/harness | Alta | El harness necesita modelo de tool/context/prompt. |
| M3 | M4 | Workflow | Media | La planificación asistida necesita ejecución gobernada. |
| M4 | M2 | Producto → spec | Alta | El backlog/AC alimenta contratos. |
| M2 | M6 | Seguridad | Alta | Los controles deben referirse a capacidades concretas. |
| M2 | M5 | Contrato → arquitectura | Alta | Las specs fijan comportamiento y límites. |
| M6 | M5 | Seguridad → arquitectura | Alta | Los controles se convierten en límites arquitectónicos. |
| M5 | M8 | Arquitectura → datos | Alta | El dominio y persistencia dependen de los límites arquitectónicos. |
| M5 | M9 | Arquitectura → backend | Alta | API/componentes definen límites del backend. |
| M7 | M9 | Tests → implementación | Alta | El loop de calidad gobierna cambios de código. |
| M8 | M9 | Datos → backend | Alta | El backend necesita persistencia definida. |
| M9 | M10 | Backend → UI | Media | La UI consume contratos/estado del backend. |
| M9 + M10 | M11 | Integración → QA | Alta | E2E requiere componentes integrados. |
| M11 | M13 | QA → release | Alta | La entrega necesita evidencia sistémica. |

## Loops

M4 ↔ M2, M5 ↔ M6, M5 ↔ M7, M7 ↔ M9, M8 ↔ M9 y M11 ↔ M13 representan refinamiento continuo. M12 alimenta contexto de dominio a todos, pero no constituye una dependencia constructiva.

## Orden resultante

`M1 → M3 → M4 → M2 → M6 → M5 → M7 → M8 → M9 → M10 → M11 → M13`
