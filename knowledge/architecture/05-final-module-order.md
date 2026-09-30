# Orden profesional final de módulos

## Orden heredado y verificado

`M1 → M3 → M4 → M2 → M6 → M5 → M7 → M8 → M9 → M10 → M11 → M13`

M12 permanece fuera del orden y es únicamente referencia.

## Justificación por etapa

### M1 — Fundamento
Contiene herramienta, contexto y prompt, incluida la distinción completion/agentic y patrones de ejecución asistida. Define cómo se trabajará con IA antes de usarla para construir.

### M3 — Harness
Contiene EPE, tools, contexto, subagents, hooks, MCP, permisos y session hygiene. Hace reproducible la ejecución asistida.

### M4 — Planificación
Convierte el producto en capacidades, backlog, criterios de aceptación, DoD, non-goals y roadmap. Su salida alimenta la especificación.

### M2 — Especificación
Formaliza capacidades mediante SDD/OpenSpec, contratos y escenarios verificables. Da a seguridad y arquitectura un objeto concreto sobre el que trabajar.

### M6 — Seguridad y privacidad
Fija trust boundaries, clasificación de datos, seguridad de interacción, mínimo privilegio, controles de herramientas y autorización antes de congelar arquitectura.

### M5 — Arquitectura y documentación
Convierte specs y controles en ADRs, C4, API/docs-as-code, runbooks y conocimiento vivo. La documentación actúa como memoria técnica consumible por humanos y agentes.

### M7 — Calidad unitaria
Establece TDD, AAA/GWT, fakes/mocks de boundaries, edge cases, coverage como señal, tests asistidos por IA y mutation testing. Prepara evidencia local de corrección.

### M8 — Datos
Desarrolla PostgreSQL, índices, migrations y evaluación de pgvector. Permite modelar incidentes, evidencia, auditoría e historial con límites ya definidos.

### M9 — Backend
Materializa dominio, API, persistencia y adapters/tools. El target requiere adaptación Python/FastAPI y LangGraph que no se presume cubierta íntegramente por el módulo.

### M10 — Frontend
Desarrolla superficie de operador, UX, accesibilidad, calidad y performance. Streamlit es opcional; React/Next.js queda como evolución.

### M11 — QA de sistema
Integra unitarias, integration, E2E y BDD, además de evaluación del comportamiento del agente. Necesita componentes reales para validar límites sistémicos.

### M13 — Entrega y operación
Integra code review, CI/CD, IaC, DevSecOps, despliegue y operación. Su posición principal es tardía, pero varias prácticas aparecen como loops antes.

## Por qué M12 no tiene puesto

M12 define el producto SRE, stack, flujo de incidentes, tools, RAG, persistencia, aprobación, executor, recuperación, postmortem y evaluación de referencia. Su función es orientar el diseño; colocarlo como etapa alteraría el contrato de exclusión heredado.

## Refutación realizada

Se revisaron especialmente las fronteras M2↔M6, M6↔M5, M7↔M8, M8↔M9 y M11↔M13, además de la exclusión de M12. No apareció evidencia que obligara a modificar el orden heredado.
