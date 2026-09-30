# Dependency Matrix

| From | To | Dependency reason | Criticality |
|---|---|---|---|
| M1 | M3 | operating model precedes harness operations | High |
| M3 | M4 | planning uses working agentic method | Medium |
| M4 | M2 | story/AC → formal spec | High |
| M2 | M6 | security constraints can be scoped to real capabilities | High |
| M6 | M5 | security choices become architecture/ADR inputs | High |
| M5 | M8 | architecture/docs inform data boundaries | High |
| M5 | M9 | API/architecture contracts inform backend | High |
| M7 | M9 | test discipline constrains implementation loop | High |
| M8 | M9 | data model precedes durable backend use cases | High |
| M9 | M10 | UI consumes backend/API behavior | Medium |
| M9+M10 | M11 | system QA spans components | High |
| M11 | M13 | delivery confidence depends on system verification | High |

## Transversal edges

- M4 ↔ M2
- M5 ↔ M6
- M5 ↔ M7
- M7 ↔ M9
- M8 ↔ M9
- M11 ↔ M13
- M12 → all modules as reference information only

## Chat 2 M1 dependencies

The seven M1 work units have their own functional dependencies; they do not rewrite this module-level matrix. The detailed unit dependency graph is documented in `11-m1-construction-plan.md` and checked by `12-m1-quality-gates.md`.

## Adenda de regresión de Chat 2

Las dependencias internas de las siete unidades de M1 se documentan en el plan específico; el grafo de módulos sigue siendo el de Chat 1 y no se sobrecarga con fronteras artificiales.
