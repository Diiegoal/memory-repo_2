# Trazabilidad de Chat 2

## Cadena

`M1 → archivo → sección/tema → capacidad → M1-PXX → artefacto futuro → evidencia futura → validación`

## Fuentes de continuidad

| Elemento | Fuente | Clasificación |
|---|---|---|
| Orden de módulos | `chats/chat-001/HANDOFF.md`, `DECISIONS.md`, `DEC-0001.md` | Decisión heredada |
| M12 fuera del orden | `DEC-0002.md` | Decisión heredada |
| Seguridad/documentación como gates + loops | `DEC-0003.md` | Decisión heredada |
| Read-only-first | `DEC-0004.md` | Decisión heredada |
| PostgreSQL + evaluación pgvector | `DEC-0005.md` | Decisión heredada |
| Streamlit opcional | `DEC-0006.md` | Decisión heredada |
| Auditoría completa M1 | `FACT-0001-chat-002-m1-source-audit.md` | Hecho de ejecución |
| Estado target | `FACT-0002-chat-002-target-repository-state.md` | Hecho de ejecución |
| Ejecución Chat 2 | `FACT-0003-chat-002-execution-record.md` | Hecho de ejecución |
| Proyecto SRE | `13-project-reference-summary.md` + fuente M12 | Referencia |

## Evidencia vs planificación

Lo observado directamente conserva etiqueta de hecho; lo heredado de Chat 1 conserva carácter de decisión histórica; lo que aún no existe en el target se marca como futuro. No se creó implementación en Chat 2.

## Fuentes externas

Las referencias y fechas se conservan en `knowledge/facts/external-research.md` y `knowledge/references/reference-index.md`. El corte heredado de afirmaciones externas sensibles al tiempo es `2026-09-11`.
