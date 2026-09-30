# Auditoría de módulos — vista orientada a construcción

## Alcance

La auditoría directa de `Diiegoal/CursoIA` en `main` identificó 13 directorios de módulos y 68 archivos Markdown. El orden de construcción incluye 12 módulos; M12 queda como reference-only.

## Matriz módulo → contenido → aplicación

| Módulo | Contenido observado | Papel de construcción | Dependencia principal |
|---|---|---|---|
| M1 | Herramienta, contexto, prompt | Fundamento de ingeniería con IA | Primero |
| M3 | Harness, EPE, tools, contexto, subagents, hooks, MCP | Operación del copiloto | M1 |
| M4 | Planning, backlog, AC, DoD, scope | Descubrimiento/planificación | M1/M3 |
| M2 | SDD/OpenSpec | Especificación | M4 |
| M6 | Seguridad, privacidad, regulación, interacción | Gate de seguridad | M2 |
| M5 | ADR, C4, API/docs-as-code, documentación para LLM | Arquitectura/conocimiento | M2/M6 |
| M7 | TDD, unit testing, AI test generation, mutation | Calidad unitaria | M5/M6; interactúa con M8/M9 |
| M8 | PostgreSQL, SQL, índices, migrations, pgvector | Datos/persistencia | M5/M7 |
| M9 | Backend, DDD, refactor, ticket-to-PR | Backend | M5/M7/M8 |
| M10 | Frontend, UX, calidad, performance, accessibility | Superficie del operador | M9/contratos |
| M11 | Integration, E2E, BDD, QA | Calidad sistémica | M9/M10 |
| M12 | Investigación SRE, RAG, LangChain/Streamlit | Reference-only | Fuera del orden |
| M13 | PR review, IaC, CI/CD, DevSecOps | Entrega/operación | M11 |

## Lectura profesional

La auditoría distingue contenido de módulo y momento de aplicación. Seguridad, documentación, testing y desarrollo asistido por IA son loops, no actividades de una sola ejecución. M9 requiere adaptación a Python/FastAPI porque el currículo no constituye por sí mismo toda la implementación específica del target.

## Resultado

El corpus completo respalda el uso de M1 como fundamento práctico y mantiene M12 fuera del orden de construcción.
