# Plan de Módulo 1 — Chat 2

## Status
- Estado: PLANIFICADO.
- El producto objetivo no fue implementado en Chat 2.
- El Paso 1 del proyecto no fue ejecutado.
- Este archivo es el registro canónico de los pasos de M1.

## Determinación dinámica de la cantidad de pasos

El conjunto final no se fijó por una cantidad prefabricada. Primero se leyó M1 completo, se inventariaron capacidades, subcapacidades, prácticas, resultados, evidencias y validaciones; después se propusieron unidades candidatas y se aplicaron pruebas de profundidad, independencia, integración, anti-compresión y anti-fragmentación. La descomposición estable resultó en siete unidades: mantiene separadas las capacidades profesionalmente independientes de selección de herramienta, contexto, prompt, workflow e integración/validación, mientras evita convertir cada subtítulo o concepto en un paso artificial.

## Secuencia final

| Paso | Título | Objetivo resumido | Dependencia | Salida principal |
|---|---|---|---|---|
| `M1-P01` | Caracterizar el trabajo de ingeniería y fijar el modelo mental de los tres pilares | Definir el marco común para usar herramienta, contexto y prompt como un sistema integrado en el proyecto SRE, sin ejecutar ninguna actividad de construcción del producto. | INDEPENDIENTE | FUTURO: `M1_OPERATING_MODEL.md`. |
| `M1-P02` | Clasificar tareas y seleccionar/evaluar herramienta y modo de interacción | Convertir el Pilar 1 en un mecanismo operativo para decidir cuándo una tarea requiere completion o agentic, qué categoría de herramienta encaja y cómo reevaluarla con evidencia. | M1-P01 | FUTURO: `M1_TOOL_MATRIX.md`. |
| `M1-P03` | Diseñar el sistema de contexto mínimo suficiente y su higiene | Definir cómo el futuro repositorio del proyecto expondrá contexto relevante, reglas, estado y memoria de trabajo sin saturar al agente ni mezclar información no pertinente. | M1-P01, M1-P02 | FUTURO: `M1_CONTEXT_KIT.md`; `AGENTS.md` corto como mapa; `CLAUDE.md` solamente si la herramienta futura lo requiere. |
| `M1-P04` | Diseñar contratos de prompt y biblioteca de patrones reutilizables | Definir prompts claros y verificables para futuras tareas del proyecto, con contexto, objetivo, éxito, restricciones, recursos y formato. | M1-P01, M1-P03 | FUTURO: `M1_PROMPT_LIBRARY.md`. |
| `M1-P05` | Definir patrones integrados de planificar, ejecutar, probar, revisar y refactorizar | Transformar la integración de los tres pilares en ciclos de trabajo repetibles para tareas futuras del proyecto, manteniendo la ejecución real fuera de Chat 2. | M1-P01, M1-P02, M1-P03, M1-P04 | FUTURO: `M1_WORKFLOW_RULES.md`. |
| `M1-P06` | Consolidar el modelo operativo AI-assisted específico del proyecto SRE | Unificar herramienta, contexto y prompt en un operating model que alimente las etapas posteriores del Agentic SDLC sin implementar el agente, backend o infraestructura. | M1-P02, M1-P03, M1-P04, M1-P05 | FUTURO: `M1_OPERATING_MODEL.md` consolidado y enlaces a los artefactos M1 específicos. |
| `M1-P07` | Validar, documentar, controlar contaminación y establecer iteración | Establecer el gate final de M1 para comprobar coherencia, procedencia, higiene contextual, reutilización e iteración antes de pasar a M3. | M1-P01, M1-P02, M1-P03, M1-P04, M1-P05, M1-P06 | FUTURO: `M1_VALIDATION_REGISTER.md`. |

## Matrices obligatorias

### Cobertura práctica M1
| Archivo M1 | Tema/sección | Capacidad | Paso | Artefacto | Evidencia | Validación | Estado |
|---|---|---|---|---|---|---|---|
| `1. El modelo mental de los 3 pilares.md` | modelo mental e integración | modelo integrado | P01, P06, P07 | `M1_OPERATING_MODEL.md` / registro | fuente M1 + decisiones Chat1 | revisión integrada | PLANIFICADO |
| `2. Pilar 1 — La Herramienta.md` | categorías, modo, selección, benchmarks, anti-patterns | clasificación/selección | P02 | `M1_TOOL_MATRIX.md` | fuente M1 | escenarios PASS/FAIL | PLANIFICADO |
| `3. Pilar 2 — El Contexto.md` | context engineering | selección, aislamiento y mantenimiento de contexto | P03 | `M1_CONTEXT_KIT.md` | fuente M1 | recuperación mínima y contaminación | PLANIFICADO |
| `4. Pilar 3 — El Prompt + Integración.md` | prompting + workflows | contratos de prompt y ciclos de trabajo | P04, P05, P06 | `M1_PROMPT_LIBRARY.md`, `M1_WORKFLOW_RULES.md` | fuente M1 | revisión de contratos/workflows | PLANIFICADO |
| `5. Recursos adicionales.md` | recursos y fuentes | procedencia/revalidación | P07 | `M1_VALIDATION_REGISTER.md` | URLs y fechas | auditoría temporal | PLANIFICADO |

### Dependencias
| Paso | Depende de | Habilita | Tipo de dependencia | Riesgo si se invierte | Evidencia |
|---|---|---|---|---|---|
| M1-P01 | INDEPENDIENTE | P02/P03/P04 | fundamento | diseño fragmentado sin modelo común | M1 files 1-4 |
| M1-P02 | P01 | P05/P06 | selección | herramienta/modo mal elegidos | M1 file 2 |
| M1-P03 | P01/P02 | P04/P05/P06 | contexto | exceso de contexto o contaminación | M1 file 3 |
| M1-P04 | P01/P03 | P05/P06 | contrato | prompts ambiguos | M1 file 4 |
| M1-P05 | P01-P04 | P06/P07 | workflow | ciclos ad hoc | M1 file 4 |
| M1-P06 | P02-P05 | P07/M3 | integración | pilares desconectados | M1 files 1-4 |
| M1-P07 | P01-P06 | siguiente módulo | gate | drift/contaminación no detectados | M1 files 1-5 |

### Concepto → actividad
| Concepto M1 | Qué significa | Cómo se aplica | Artefacto | Evidencia | Validación |
|---|---|---|---|---|---|
| Tres pilares | herramienta, contexto y prompt se co-determinan | integrar decisiones antes de actuar | `M1_OPERATING_MODEL.md` | M1 files 1-4 | prueba P01/P06 |
| Selección de herramienta | elegir modo/categoría con criterios | clasificar escenarios | `M1_TOOL_MATRIX.md` | M1 file 2 | T01-P02 |
| Context engineering | seleccionar/aislar/compactar contexto | mapa de contexto mínimo | `M1_CONTEXT_KIT.md` | M1 file 3 | T01-P03 |
| Prompt contract | objetivo/éxito/límites/recursos/formato | plantillas reutilizables | `M1_PROMPT_LIBRARY.md` | M1 file 4 | T01-P04 |
| Workflow loops | plan/execution/test/review/refactor | ciclos futuros de ingeniería | `M1_WORKFLOW_RULES.md` | M1 file 4 | T01-P05 |
| Validación/iteración | usar feedback para corregir | gate de M1 | `M1_VALIDATION_REGISTER.md` | M1 file 5 + R21 | T01-P07 |

### Paso → resultado
| Paso | Entrada | Actividad | Salida | Evidencia | Criterio de aceptación | Siguiente paso |
|---|---|---|---|---|---|---|
| M1-P01 | M1 + contexto SRE + restricciones heredadas | Definir una representación de tarea AI-assisted: tarea, modo/herramienta, contexto, prompt, revisión y resultado. | FUTURO: `M1_OPERATING_MODEL.md`. | M1 file 1 y su integración explícita con files 2-4. | objetivo + cobertura + trazabilidad + estado PLANIFICADO | M1-P02, M1-P03, M1-P04 |
| M1-P02 | M1 + contexto SRE + restricciones heredadas | Clasificar escenarios del proyecto y registrar categoría, modo, criterios de selección, evidencia y condición de reevaluación. | FUTURO: `M1_TOOL_MATRIX.md`. | M1 file 2 contiene las categorías, árbol de decisión, criterios, snapshot de modelos, benchmarks y anti-patterns. | objetivo + cobertura + trazabilidad + estado PLANIFICADO | M1-P05, M1-P06 |
| M1-P03 | M1 + contexto SRE + restricciones heredadas | Clasificar contexto estable vs situacional, definir entradas mínimas y reglas de recuperación/aislamiento, y diseñar un mapa de navegación hacia fuentes profundas. | FUTURO: `M1_CONTEXT_KIT.md`; `AGENTS.md` corto como mapa; `CLAUDE.md` solamente si la herramienta futura lo requiere. | M1 file 3. | objetivo + cobertura + trazabilidad + estado PLANIFICADO | M1-P04, M1-P05, M1-P06 |
| M1-P04 | M1 + contexto SRE + restricciones heredadas | Diseñar plantillas para análisis, planificación futura, revisión y documentación, cada una con entradas, objetivo, criterios de aceptación, límites y formato. | FUTURO: `M1_PROMPT_LIBRARY.md`. | M1 file 4. | objetivo + cobertura + trazabilidad + estado PLANIFICADO | M1-P05, M1-P06 |
| M1-P05 | M1 + contexto SRE + restricciones heredadas | Definir para cada workflow cuándo explorar, planificar, ejecutar, probar, revisar y cerrar, y qué salida produce cada etapa. | FUTURO: `M1_WORKFLOW_RULES.md`. | M1 file 4 y sus casos de aplicación. | objetivo + cobertura + trazabilidad + estado PLANIFICADO | M1-P06, M1-P07 |
| M1-P06 | M1 + contexto SRE + restricciones heredadas | Integrar P02-P05 en una secuencia única: entrada de tarea → selección de modo/herramienta → contexto → prompt → ejecución futura → revisión/test → cierre. | FUTURO: `M1_OPERATING_MODEL.md` consolidado y enlaces a los artefactos M1 específicos. | M1 files 1-4 y decisiones Chat 1 relevantes. | objetivo + cobertura + trazabilidad + estado PLANIFICADO | M1-P07, M3 |
| M1-P07 | M1 + contexto SRE + restricciones heredadas | Definir un registro de validación y una rutina de regresión para detectar prompts ambiguos, contexto excesivo, tool/mode mismatch, fuentes desactualizadas y reglas contradictorias. | FUTURO: `M1_VALIDATION_REGISTER.md`. | M1 file 5 y su conjunto de recursos; además de OpenAI harness engineering como corroboración externa. | objetivo + cobertura + trazabilidad + estado PLANIFICADO | Siguiente módulo (M3) sin ejecución |

## Hard boundaries
- M12 es exclusivamente referencia; no forma parte del plan de construcción.
- M2–M13 no se implementan durante M1.
- Ningún repositorio externo es modificado.
- Los comandos, archivos y código del producto son FUTUROS.
- No se crea código del Paso 1.
- No se crean ZIP incrementales por paso durante Chat 2; se define su función para ejecución futura.

## Pruebas de calidad del plan
- Cobertura completa: cinco archivos de M1 trazados a pasos.
- Profundidad: cada capacidad conserva variantes/criterios/prácticas que M1 diferencia.
- No contaminación: no se ejecuta trabajo de M2–M13; M12 solo contextualiza.
- Originalidad: Example2 se usa como referencia de documentación y estructura de proyecto, no como plantilla/código.
- Estructura: cada paso usa los 26 campos en orden.
- Tests: cada paso tiene una prueba concreta con entrada, resultado esperado y PASS/FAIL.

## Regla de cierre
El conjunto se considera congelado únicamente cuando los siete pasos pasan las auditorías estructural y semántica, el plan puede reconstruirse desde este archivo y el estado de todos los pasos permanece PLANIFICADO.

## Paso 01 — Caracterizar el trabajo de ingeniería y fijar el modelo mental de los tres pilares

### 1. Identification

- ID del paso: `M1-P01`
- Fase: Fase A — Construcción cognitiva del plan
- Subfase: Fundamentación
- Estado: PLANIFICADO
- Tipo de paso: Unidad profesional coherente de planificación de M1.

### 2. Objective

- Objetivo exacto del paso: Definir el marco común para usar herramienta, contexto y prompt como un sistema integrado en el proyecto SRE, sin ejecutar ninguna actividad de construcción del producto.

### 3. Direct relation to M1

- Archivo(s) de M1: `1. El modelo mental de los 3 pilares.md`: modelo mental de tres pilares e integración. `2. Pilar 1 — La Herramienta.md`, `3. Pilar 2 — El Contexto.md`, `4. Pilar 3 — El Prompt + Integración.md`: relación práctica entre pilares.
- Sección(es)/tema(s): `1. El modelo mental de los 3 pilares.md`: modelo mental de tres pilares e integración. `2. Pilar 1 — La Herramienta.md`, `3. Pilar 2 — El Contexto.md`, `4. Pilar 3 — El Prompt + Integración.md`: relación práctica entre pilares.
- Concepto(s) de M1: Herramienta + contexto + prompt como sistema integrado; el modelo no es el único cuello de botella; la calidad depende de los tres pilares.
- Relación directa: El contenido se convierte en una actividad futura verificable sobre el proyecto real, sin ejecutar el producto durante Chat 2.

### 4. Prerequisites

- Conocimientos previos: lectura completa de M1 y comprensión del objetivo SRE como contexto.
- Condiciones previas: bootstrap Chat 2, STATE/DECISIONS/OPEN_QUESTIONS/HANDOFF recuperados.
- Evidencia o artefactos necesarios: fuentes M1, decisiones Chat1 y referencia SRE.

### 5. Dependencies

- Depende de: INDEPENDIENTE
- Habilita: M1-P02, M1-P03, M1-P04
- Tipo de dependencia: secuencial funcional dentro de M1.
- Riesgo si se altera el orden: se perdería una entrada de diseño o se introduciría retrabajo/ambigüedad; para P01 no existe dependencia previa de M1.

### 6. Preparation

- Preparación necesaria: Definir una representación de tarea AI-assisted: tarea, modo/herramienta, contexto, prompt, revisión y resultado.
- Entorno: copia de trabajo independiente; ningún repositorio externo se modifica.
- Información que debe estar disponible: M1 completo, decisiones heredadas, límites M12 reference-only y estado real del nuevo proyecto.

### 7. Files

- Archivos que se leerán: Los cinco archivos de M1 y los artefactos de continuidad de Chat 1.
- Archivos que se crearán en la ejecución futura: FUTURO: `M1_OPERATING_MODEL.md`.
- Archivos que se modificarían en la ejecución futura: FUTURO y sujeto a revisión; ninguno se modifica durante Chat 2.
- Ubicación exacta de cada archivo: artefactos futuros en la raíz documental del nuevo proyecto; no existen físicamente durante Chat 2.

### 8. Directory structure

```text
<raíz del proyecto SRE — ejecución futura>
├── M1_OPERATING_MODEL.md
├── M1_TOOL_MATRIX.md
├── M1_CONTEXT_KIT.md
├── M1_PROMPT_LIBRARY.md
├── M1_WORKFLOW_RULES.md
└── M1_VALIDATION_REGISTER.md
```
Los nombres muestran el conjunto de posibles artefactos M1; cada paso crea solo el que su campo Files identifica y únicamente en ejecución futura.

### 9. Required concepts

- Concepto: Herramienta + contexto + prompt como sistema integrado; el modelo no es el único cuello de botella; la calidad depende de los tres pilares.
- Explicación necesaria: desarrollar qué es, cuándo se usa, cómo se aplica, criterio de elección, entrada, salida, evidencia y validación cuando M1 los diferencia.
- Nivel requerido para ejecutar el paso: aplicación operativa y verificable; no implementación del producto.

### 10. Commands

```text
NO APLICA — Chat 2 es planificación; no se ejecuta ningún comando del proyecto nuevo.
```
- Ubicación desde la que se ejecuta cada comando: NO APLICA durante Chat 2.
- Resultado esperado: no existe ejecución del proyecto.
- Verificación: revisar que los comandos futuros estén marcados FUTURO/PLANIFICADO.

### 11. Code

```text
NO APLICA — no se crea código del producto durante Chat 2.
```
- Propósito: conservar la frontera entre planificación y ejecución.
- Partes relevantes: ningún código ejecutado.
- Personalización requerida: se resolverá en la ejecución futura con el repositorio real.

### 12. Action

- Acción concreta que se realizará: Definir una representación de tarea AI-assisted: tarea, modo/herramienta, contexto, prompt, revisión y resultado.
- Orden de ejecución: aplicar el contenido M1 indicado → producir artefacto futuro → validar → registrar evidencia.
- Entrada utilizada: contenido real de M1 + contexto SRE + decisiones heredadas.
- Salida producida: FUTURO: `M1_OPERATING_MODEL.md`.

### 13. Reason

- Por qué se realiza esta acción: convierte conocimiento de M1 en una unidad profesional reutilizable.
- Qué problema resuelve: Pérdida de un pilar o mezcla con responsabilidades de módulos posteriores.
- Por qué corresponde a M1: deriva del contenido práctico de M1 y no de implementación posterior.

### 14. Expected result

- Resultado esperado: FUTURO: `M1_OPERATING_MODEL.md`. queda definido como salida futura y su contenido está especificado por el paso.
- Estado esperado: PLANIFICADO; no existe físicamente durante Chat 2.
- Evidencia esperada: M1 file 1 y su integración explícita con files 2-4.
- Memoria incremental del paso: ZIP de memoria acumulativa FUTURO, generado solo cuando el paso sea ejecutado; durante Chat 2 se define su estructura y función, pero no se crea.

### 15. Evidence

- Evidencia que demuestra el resultado: M1 file 1 y su integración explícita con files 2-4.
- Fuente de la evidencia: fuente M1 concreta, más decisiones Chat1 cuando limitan el proyecto.
- Cómo se conservará: en el artefacto futuro, en el plan y en la trazabilidad de memoria; no reemplaza RAW.

### 16. Validation

- Qué se debe verificar: Revisar tres escenarios del proyecto y comprobar que cada uno puede expresarse mediante los tres pilares sin adelantar módulos posteriores.
- Cómo se verifica: revisión contra M1, matriz de cobertura, dependencias, criterios y estado PLANIFICADO.
- Resultado esperado de la validación: PASS cuando la unidad esté específica, completa y correctamente acotada.

### 17. Acceptance criteria

- Criterio 1: La unidad tiene un único objetivo profesional principal.
- Criterio 2: Todo contenido práctico de M1 que le corresponde conserva sus subcapacidades relevantes.
- Criterio 3: No se presenta ninguna acción futura como ejecutada durante Chat 2.

### 18. Tests

- ID de prueba: `T01-M1-P01`
- Capacidad/subcapacidad cubierta: indicada en la descripción de la prueba.
- Prueba: T01-M1-P01 — Capacidad: integración de los tres pilares. Prueba: mapear tres escenarios de ingeniería sin ejecutar el proyecto. Entrada: escenarios de análisis, documentación y revisión. Resultado: cada escenario contiene herramienta/modo, contexto, prompt y revisión. PASS si los tres pilares están presentes y no se introduce trabajo de M3–M13.
- Entrada: plan M1, contenido de M1 y escenario correspondiente.
- Resultado esperado: evidencia observable de cobertura, coherencia y trazabilidad.
- Condición de aprobación: PASS únicamente cuando la prueba produzca el resultado indicado y no dependa de una ejecución del proyecto durante Chat 2.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors

- Error plausible: Pérdida de un pilar o mezcla con responsabilidades de módulos posteriores.
- Cuándo podría aparecer: al redactar, revisar o ejecutar futuramente la unidad.
- Síntoma: una subcapacidad queda comprimida, no verificable o mezclada con trabajo posterior.

### 20. Detection

- Cómo detectar el error: confrontar el paso con la fuente M1, su matriz de cobertura y sus criterios de aceptación.
- Evidencia del error: fila o concepto sin actividad/artefacto/validación o una afirmación de ejecución actual.
- Señal observable: FAIL en la auditoría estructural o semántica.

### 21. Meaning

- Qué significa el error o resultado: una frontera de trabajo o una afirmación de procedencia es incorrecta.
- Qué parte del proceso afecta: calidad del paso y continuidad al siguiente.

### 22. Diagnosis

- Causa probable: compresión artificial, dependencia oculta, ambigüedad de prompt/contexto o mezcla de módulos.
- Evidencia que confirma o descarta la causa: fuente M1 → campo del paso → matriz → decisiones heredadas.
- Orden de diagnóstico: fuente → cobertura → profundidad → independencia → trazabilidad → estado.

### 23. Correction

- Corrección: ajustar contenido, separar si la independencia funcional lo exige o reclasificar como futuro/no aplica con justificación.
- Acción concreta: Reformular la unidad o mover el contenido ajeno a M1 a su módulo posterior.
- Verificación posterior: repetir cobertura, profundidad, independencia, integración, trazabilidad y tests.
- Riesgos de la corrección: incrementar artificialmente pasos o adelantar módulos posteriores.

### 24. Close checklist

- [ ] Objetivo cumplido.
- [ ] Dependencias satisfechas.
- [ ] Archivos comprobados.
- [ ] Validación completada.
- [ ] Criterios de aceptación cumplidos.
- [ ] Evidencia conservada.
- [ ] Trazabilidad completada.
- [ ] Estado actualizado.

### 25. Traceability

- M1 → archivo → sección/tema → concepto: `1. El modelo mental de los 3 pilares.md`: modelo mental de tres pilares e integración. `2. Pilar 1 — La Herramienta.md`, `3. Pilar 2 — El Contexto.md`, `4. Pilar 3 — El Prompt + Integración.md`: relación práctica entre pilares. → Herramienta + contexto + prompt como sistema integrado; el modelo no es el único cuello de botella; la calidad depende de los tres pilares..
- Concepto → actividad: Definir una representación de tarea AI-assisted: tarea, modo/herramienta, contexto, prompt, revisión y resultado..
- Actividad → paso: `M1-P01`.
- Paso → artefacto: FUTURO: `M1_OPERATING_MODEL.md`..
- Paso → evidencia: documental; el resultado futuro no está ejecutado.
- Paso → validación: Revisar tres escenarios del proyecto y comprobar que cada uno puede expresarse mediante los tres pilares sin adelantar módulos posteriores..
- Paso → memoria ZIP incremental: definida como artefacto FUTURO de continuidad por ejecución.
- Paso → siguiente paso: M1-P02, M1-P03, M1-P04.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada: OpenAI, 2026-02-11, https://openai.com/index/harness-engineering/, repository knowledge como system of record y progressive disclosure; consulta dentro del cutoff de 2026-09-11.

### 26. State

- Estado inicial: PLANIFICADO.
- Estado final esperado: salida futura definida y lista para validación/ejecución posterior.
- Estado real: durante Chat 2 se diseñó el plan; no se ejecutó la unidad sobre el producto.
- Qué queda pendiente: ejecución futura y generación del artefacto real.
- Relación con el siguiente paso: M1-P02, M1-P03, M1-P04.

## Paso 02 — Clasificar tareas y seleccionar/evaluar herramienta y modo de interacción

### 1. Identification

- ID del paso: `M1-P02`
- Fase: Fase A — Construcción cognitiva del plan
- Subfase: Selección y evaluación
- Estado: PLANIFICADO
- Tipo de paso: Unidad profesional coherente de planificación de M1.

### 2. Objective

- Objetivo exacto del paso: Convertir el Pilar 1 en un mecanismo operativo para decidir cuándo una tarea requiere completion o agentic, qué categoría de herramienta encaja y cómo reevaluarla con evidencia.

### 3. Direct relation to M1

- Archivo(s) de M1: `2. Pilar 1 — La Herramienta.md`: categorías A-D; completion vs agentic; reglas de cambio; criterios de selección; benchmarks; anti-patterns.
- Sección(es)/tema(s): `2. Pilar 1 — La Herramienta.md`: categorías A-D; completion vs agentic; reglas de cambio; criterios de selección; benchmarks; anti-patterns.
- Concepto(s) de M1: Categorías A IDE, B terminal/CLI agentic, C cloud autonomous, D especializado; completion/agentic; tamaño/forma del codebase; lenguaje; privacidad/compliance; presupuesto; estilo; benchmarks SWE-Bench Verified/Pro, Aider Polyglot y Terminal-Bench 2.0; anti-patterns.
- Relación directa: El contenido se convierte en una actividad futura verificable sobre el proyecto real, sin ejecutar el producto durante Chat 2.

### 4. Prerequisites

- Conocimientos previos: lectura completa de M1 y comprensión del objetivo SRE como contexto.
- Condiciones previas: bootstrap Chat 2, STATE/DECISIONS/OPEN_QUESTIONS/HANDOFF recuperados.
- Evidencia o artefactos necesarios: fuentes M1, decisiones Chat1 y referencia SRE.

### 5. Dependencies

- Depende de: M1-P01
- Habilita: M1-P05, M1-P06
- Tipo de dependencia: secuencial funcional dentro de M1.
- Riesgo si se altera el orden: se perdería una entrada de diseño o se introduciría retrabajo/ambigüedad; para P01 no existe dependencia previa de M1.

### 6. Preparation

- Preparación necesaria: Clasificar escenarios del proyecto y registrar categoría, modo, criterios de selección, evidencia y condición de reevaluación.
- Entorno: copia de trabajo independiente; ningún repositorio externo se modifica.
- Información que debe estar disponible: M1 completo, decisiones heredadas, límites M12 reference-only y estado real del nuevo proyecto.

### 7. Files

- Archivos que se leerán: `2. Pilar 1 — La Herramienta.md`.
- Archivos que se crearán en la ejecución futura: FUTURO: `M1_TOOL_MATRIX.md`.
- Archivos que se modificarían en la ejecución futura: FUTURO y sujeto a revisión; ninguno se modifica durante Chat 2.
- Ubicación exacta de cada archivo: artefactos futuros en la raíz documental del nuevo proyecto; no existen físicamente durante Chat 2.

### 8. Directory structure

```text
<raíz del proyecto SRE — ejecución futura>
├── M1_OPERATING_MODEL.md
├── M1_TOOL_MATRIX.md
├── M1_CONTEXT_KIT.md
├── M1_PROMPT_LIBRARY.md
├── M1_WORKFLOW_RULES.md
└── M1_VALIDATION_REGISTER.md
```
Los nombres muestran el conjunto de posibles artefactos M1; cada paso crea solo el que su campo Files identifica y únicamente en ejecución futura.

### 9. Required concepts

- Concepto: Categorías A IDE, B terminal/CLI agentic, C cloud autonomous, D especializado; completion/agentic; tamaño/forma del codebase; lenguaje; privacidad/compliance; presupuesto; estilo; benchmarks SWE-Bench Verified/Pro, Aider Polyglot y Terminal-Bench 2.0; anti-patterns.
- Explicación necesaria: desarrollar qué es, cuándo se usa, cómo se aplica, criterio de elección, entrada, salida, evidencia y validación cuando M1 los diferencia.
- Nivel requerido para ejecutar el paso: aplicación operativa y verificable; no implementación del producto.

### 10. Commands

```text
NO APLICA — Chat 2 es planificación; no se ejecuta ningún comando del proyecto nuevo.
```
- Ubicación desde la que se ejecuta cada comando: NO APLICA durante Chat 2.
- Resultado esperado: no existe ejecución del proyecto.
- Verificación: revisar que los comandos futuros estén marcados FUTURO/PLANIFICADO.

### 11. Code

```text
NO APLICA — no se crea código del producto durante Chat 2.
```
- Propósito: conservar la frontera entre planificación y ejecución.
- Partes relevantes: ningún código ejecutado.
- Personalización requerida: se resolverá en la ejecución futura con el repositorio real.

### 12. Action

- Acción concreta que se realizará: Clasificar escenarios del proyecto y registrar categoría, modo, criterios de selección, evidencia y condición de reevaluación.
- Orden de ejecución: aplicar el contenido M1 indicado → producir artefacto futuro → validar → registrar evidencia.
- Entrada utilizada: contenido real de M1 + contexto SRE + decisiones heredadas.
- Salida producida: FUTURO: `M1_TOOL_MATRIX.md`.

### 13. Reason

- Por qué se realiza esta acción: convierte conocimiento de M1 en una unidad profesional reutilizable.
- Qué problema resuelve: Elegir herramienta por moda o tratar benchmarks como garantía de calidad individual.
- Por qué corresponde a M1: deriva del contenido práctico de M1 y no de implementación posterior.

### 14. Expected result

- Resultado esperado: FUTURO: `M1_TOOL_MATRIX.md`. queda definido como salida futura y su contenido está especificado por el paso.
- Estado esperado: PLANIFICADO; no existe físicamente durante Chat 2.
- Evidencia esperada: M1 file 2 contiene las categorías, árbol de decisión, criterios, snapshot de modelos, benchmarks y anti-patterns.
- Memoria incremental del paso: ZIP de memoria acumulativa FUTURO, generado solo cuando el paso sea ejecutado; durante Chat 2 se define su estructura y función, pero no se crea.

### 15. Evidence

- Evidencia que demuestra el resultado: M1 file 2 contiene las categorías, árbol de decisión, criterios, snapshot de modelos, benchmarks y anti-patterns.
- Fuente de la evidencia: fuente M1 concreta, más decisiones Chat1 cuando limitan el proyecto.
- Cómo se conservará: en el artefacto futuro, en el plan y en la trazabilidad de memoria; no reemplaza RAW.

### 16. Validation

- Qué se debe verificar: Revisar cuatro escenarios representativos y comprobar que cada selección se deriva de criterios explícitos y no de una preferencia por proveedor.
- Cómo se verifica: revisión contra M1, matriz de cobertura, dependencias, criterios y estado PLANIFICADO.
- Resultado esperado de la validación: PASS cuando la unidad esté específica, completa y correctamente acotada.

### 17. Acceptance criteria

- Criterio 1: La unidad tiene un único objetivo profesional principal.
- Criterio 2: Todo contenido práctico de M1 que le corresponde conserva sus subcapacidades relevantes.
- Criterio 3: No se presenta ninguna acción futura como ejecutada durante Chat 2.

### 18. Tests

- ID de prueba: `T01-M1-P02`
- Capacidad/subcapacidad cubierta: indicada en la descripción de la prueba.
- Prueba: T01-M1-P02 — Capacidad: clasificación y selección de herramienta/modo. Prueba: evaluar cuatro escenarios con restricciones distintas. Entrada: escenarios + tamaño de tarea + privacidad + presupuesto. Resultado: categoría y modo con justificación. PASS si cada selección es explicable y existe una condición de cambio/revisión.
- Entrada: plan M1, contenido de M1 y escenario correspondiente.
- Resultado esperado: evidencia observable de cobertura, coherencia y trazabilidad.
- Condición de aprobación: PASS únicamente cuando la prueba produzca el resultado indicado y no dependa de una ejecución del proyecto durante Chat 2.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors

- Error plausible: Elegir herramienta por moda o tratar benchmarks como garantía de calidad individual.
- Cuándo podría aparecer: al redactar, revisar o ejecutar futuramente la unidad.
- Síntoma: una subcapacidad queda comprimida, no verificable o mezclada con trabajo posterior.

### 20. Detection

- Cómo detectar el error: confrontar el paso con la fuente M1, su matriz de cobertura y sus criterios de aceptación.
- Evidencia del error: fila o concepto sin actividad/artefacto/validación o una afirmación de ejecución actual.
- Señal observable: FAIL en la auditoría estructural o semántica.

### 21. Meaning

- Qué significa el error o resultado: una frontera de trabajo o una afirmación de procedencia es incorrecta.
- Qué parte del proceso afecta: calidad del paso y continuidad al siguiente.

### 22. Diagnosis

- Causa probable: compresión artificial, dependencia oculta, ambigüedad de prompt/contexto o mezcla de módulos.
- Evidencia que confirma o descarta la causa: fuente M1 → campo del paso → matriz → decisiones heredadas.
- Orden de diagnóstico: fuente → cobertura → profundidad → independencia → trazabilidad → estado.

### 23. Correction

- Corrección: ajustar contenido, separar si la independencia funcional lo exige o reclasificar como futuro/no aplica con justificación.
- Acción concreta: Volver a los criterios del Pilar 1, explicitar incertidumbre y mantener la selección como propuesta hasta que exista evidencia de ejecución futura.
- Verificación posterior: repetir cobertura, profundidad, independencia, integración, trazabilidad y tests.
- Riesgos de la corrección: incrementar artificialmente pasos o adelantar módulos posteriores.

### 24. Close checklist

- [ ] Objetivo cumplido.
- [ ] Dependencias satisfechas.
- [ ] Archivos comprobados.
- [ ] Validación completada.
- [ ] Criterios de aceptación cumplidos.
- [ ] Evidencia conservada.
- [ ] Trazabilidad completada.
- [ ] Estado actualizado.

### 25. Traceability

- M1 → archivo → sección/tema → concepto: `2. Pilar 1 — La Herramienta.md`: categorías A-D; completion vs agentic; reglas de cambio; criterios de selección; benchmarks; anti-patterns. → Categorías A IDE, B terminal/CLI agentic, C cloud autonomous, D especializado; completion/agentic; tamaño/forma del codebase; lenguaje; privacidad/compliance; presupuesto; estilo; benchmarks SWE-Bench Verified/Pro, Aider Polyglot y Terminal-Bench 2.0; anti-patterns..
- Concepto → actividad: Clasificar escenarios del proyecto y registrar categoría, modo, criterios de selección, evidencia y condición de reevaluación..
- Actividad → paso: `M1-P02`.
- Paso → artefacto: FUTURO: `M1_TOOL_MATRIX.md`..
- Paso → evidencia: documental; el resultado futuro no está ejecutado.
- Paso → validación: Revisar cuatro escenarios representativos y comprobar que cada selección se deriva de criterios explícitos y no de una preferencia por proveedor..
- Paso → memoria ZIP incremental: definida como artefacto FUTURO de continuidad por ejecución.
- Paso → siguiente paso: M1-P05, M1-P06.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada: OpenAI, 2026-02-11, https://openai.com/index/harness-engineering/, repository knowledge como system of record y progressive disclosure; consulta dentro del cutoff de 2026-09-11.

### 26. State

- Estado inicial: PLANIFICADO.
- Estado final esperado: salida futura definida y lista para validación/ejecución posterior.
- Estado real: durante Chat 2 se diseñó el plan; no se ejecutó la unidad sobre el producto.
- Qué queda pendiente: ejecución futura y generación del artefacto real.
- Relación con el siguiente paso: M1-P05, M1-P06.

## Paso 03 — Diseñar el sistema de contexto mínimo suficiente y su higiene

### 1. Identification

- ID del paso: `M1-P03`
- Fase: Fase A — Construcción cognitiva del plan
- Subfase: Context engineering
- Estado: PLANIFICADO
- Tipo de paso: Unidad profesional coherente de planificación de M1.

### 2. Objective

- Objetivo exacto del paso: Definir cómo el futuro repositorio del proyecto expondrá contexto relevante, reglas, estado y memoria de trabajo sin saturar al agente ni mezclar información no pertinente.

### 3. Direct relation to M1

- Archivo(s) de M1: `3. Pilar 2 — El Contexto.md`: context rot; tipos de contexto; Write/Select/Compress/Isolate; AGENTS.md/CLAUDE.md; subagentes; compactación; higiene contextual.
- Sección(es)/tema(s): `3. Pilar 2 — El Contexto.md`: context rot; tipos de contexto; Write/Select/Compress/Isolate; AGENTS.md/CLAUDE.md; subagentes; compactación; higiene contextual.
- Concepto(s) de M1: Context rot; contexto de código relevante, convenciones, estado actual, intención/especificación, restricciones, memoria persistente, documentación externa e historial; Write, Select, Compress, Isolate; progressive disclosure; AGENTS/CLAUDE; subagentes.
- Relación directa: El contenido se convierte en una actividad futura verificable sobre el proyecto real, sin ejecutar el producto durante Chat 2.

### 4. Prerequisites

- Conocimientos previos: lectura completa de M1 y comprensión del objetivo SRE como contexto.
- Condiciones previas: bootstrap Chat 2, STATE/DECISIONS/OPEN_QUESTIONS/HANDOFF recuperados.
- Evidencia o artefactos necesarios: fuentes M1, decisiones Chat1 y referencia SRE.

### 5. Dependencies

- Depende de: M1-P01, M1-P02
- Habilita: M1-P04, M1-P05, M1-P06
- Tipo de dependencia: secuencial funcional dentro de M1.
- Riesgo si se altera el orden: se perdería una entrada de diseño o se introduciría retrabajo/ambigüedad; para P01 no existe dependencia previa de M1.

### 6. Preparation

- Preparación necesaria: Clasificar contexto estable vs situacional, definir entradas mínimas y reglas de recuperación/aislamiento, y diseñar un mapa de navegación hacia fuentes profundas.
- Entorno: copia de trabajo independiente; ningún repositorio externo se modifica.
- Información que debe estar disponible: M1 completo, decisiones heredadas, límites M12 reference-only y estado real del nuevo proyecto.

### 7. Files

- Archivos que se leerán: `3. Pilar 2 — El Contexto.md` y fuentes de M1 relacionadas.
- Archivos que se crearán en la ejecución futura: FUTURO: `M1_CONTEXT_KIT.md`; `AGENTS.md` corto como mapa; `CLAUDE.md` solamente si la herramienta futura lo requiere.
- Archivos que se modificarían en la ejecución futura: FUTURO y sujeto a revisión; ninguno se modifica durante Chat 2.
- Ubicación exacta de cada archivo: artefactos futuros en la raíz documental del nuevo proyecto; no existen físicamente durante Chat 2.

### 8. Directory structure

```text
<raíz del proyecto SRE — ejecución futura>
├── M1_OPERATING_MODEL.md
├── M1_TOOL_MATRIX.md
├── M1_CONTEXT_KIT.md
├── M1_PROMPT_LIBRARY.md
├── M1_WORKFLOW_RULES.md
└── M1_VALIDATION_REGISTER.md
```
Los nombres muestran el conjunto de posibles artefactos M1; cada paso crea solo el que su campo Files identifica y únicamente en ejecución futura.

### 9. Required concepts

- Concepto: Context rot; contexto de código relevante, convenciones, estado actual, intención/especificación, restricciones, memoria persistente, documentación externa e historial; Write, Select, Compress, Isolate; progressive disclosure; AGENTS/CLAUDE; subagentes.
- Explicación necesaria: desarrollar qué es, cuándo se usa, cómo se aplica, criterio de elección, entrada, salida, evidencia y validación cuando M1 los diferencia.
- Nivel requerido para ejecutar el paso: aplicación operativa y verificable; no implementación del producto.

### 10. Commands

```text
NO APLICA — Chat 2 es planificación; no se ejecuta ningún comando del proyecto nuevo.
```
- Ubicación desde la que se ejecuta cada comando: NO APLICA durante Chat 2.
- Resultado esperado: no existe ejecución del proyecto.
- Verificación: revisar que los comandos futuros estén marcados FUTURO/PLANIFICADO.

### 11. Code

```text
NO APLICA — no se crea código del producto durante Chat 2.
```
- Propósito: conservar la frontera entre planificación y ejecución.
- Partes relevantes: ningún código ejecutado.
- Personalización requerida: se resolverá en la ejecución futura con el repositorio real.

### 12. Action

- Acción concreta que se realizará: Clasificar contexto estable vs situacional, definir entradas mínimas y reglas de recuperación/aislamiento, y diseñar un mapa de navegación hacia fuentes profundas.
- Orden de ejecución: aplicar el contenido M1 indicado → producir artefacto futuro → validar → registrar evidencia.
- Entrada utilizada: contenido real de M1 + contexto SRE + decisiones heredadas.
- Salida producida: FUTURO: `M1_CONTEXT_KIT.md`; `AGENTS.md` corto como mapa; `CLAUDE.md` solamente si la herramienta futura lo requiere.

### 13. Reason

- Por qué se realiza esta acción: convierte conocimiento de M1 en una unidad profesional reutilizable.
- Qué problema resuelve: Megaprompt, contexto redundante, reglas contradictorias o mezcla de histórico irrelevante.
- Por qué corresponde a M1: deriva del contenido práctico de M1 y no de implementación posterior.

### 14. Expected result

- Resultado esperado: FUTURO: `M1_CONTEXT_KIT.md`; `AGENTS.md` corto como mapa; `CLAUDE.md` solamente si la herramienta futura lo requiere. queda definido como salida futura y su contenido está especificado por el paso.
- Estado esperado: PLANIFICADO; no existe físicamente durante Chat 2.
- Evidencia esperada: M1 file 3.
- Memoria incremental del paso: ZIP de memoria acumulativa FUTURO, generado solo cuando el paso sea ejecutado; durante Chat 2 se define su estructura y función, pero no se crea.

### 15. Evidence

- Evidencia que demuestra el resultado: M1 file 3.
- Fuente de la evidencia: fuente M1 concreta, más decisiones Chat1 cuando limitan el proyecto.
- Cómo se conservará: en el artefacto futuro, en el plan y en la trazabilidad de memoria; no reemplaza RAW.

### 16. Validation

- Qué se debe verificar: Comprobar que cada tipo de contexto tiene una regla de inclusión y que una tarea concreta puede resolverse con un paquete mínimo sin cargar historial irrelevante.
- Cómo se verifica: revisión contra M1, matriz de cobertura, dependencias, criterios y estado PLANIFICADO.
- Resultado esperado de la validación: PASS cuando la unidad esté específica, completa y correctamente acotada.

### 17. Acceptance criteria

- Criterio 1: La unidad tiene un único objetivo profesional principal.
- Criterio 2: Todo contenido práctico de M1 que le corresponde conserva sus subcapacidades relevantes.
- Criterio 3: No se presenta ninguna acción futura como ejecutada durante Chat 2.

### 18. Tests

- ID de prueba: `T01-M1-P03`
- Capacidad/subcapacidad cubierta: indicada en la descripción de la prueba.
- Prueba: T01-M1-P03 — Capacidad: selección y aislamiento de contexto. Prueba: construir un paquete conceptual mínimo para una investigación read-only. Entrada: tarea + estado + restricciones + archivos candidatos. Resultado: contexto mínimo con fuentes profundas enlazadas. PASS si el paquete excluye material no pertinente y no depende de un megaprompt.
- Entrada: plan M1, contenido de M1 y escenario correspondiente.
- Resultado esperado: evidencia observable de cobertura, coherencia y trazabilidad.
- Condición de aprobación: PASS únicamente cuando la prueba produzca el resultado indicado y no dependa de una ejecución del proyecto durante Chat 2.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors

- Error plausible: Megaprompt, contexto redundante, reglas contradictorias o mezcla de histórico irrelevante.
- Cuándo podría aparecer: al redactar, revisar o ejecutar futuramente la unidad.
- Síntoma: una subcapacidad queda comprimida, no verificable o mezclada con trabajo posterior.

### 20. Detection

- Cómo detectar el error: confrontar el paso con la fuente M1, su matriz de cobertura y sus criterios de aceptación.
- Evidencia del error: fila o concepto sin actividad/artefacto/validación o una afirmación de ejecución actual.
- Señal observable: FAIL en la auditoría estructural o semántica.

### 21. Meaning

- Qué significa el error o resultado: una frontera de trabajo o una afirmación de procedencia es incorrecta.
- Qué parte del proceso afecta: calidad del paso y continuidad al siguiente.

### 22. Diagnosis

- Causa probable: compresión artificial, dependencia oculta, ambigüedad de prompt/contexto o mezcla de módulos.
- Evidencia que confirma o descarta la causa: fuente M1 → campo del paso → matriz → decisiones heredadas.
- Orden de diagnóstico: fuente → cobertura → profundidad → independencia → trazabilidad → estado.

### 23. Correction

- Corrección: ajustar contenido, separar si la independencia funcional lo exige o reclasificar como futuro/no aplica con justificación.
- Acción concreta: Aplicar Select/Compress/Isolate, reducir el punto de entrada y mover detalle a fuentes recuperables.
- Verificación posterior: repetir cobertura, profundidad, independencia, integración, trazabilidad y tests.
- Riesgos de la corrección: incrementar artificialmente pasos o adelantar módulos posteriores.

### 24. Close checklist

- [ ] Objetivo cumplido.
- [ ] Dependencias satisfechas.
- [ ] Archivos comprobados.
- [ ] Validación completada.
- [ ] Criterios de aceptación cumplidos.
- [ ] Evidencia conservada.
- [ ] Trazabilidad completada.
- [ ] Estado actualizado.

### 25. Traceability

- M1 → archivo → sección/tema → concepto: `3. Pilar 2 — El Contexto.md`: context rot; tipos de contexto; Write/Select/Compress/Isolate; AGENTS.md/CLAUDE.md; subagentes; compactación; higiene contextual. → Context rot; contexto de código relevante, convenciones, estado actual, intención/especificación, restricciones, memoria persistente, documentación externa e historial; Write, Select, Compress, Isolate; progressive disclosure; AGENTS/CLAUDE; subagentes..
- Concepto → actividad: Clasificar contexto estable vs situacional, definir entradas mínimas y reglas de recuperación/aislamiento, y diseñar un mapa de navegación hacia fuentes profundas..
- Actividad → paso: `M1-P03`.
- Paso → artefacto: FUTURO: `M1_CONTEXT_KIT.md`; `AGENTS.md` corto como mapa; `CLAUDE.md` solamente si la herramienta futura lo requiere..
- Paso → evidencia: documental; el resultado futuro no está ejecutado.
- Paso → validación: Comprobar que cada tipo de contexto tiene una regla de inclusión y que una tarea concreta puede resolverse con un paquete mínimo sin cargar historial irrelevante..
- Paso → memoria ZIP incremental: definida como artefacto FUTURO de continuidad por ejecución.
- Paso → siguiente paso: M1-P04, M1-P05, M1-P06.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada: OpenAI, 2026-02-11, https://openai.com/index/harness-engineering/, repository knowledge como system of record y progressive disclosure; consulta dentro del cutoff de 2026-09-11.

### 26. State

- Estado inicial: PLANIFICADO.
- Estado final esperado: salida futura definida y lista para validación/ejecución posterior.
- Estado real: durante Chat 2 se diseñó el plan; no se ejecutó la unidad sobre el producto.
- Qué queda pendiente: ejecución futura y generación del artefacto real.
- Relación con el siguiente paso: M1-P04, M1-P05, M1-P06.

## Paso 04 — Diseñar contratos de prompt y biblioteca de patrones reutilizables

### 1. Identification

- ID del paso: `M1-P04`
- Fase: Fase A — Construcción cognitiva del plan
- Subfase: Diseño de prompts
- Estado: PLANIFICADO
- Tipo de paso: Unidad profesional coherente de planificación de M1.

### 2. Objective

- Objetivo exacto del paso: Definir prompts claros y verificables para futuras tareas del proyecto, con contexto, objetivo, éxito, restricciones, recursos y formato.

### 3. Direct relation to M1

- Archivo(s) de M1: `4. Pilar 3 — El Prompt + Integración.md`: anatomía del prompt; delimitadores; XML/Markdown; criterios de éxito; restricciones; anti-patterns; casos de integración.
- Sección(es)/tema(s): `4. Pilar 3 — El Prompt + Integración.md`: anatomía del prompt; delimitadores; XML/Markdown; criterios de éxito; restricciones; anti-patterns; casos de integración.
- Concepto(s) de M1: Role, context, objective, success criteria, constraints, resources y output/format; delimitadores; positive framing; few-shot cuando aporte valor; evitar solicitar chain-of-thought; prompts cortos/directos; anti-patterns.
- Relación directa: El contenido se convierte en una actividad futura verificable sobre el proyecto real, sin ejecutar el producto durante Chat 2.

### 4. Prerequisites

- Conocimientos previos: lectura completa de M1 y comprensión del objetivo SRE como contexto.
- Condiciones previas: bootstrap Chat 2, STATE/DECISIONS/OPEN_QUESTIONS/HANDOFF recuperados.
- Evidencia o artefactos necesarios: fuentes M1, decisiones Chat1 y referencia SRE.

### 5. Dependencies

- Depende de: M1-P01, M1-P03
- Habilita: M1-P05, M1-P06
- Tipo de dependencia: secuencial funcional dentro de M1.
- Riesgo si se altera el orden: se perdería una entrada de diseño o se introduciría retrabajo/ambigüedad; para P01 no existe dependencia previa de M1.

### 6. Preparation

- Preparación necesaria: Diseñar plantillas para análisis, planificación futura, revisión y documentación, cada una con entradas, objetivo, criterios de aceptación, límites y formato.
- Entorno: copia de trabajo independiente; ningún repositorio externo se modifica.
- Información que debe estar disponible: M1 completo, decisiones heredadas, límites M12 reference-only y estado real del nuevo proyecto.

### 7. Files

- Archivos que se leerán: `4. Pilar 3 — El Prompt + Integración.md` y referencias M1.
- Archivos que se crearán en la ejecución futura: FUTURO: `M1_PROMPT_LIBRARY.md`.
- Archivos que se modificarían en la ejecución futura: FUTURO y sujeto a revisión; ninguno se modifica durante Chat 2.
- Ubicación exacta de cada archivo: artefactos futuros en la raíz documental del nuevo proyecto; no existen físicamente durante Chat 2.

### 8. Directory structure

```text
<raíz del proyecto SRE — ejecución futura>
├── M1_OPERATING_MODEL.md
├── M1_TOOL_MATRIX.md
├── M1_CONTEXT_KIT.md
├── M1_PROMPT_LIBRARY.md
├── M1_WORKFLOW_RULES.md
└── M1_VALIDATION_REGISTER.md
```
Los nombres muestran el conjunto de posibles artefactos M1; cada paso crea solo el que su campo Files identifica y únicamente en ejecución futura.

### 9. Required concepts

- Concepto: Role, context, objective, success criteria, constraints, resources y output/format; delimitadores; positive framing; few-shot cuando aporte valor; evitar solicitar chain-of-thought; prompts cortos/directos; anti-patterns.
- Explicación necesaria: desarrollar qué es, cuándo se usa, cómo se aplica, criterio de elección, entrada, salida, evidencia y validación cuando M1 los diferencia.
- Nivel requerido para ejecutar el paso: aplicación operativa y verificable; no implementación del producto.

### 10. Commands

```text
NO APLICA — Chat 2 es planificación; no se ejecuta ningún comando del proyecto nuevo.
```
- Ubicación desde la que se ejecuta cada comando: NO APLICA durante Chat 2.
- Resultado esperado: no existe ejecución del proyecto.
- Verificación: revisar que los comandos futuros estén marcados FUTURO/PLANIFICADO.

### 11. Code

```text
NO APLICA — no se crea código del producto durante Chat 2.
```
- Propósito: conservar la frontera entre planificación y ejecución.
- Partes relevantes: ningún código ejecutado.
- Personalización requerida: se resolverá en la ejecución futura con el repositorio real.

### 12. Action

- Acción concreta que se realizará: Diseñar plantillas para análisis, planificación futura, revisión y documentación, cada una con entradas, objetivo, criterios de aceptación, límites y formato.
- Orden de ejecución: aplicar el contenido M1 indicado → producir artefacto futuro → validar → registrar evidencia.
- Entrada utilizada: contenido real de M1 + contexto SRE + decisiones heredadas.
- Salida producida: FUTURO: `M1_PROMPT_LIBRARY.md`.

### 13. Reason

- Por qué se realiza esta acción: convierte conocimiento de M1 en una unidad profesional reutilizable.
- Qué problema resuelve: Prompt ambiguo, exceso de instrucciones, criterios de éxito no observables o delimitación insuficiente.
- Por qué corresponde a M1: deriva del contenido práctico de M1 y no de implementación posterior.

### 14. Expected result

- Resultado esperado: FUTURO: `M1_PROMPT_LIBRARY.md`. queda definido como salida futura y su contenido está especificado por el paso.
- Estado esperado: PLANIFICADO; no existe físicamente durante Chat 2.
- Evidencia esperada: M1 file 4.
- Memoria incremental del paso: ZIP de memoria acumulativa FUTURO, generado solo cuando el paso sea ejecutado; durante Chat 2 se define su estructura y función, pero no se crea.

### 15. Evidence

- Evidencia que demuestra el resultado: M1 file 4.
- Fuente de la evidencia: fuente M1 concreta, más decisiones Chat1 cuando limitan el proyecto.
- Cómo se conservará: en el artefacto futuro, en el plan y en la trazabilidad de memoria; no reemplaza RAW.

### 16. Validation

- Qué se debe verificar: Revisar cada plantilla contra la anatomía de M1 y comprobar que el éxito es observable sin depender de razonamiento interno oculto.
- Cómo se verifica: revisión contra M1, matriz de cobertura, dependencias, criterios y estado PLANIFICADO.
- Resultado esperado de la validación: PASS cuando la unidad esté específica, completa y correctamente acotada.

### 17. Acceptance criteria

- Criterio 1: La unidad tiene un único objetivo profesional principal.
- Criterio 2: Todo contenido práctico de M1 que le corresponde conserva sus subcapacidades relevantes.
- Criterio 3: No se presenta ninguna acción futura como ejecutada durante Chat 2.

### 18. Tests

- ID de prueba: `T01-M1-P04`
- Capacidad/subcapacidad cubierta: indicada en la descripción de la prueba.
- Prueba: T01-M1-P04 — Capacidad: contrato de prompt. Prueba: revisar dos plantillas para tareas diferentes. Entrada: tarea + contexto + restricciones. Resultado: prompt estructurado con éxito observable. PASS si incluye objetivo, contexto, éxito, límites y formato, y no solicita razonamiento interno.
- Entrada: plan M1, contenido de M1 y escenario correspondiente.
- Resultado esperado: evidencia observable de cobertura, coherencia y trazabilidad.
- Condición de aprobación: PASS únicamente cuando la prueba produzca el resultado indicado y no dependa de una ejecución del proyecto durante Chat 2.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors

- Error plausible: Prompt ambiguo, exceso de instrucciones, criterios de éxito no observables o delimitación insuficiente.
- Cuándo podría aparecer: al redactar, revisar o ejecutar futuramente la unidad.
- Síntoma: una subcapacidad queda comprimida, no verificable o mezclada con trabajo posterior.

### 20. Detection

- Cómo detectar el error: confrontar el paso con la fuente M1, su matriz de cobertura y sus criterios de aceptación.
- Evidencia del error: fila o concepto sin actividad/artefacto/validación o una afirmación de ejecución actual.
- Señal observable: FAIL en la auditoría estructural o semántica.

### 21. Meaning

- Qué significa el error o resultado: una frontera de trabajo o una afirmación de procedencia es incorrecta.
- Qué parte del proceso afecta: calidad del paso y continuidad al siguiente.

### 22. Diagnosis

- Causa probable: compresión artificial, dependencia oculta, ambigüedad de prompt/contexto o mezcla de módulos.
- Evidencia que confirma o descarta la causa: fuente M1 → campo del paso → matriz → decisiones heredadas.
- Orden de diagnóstico: fuente → cobertura → profundidad → independencia → trazabilidad → estado.

### 23. Correction

- Corrección: ajustar contenido, separar si la independencia funcional lo exige o reclasificar como futuro/no aplica con justificación.
- Acción concreta: Acortar, ordenar por objetivo/éxito/constraints/resources/output y añadir delimitadores donde mejoren robustez.
- Verificación posterior: repetir cobertura, profundidad, independencia, integración, trazabilidad y tests.
- Riesgos de la corrección: incrementar artificialmente pasos o adelantar módulos posteriores.

### 24. Close checklist

- [ ] Objetivo cumplido.
- [ ] Dependencias satisfechas.
- [ ] Archivos comprobados.
- [ ] Validación completada.
- [ ] Criterios de aceptación cumplidos.
- [ ] Evidencia conservada.
- [ ] Trazabilidad completada.
- [ ] Estado actualizado.

### 25. Traceability

- M1 → archivo → sección/tema → concepto: `4. Pilar 3 — El Prompt + Integración.md`: anatomía del prompt; delimitadores; XML/Markdown; criterios de éxito; restricciones; anti-patterns; casos de integración. → Role, context, objective, success criteria, constraints, resources y output/format; delimitadores; positive framing; few-shot cuando aporte valor; evitar solicitar chain-of-thought; prompts cortos/directos; anti-patterns..
- Concepto → actividad: Diseñar plantillas para análisis, planificación futura, revisión y documentación, cada una con entradas, objetivo, criterios de aceptación, límites y formato..
- Actividad → paso: `M1-P04`.
- Paso → artefacto: FUTURO: `M1_PROMPT_LIBRARY.md`..
- Paso → evidencia: documental; el resultado futuro no está ejecutado.
- Paso → validación: Revisar cada plantilla contra la anatomía de M1 y comprobar que el éxito es observable sin depender de razonamiento interno oculto..
- Paso → memoria ZIP incremental: definida como artefacto FUTURO de continuidad por ejecución.
- Paso → siguiente paso: M1-P05, M1-P06.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada: OpenAI, 2026-02-11, https://openai.com/index/harness-engineering/, repository knowledge como system of record y progressive disclosure; consulta dentro del cutoff de 2026-09-11.

### 26. State

- Estado inicial: PLANIFICADO.
- Estado final esperado: salida futura definida y lista para validación/ejecución posterior.
- Estado real: durante Chat 2 se diseñó el plan; no se ejecutó la unidad sobre el producto.
- Qué queda pendiente: ejecución futura y generación del artefacto real.
- Relación con el siguiente paso: M1-P05, M1-P06.

## Paso 05 — Definir patrones integrados de planificar, ejecutar, probar, revisar y refactorizar

### 1. Identification

- ID del paso: `M1-P05`
- Fase: Fase A — Construcción cognitiva del plan
- Subfase: Workflows integrados
- Estado: PLANIFICADO
- Tipo de paso: Unidad profesional coherente de planificación de M1.

### 2. Objective

- Objetivo exacto del paso: Transformar la integración de los tres pilares en ciclos de trabajo repetibles para tareas futuras del proyecto, manteniendo la ejecución real fuera de Chat 2.

### 3. Direct relation to M1

- Archivo(s) de M1: `4. Pilar 3 — El Prompt + Integración.md`: spec-driven preview, plan-then-execute, test-first, refactor anchors, critic loops e integración de tree/context/prompt/execute/review.
- Sección(es)/tema(s): `4. Pilar 3 — El Prompt + Integración.md`: spec-driven preview, plan-then-execute, test-first, refactor anchors, critic loops e integración de tree/context/prompt/execute/review.
- Concepto(s) de M1: Explorar antes de actuar; plan-then-execute; test-first; refactor anchors; critic/review loops; feedback; límites entre plan y ejecución.
- Relación directa: El contenido se convierte en una actividad futura verificable sobre el proyecto real, sin ejecutar el producto durante Chat 2.

### 4. Prerequisites

- Conocimientos previos: lectura completa de M1 y comprensión del objetivo SRE como contexto.
- Condiciones previas: bootstrap Chat 2, STATE/DECISIONS/OPEN_QUESTIONS/HANDOFF recuperados.
- Evidencia o artefactos necesarios: fuentes M1, decisiones Chat1 y referencia SRE.

### 5. Dependencies

- Depende de: M1-P01, M1-P02, M1-P03, M1-P04
- Habilita: M1-P06, M1-P07
- Tipo de dependencia: secuencial funcional dentro de M1.
- Riesgo si se altera el orden: se perdería una entrada de diseño o se introduciría retrabajo/ambigüedad; para P01 no existe dependencia previa de M1.

### 6. Preparation

- Preparación necesaria: Definir para cada workflow cuándo explorar, planificar, ejecutar, probar, revisar y cerrar, y qué salida produce cada etapa.
- Entorno: copia de trabajo independiente; ningún repositorio externo se modifica.
- Información que debe estar disponible: M1 completo, decisiones heredadas, límites M12 reference-only y estado real del nuevo proyecto.

### 7. Files

- Archivos que se leerán: `4. Pilar 3 — El Prompt + Integración.md`.
- Archivos que se crearán en la ejecución futura: FUTURO: `M1_WORKFLOW_RULES.md`.
- Archivos que se modificarían en la ejecución futura: FUTURO y sujeto a revisión; ninguno se modifica durante Chat 2.
- Ubicación exacta de cada archivo: artefactos futuros en la raíz documental del nuevo proyecto; no existen físicamente durante Chat 2.

### 8. Directory structure

```text
<raíz del proyecto SRE — ejecución futura>
├── M1_OPERATING_MODEL.md
├── M1_TOOL_MATRIX.md
├── M1_CONTEXT_KIT.md
├── M1_PROMPT_LIBRARY.md
├── M1_WORKFLOW_RULES.md
└── M1_VALIDATION_REGISTER.md
```
Los nombres muestran el conjunto de posibles artefactos M1; cada paso crea solo el que su campo Files identifica y únicamente en ejecución futura.

### 9. Required concepts

- Concepto: Explorar antes de actuar; plan-then-execute; test-first; refactor anchors; critic/review loops; feedback; límites entre plan y ejecución.
- Explicación necesaria: desarrollar qué es, cuándo se usa, cómo se aplica, criterio de elección, entrada, salida, evidencia y validación cuando M1 los diferencia.
- Nivel requerido para ejecutar el paso: aplicación operativa y verificable; no implementación del producto.

### 10. Commands

```text
NO APLICA — Chat 2 es planificación; no se ejecuta ningún comando del proyecto nuevo.
```
- Ubicación desde la que se ejecuta cada comando: NO APLICA durante Chat 2.
- Resultado esperado: no existe ejecución del proyecto.
- Verificación: revisar que los comandos futuros estén marcados FUTURO/PLANIFICADO.

### 11. Code

```text
NO APLICA — no se crea código del producto durante Chat 2.
```
- Propósito: conservar la frontera entre planificación y ejecución.
- Partes relevantes: ningún código ejecutado.
- Personalización requerida: se resolverá en la ejecución futura con el repositorio real.

### 12. Action

- Acción concreta que se realizará: Definir para cada workflow cuándo explorar, planificar, ejecutar, probar, revisar y cerrar, y qué salida produce cada etapa.
- Orden de ejecución: aplicar el contenido M1 indicado → producir artefacto futuro → validar → registrar evidencia.
- Entrada utilizada: contenido real de M1 + contexto SRE + decisiones heredadas.
- Salida producida: FUTURO: `M1_WORKFLOW_RULES.md`.

### 13. Reason

- Por qué se realiza esta acción: convierte conocimiento de M1 en una unidad profesional reutilizable.
- Qué problema resuelve: Salto de planificación, ejecución no autorizada, ausencia de feedback o refactor sin ancla.
- Por qué corresponde a M1: deriva del contenido práctico de M1 y no de implementación posterior.

### 14. Expected result

- Resultado esperado: FUTURO: `M1_WORKFLOW_RULES.md`. queda definido como salida futura y su contenido está especificado por el paso.
- Estado esperado: PLANIFICADO; no existe físicamente durante Chat 2.
- Evidencia esperada: M1 file 4 y sus casos de aplicación.
- Memoria incremental del paso: ZIP de memoria acumulativa FUTURO, generado solo cuando el paso sea ejecutado; durante Chat 2 se define su estructura y función, pero no se crea.

### 15. Evidence

- Evidencia que demuestra el resultado: M1 file 4 y sus casos de aplicación.
- Fuente de la evidencia: fuente M1 concreta, más decisiones Chat1 cuando limitan el proyecto.
- Cómo se conservará: en el artefacto futuro, en el plan y en la trazabilidad de memoria; no reemplaza RAW.

### 16. Validation

- Qué se debe verificar: Recorrer un cambio hipotético y una revisión hipotética sin tocar el proyecto, verificando entradas, gates y salidas.
- Cómo se verifica: revisión contra M1, matriz de cobertura, dependencias, criterios y estado PLANIFICADO.
- Resultado esperado de la validación: PASS cuando la unidad esté específica, completa y correctamente acotada.

### 17. Acceptance criteria

- Criterio 1: La unidad tiene un único objetivo profesional principal.
- Criterio 2: Todo contenido práctico de M1 que le corresponde conserva sus subcapacidades relevantes.
- Criterio 3: No se presenta ninguna acción futura como ejecutada durante Chat 2.

### 18. Tests

- ID de prueba: `T01-M1-P05`
- Capacidad/subcapacidad cubierta: indicada en la descripción de la prueba.
- Prueba: T01-M1-P05 — Capacidad: workflow agentic controlado. Prueba: recorrer un cambio hipotético sin escribir código. Entrada: cambio + restricciones + criterios. Resultado: secuencia de fases y gates. PASS si la planificación precede a la ejecución futura y la validación futura tiene PASS/FAIL concreto.
- Entrada: plan M1, contenido de M1 y escenario correspondiente.
- Resultado esperado: evidencia observable de cobertura, coherencia y trazabilidad.
- Condición de aprobación: PASS únicamente cuando la prueba produzca el resultado indicado y no dependa de una ejecución del proyecto durante Chat 2.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors

- Error plausible: Salto de planificación, ejecución no autorizada, ausencia de feedback o refactor sin ancla.
- Cuándo podría aparecer: al redactar, revisar o ejecutar futuramente la unidad.
- Síntoma: una subcapacidad queda comprimida, no verificable o mezclada con trabajo posterior.

### 20. Detection

- Cómo detectar el error: confrontar el paso con la fuente M1, su matriz de cobertura y sus criterios de aceptación.
- Evidencia del error: fila o concepto sin actividad/artefacto/validación o una afirmación de ejecución actual.
- Señal observable: FAIL en la auditoría estructural o semántica.

### 21. Meaning

- Qué significa el error o resultado: una frontera de trabajo o una afirmación de procedencia es incorrecta.
- Qué parte del proceso afecta: calidad del paso y continuidad al siguiente.

### 22. Diagnosis

- Causa probable: compresión artificial, dependencia oculta, ambigüedad de prompt/contexto o mezcla de módulos.
- Evidencia que confirma o descarta la causa: fuente M1 → campo del paso → matriz → decisiones heredadas.
- Orden de diagnóstico: fuente → cobertura → profundidad → independencia → trazabilidad → estado.

### 23. Correction

- Corrección: ajustar contenido, separar si la independencia funcional lo exige o reclasificar como futuro/no aplica con justificación.
- Acción concreta: Restaurar el ciclo plan→execute→test→review y marcar cualquier acción aún no realizada como FUTURA.
- Verificación posterior: repetir cobertura, profundidad, independencia, integración, trazabilidad y tests.
- Riesgos de la corrección: incrementar artificialmente pasos o adelantar módulos posteriores.

### 24. Close checklist

- [ ] Objetivo cumplido.
- [ ] Dependencias satisfechas.
- [ ] Archivos comprobados.
- [ ] Validación completada.
- [ ] Criterios de aceptación cumplidos.
- [ ] Evidencia conservada.
- [ ] Trazabilidad completada.
- [ ] Estado actualizado.

### 25. Traceability

- M1 → archivo → sección/tema → concepto: `4. Pilar 3 — El Prompt + Integración.md`: spec-driven preview, plan-then-execute, test-first, refactor anchors, critic loops e integración de tree/context/prompt/execute/review. → Explorar antes de actuar; plan-then-execute; test-first; refactor anchors; critic/review loops; feedback; límites entre plan y ejecución..
- Concepto → actividad: Definir para cada workflow cuándo explorar, planificar, ejecutar, probar, revisar y cerrar, y qué salida produce cada etapa..
- Actividad → paso: `M1-P05`.
- Paso → artefacto: FUTURO: `M1_WORKFLOW_RULES.md`..
- Paso → evidencia: documental; el resultado futuro no está ejecutado.
- Paso → validación: Recorrer un cambio hipotético y una revisión hipotética sin tocar el proyecto, verificando entradas, gates y salidas..
- Paso → memoria ZIP incremental: definida como artefacto FUTURO de continuidad por ejecución.
- Paso → siguiente paso: M1-P06, M1-P07.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada: OpenAI, 2026-02-11, https://openai.com/index/harness-engineering/, repository knowledge como system of record y progressive disclosure; consulta dentro del cutoff de 2026-09-11.

### 26. State

- Estado inicial: PLANIFICADO.
- Estado final esperado: salida futura definida y lista para validación/ejecución posterior.
- Estado real: durante Chat 2 se diseñó el plan; no se ejecutó la unidad sobre el producto.
- Qué queda pendiente: ejecución futura y generación del artefacto real.
- Relación con el siguiente paso: M1-P06, M1-P07.

## Paso 06 — Consolidar el modelo operativo AI-assisted específico del proyecto SRE

### 1. Identification

- ID del paso: `M1-P06`
- Fase: Fase A — Construcción cognitiva del plan
- Subfase: Consolidación
- Estado: PLANIFICADO
- Tipo de paso: Unidad profesional coherente de planificación de M1.

### 2. Objective

- Objetivo exacto del paso: Unificar herramienta, contexto y prompt en un operating model que alimente las etapas posteriores del Agentic SDLC sin implementar el agente, backend o infraestructura.

### 3. Direct relation to M1

- Archivo(s) de M1: `1. El modelo mental de los 3 pilares.md` + `2. Pilar 1 — La Herramienta.md` + `3. Pilar 2 — El Contexto.md` + `4. Pilar 3 — El Prompt + Integración.md`.
- Sección(es)/tema(s): `1. El modelo mental de los 3 pilares.md` + `2. Pilar 1 — La Herramienta.md` + `3. Pilar 2 — El Contexto.md` + `4. Pilar 3 — El Prompt + Integración.md`.
- Concepto(s) de M1: Integración de tres pilares; trazabilidad; elección de herramienta; contexto mínimo suficiente; prompt como contrato; feedback loops; read-only-first como límite heredado.
- Relación directa: El contenido se convierte en una actividad futura verificable sobre el proyecto real, sin ejecutar el producto durante Chat 2.

### 4. Prerequisites

- Conocimientos previos: lectura completa de M1 y comprensión del objetivo SRE como contexto.
- Condiciones previas: bootstrap Chat 2, STATE/DECISIONS/OPEN_QUESTIONS/HANDOFF recuperados.
- Evidencia o artefactos necesarios: fuentes M1, decisiones Chat1 y referencia SRE.

### 5. Dependencies

- Depende de: M1-P02, M1-P03, M1-P04, M1-P05
- Habilita: M1-P07, M3
- Tipo de dependencia: secuencial funcional dentro de M1.
- Riesgo si se altera el orden: se perdería una entrada de diseño o se introduciría retrabajo/ambigüedad; para P01 no existe dependencia previa de M1.

### 6. Preparation

- Preparación necesaria: Integrar P02-P05 en una secuencia única: entrada de tarea → selección de modo/herramienta → contexto → prompt → ejecución futura → revisión/test → cierre.
- Entorno: copia de trabajo independiente; ningún repositorio externo se modifica.
- Información que debe estar disponible: M1 completo, decisiones heredadas, límites M12 reference-only y estado real del nuevo proyecto.

### 7. Files

- Archivos que se leerán: M1 files 1-4; decisiones heredadas DEC-0002 y DEC-0004.
- Archivos que se crearán en la ejecución futura: FUTURO: `M1_OPERATING_MODEL.md` consolidado y enlaces a los artefactos M1 específicos.
- Archivos que se modificarían en la ejecución futura: FUTURO y sujeto a revisión; ninguno se modifica durante Chat 2.
- Ubicación exacta de cada archivo: artefactos futuros en la raíz documental del nuevo proyecto; no existen físicamente durante Chat 2.

### 8. Directory structure

```text
<raíz del proyecto SRE — ejecución futura>
├── M1_OPERATING_MODEL.md
├── M1_TOOL_MATRIX.md
├── M1_CONTEXT_KIT.md
├── M1_PROMPT_LIBRARY.md
├── M1_WORKFLOW_RULES.md
└── M1_VALIDATION_REGISTER.md
```
Los nombres muestran el conjunto de posibles artefactos M1; cada paso crea solo el que su campo Files identifica y únicamente en ejecución futura.

### 9. Required concepts

- Concepto: Integración de tres pilares; trazabilidad; elección de herramienta; contexto mínimo suficiente; prompt como contrato; feedback loops; read-only-first como límite heredado.
- Explicación necesaria: desarrollar qué es, cuándo se usa, cómo se aplica, criterio de elección, entrada, salida, evidencia y validación cuando M1 los diferencia.
- Nivel requerido para ejecutar el paso: aplicación operativa y verificable; no implementación del producto.

### 10. Commands

```text
NO APLICA — Chat 2 es planificación; no se ejecuta ningún comando del proyecto nuevo.
```
- Ubicación desde la que se ejecuta cada comando: NO APLICA durante Chat 2.
- Resultado esperado: no existe ejecución del proyecto.
- Verificación: revisar que los comandos futuros estén marcados FUTURO/PLANIFICADO.

### 11. Code

```text
NO APLICA — no se crea código del producto durante Chat 2.
```
- Propósito: conservar la frontera entre planificación y ejecución.
- Partes relevantes: ningún código ejecutado.
- Personalización requerida: se resolverá en la ejecución futura con el repositorio real.

### 12. Action

- Acción concreta que se realizará: Integrar P02-P05 en una secuencia única: entrada de tarea → selección de modo/herramienta → contexto → prompt → ejecución futura → revisión/test → cierre.
- Orden de ejecución: aplicar el contenido M1 indicado → producir artefacto futuro → validar → registrar evidencia.
- Entrada utilizada: contenido real de M1 + contexto SRE + decisiones heredadas.
- Salida producida: FUTURO: `M1_OPERATING_MODEL.md` consolidado y enlaces a los artefactos M1 específicos.

### 13. Reason

- Por qué se realiza esta acción: convierte conocimiento de M1 en una unidad profesional reutilizable.
- Qué problema resuelve: Integración que diluya una capacidad independiente o que introduzca infraestructura/harness no derivado de M1.
- Por qué corresponde a M1: deriva del contenido práctico de M1 y no de implementación posterior.

### 14. Expected result

- Resultado esperado: FUTURO: `M1_OPERATING_MODEL.md` consolidado y enlaces a los artefactos M1 específicos. queda definido como salida futura y su contenido está especificado por el paso.
- Estado esperado: PLANIFICADO; no existe físicamente durante Chat 2.
- Evidencia esperada: M1 files 1-4 y decisiones Chat 1 relevantes.
- Memoria incremental del paso: ZIP de memoria acumulativa FUTURO, generado solo cuando el paso sea ejecutado; durante Chat 2 se define su estructura y función, pero no se crea.

### 15. Evidence

- Evidencia que demuestra el resultado: M1 files 1-4 y decisiones Chat 1 relevantes.
- Fuente de la evidencia: fuente M1 concreta, más decisiones Chat1 cuando limitan el proyecto.
- Cómo se conservará: en el artefacto futuro, en el plan y en la trazabilidad de memoria; no reemplaza RAW.

### 16. Validation

- Qué se debe verificar: Comprobar que cada pilar conserva su contenido práctico y que la integración no adelanta M3 ni módulos posteriores.
- Cómo se verifica: revisión contra M1, matriz de cobertura, dependencias, criterios y estado PLANIFICADO.
- Resultado esperado de la validación: PASS cuando la unidad esté específica, completa y correctamente acotada.

### 17. Acceptance criteria

- Criterio 1: La unidad tiene un único objetivo profesional principal.
- Criterio 2: Todo contenido práctico de M1 que le corresponde conserva sus subcapacidades relevantes.
- Criterio 3: No se presenta ninguna acción futura como ejecutada durante Chat 2.

### 18. Tests

- ID de prueba: `T01-M1-P06`
- Capacidad/subcapacidad cubierta: indicada en la descripción de la prueba.
- Prueba: T01-M1-P06 — Capacidad: integración tool/context/prompt. Prueba: producir la cadena de trabajo para una investigación read-only. Entrada: escenario + restricciones heredadas. Resultado: operating model completo. PASS si cada etapa tiene salida/gate y ninguna etapa habilita mutación.
- Entrada: plan M1, contenido de M1 y escenario correspondiente.
- Resultado esperado: evidencia observable de cobertura, coherencia y trazabilidad.
- Condición de aprobación: PASS únicamente cuando la prueba produzca el resultado indicado y no dependa de una ejecución del proyecto durante Chat 2.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors

- Error plausible: Integración que diluya una capacidad independiente o que introduzca infraestructura/harness no derivado de M1.
- Cuándo podría aparecer: al redactar, revisar o ejecutar futuramente la unidad.
- Síntoma: una subcapacidad queda comprimida, no verificable o mezclada con trabajo posterior.

### 20. Detection

- Cómo detectar el error: confrontar el paso con la fuente M1, su matriz de cobertura y sus criterios de aceptación.
- Evidencia del error: fila o concepto sin actividad/artefacto/validación o una afirmación de ejecución actual.
- Señal observable: FAIL en la auditoría estructural o semántica.

### 21. Meaning

- Qué significa el error o resultado: una frontera de trabajo o una afirmación de procedencia es incorrecta.
- Qué parte del proceso afecta: calidad del paso y continuidad al siguiente.

### 22. Diagnosis

- Causa probable: compresión artificial, dependencia oculta, ambigüedad de prompt/contexto o mezcla de módulos.
- Evidencia que confirma o descarta la causa: fuente M1 → campo del paso → matriz → decisiones heredadas.
- Orden de diagnóstico: fuente → cobertura → profundidad → independencia → trazabilidad → estado.

### 23. Correction

- Corrección: ajustar contenido, separar si la independencia funcional lo exige o reclasificar como futuro/no aplica con justificación.
- Acción concreta: Restituir el detalle práctico de los pasos P02-P05 y eliminar cualquier implementación de módulos posteriores.
- Verificación posterior: repetir cobertura, profundidad, independencia, integración, trazabilidad y tests.
- Riesgos de la corrección: incrementar artificialmente pasos o adelantar módulos posteriores.

### 24. Close checklist

- [ ] Objetivo cumplido.
- [ ] Dependencias satisfechas.
- [ ] Archivos comprobados.
- [ ] Validación completada.
- [ ] Criterios de aceptación cumplidos.
- [ ] Evidencia conservada.
- [ ] Trazabilidad completada.
- [ ] Estado actualizado.

### 25. Traceability

- M1 → archivo → sección/tema → concepto: `1. El modelo mental de los 3 pilares.md` + `2. Pilar 1 — La Herramienta.md` + `3. Pilar 2 — El Contexto.md` + `4. Pilar 3 — El Prompt + Integración.md`. → Integración de tres pilares; trazabilidad; elección de herramienta; contexto mínimo suficiente; prompt como contrato; feedback loops; read-only-first como límite heredado..
- Concepto → actividad: Integrar P02-P05 en una secuencia única: entrada de tarea → selección de modo/herramienta → contexto → prompt → ejecución futura → revisión/test → cierre..
- Actividad → paso: `M1-P06`.
- Paso → artefacto: FUTURO: `M1_OPERATING_MODEL.md` consolidado y enlaces a los artefactos M1 específicos..
- Paso → evidencia: documental; el resultado futuro no está ejecutado.
- Paso → validación: Comprobar que cada pilar conserva su contenido práctico y que la integración no adelanta M3 ni módulos posteriores..
- Paso → memoria ZIP incremental: definida como artefacto FUTURO de continuidad por ejecución.
- Paso → siguiente paso: M1-P07, M3.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada: OpenAI, 2026-02-11, https://openai.com/index/harness-engineering/, repository knowledge como system of record y progressive disclosure; consulta dentro del cutoff de 2026-09-11.

### 26. State

- Estado inicial: PLANIFICADO.
- Estado final esperado: salida futura definida y lista para validación/ejecución posterior.
- Estado real: durante Chat 2 se diseñó el plan; no se ejecutó la unidad sobre el producto.
- Qué queda pendiente: ejecución futura y generación del artefacto real.
- Relación con el siguiente paso: M1-P07, M3.

## Paso 07 — Validar, documentar, controlar contaminación y establecer iteración

### 1. Identification

- ID del paso: `M1-P07`
- Fase: Fase B — Auditoría semántica y estructural
- Subfase: Gate de validación
- Estado: PLANIFICADO
- Tipo de paso: Unidad profesional coherente de planificación de M1.

### 2. Objective

- Objetivo exacto del paso: Establecer el gate final de M1 para comprobar coherencia, procedencia, higiene contextual, reutilización e iteración antes de pasar a M3.

### 3. Direct relation to M1

- Archivo(s) de M1: `1. El modelo mental de los 3 pilares.md`, `2. Pilar 1 — La Herramienta.md`, `3. Pilar 2 — El Contexto.md`, `4. Pilar 3 — El Prompt + Integración.md`, `5. Recursos adicionales.md`.
- Sección(es)/tema(s): `1. El modelo mental de los 3 pilares.md`, `2. Pilar 1 — La Herramienta.md`, `3. Pilar 2 — El Contexto.md`, `4. Pilar 3 — El Prompt + Integración.md`, `5. Recursos adicionales.md`.
- Concepto(s) de M1: Cobertura, procedencia, fecha de fuentes, contaminación, contradicciones, iteración, compactación/nueva sesión, feedback y revalidación.
- Relación directa: El contenido se convierte en una actividad futura verificable sobre el proyecto real, sin ejecutar el producto durante Chat 2.

### 4. Prerequisites

- Conocimientos previos: lectura completa de M1 y comprensión del objetivo SRE como contexto.
- Condiciones previas: bootstrap Chat 2, STATE/DECISIONS/OPEN_QUESTIONS/HANDOFF recuperados.
- Evidencia o artefactos necesarios: fuentes M1, decisiones Chat1 y referencia SRE.

### 5. Dependencies

- Depende de: M1-P01, M1-P02, M1-P03, M1-P04, M1-P05, M1-P06
- Habilita: Siguiente módulo (M3) sin ejecución
- Tipo de dependencia: secuencial funcional dentro de M1.
- Riesgo si se altera el orden: se perdería una entrada de diseño o se introduciría retrabajo/ambigüedad; para P01 no existe dependencia previa de M1.

### 6. Preparation

- Preparación necesaria: Definir un registro de validación y una rutina de regresión para detectar prompts ambiguos, contexto excesivo, tool/mode mismatch, fuentes desactualizadas y reglas contradictorias.
- Entorno: copia de trabajo independiente; ningún repositorio externo se modifica.
- Información que debe estar disponible: M1 completo, decisiones heredadas, límites M12 reference-only y estado real del nuevo proyecto.

### 7. Files

- Archivos que se leerán: M1 files 1-5; `MEMORY_PROTOCOL.md`; registro de fuentes.
- Archivos que se crearán en la ejecución futura: FUTURO: `M1_VALIDATION_REGISTER.md`.
- Archivos que se modificarían en la ejecución futura: FUTURO y sujeto a revisión; ninguno se modifica durante Chat 2.
- Ubicación exacta de cada archivo: artefactos futuros en la raíz documental del nuevo proyecto; no existen físicamente durante Chat 2.

### 8. Directory structure

```text
<raíz del proyecto SRE — ejecución futura>
├── M1_OPERATING_MODEL.md
├── M1_TOOL_MATRIX.md
├── M1_CONTEXT_KIT.md
├── M1_PROMPT_LIBRARY.md
├── M1_WORKFLOW_RULES.md
└── M1_VALIDATION_REGISTER.md
```
Los nombres muestran el conjunto de posibles artefactos M1; cada paso crea solo el que su campo Files identifica y únicamente en ejecución futura.

### 9. Required concepts

- Concepto: Cobertura, procedencia, fecha de fuentes, contaminación, contradicciones, iteración, compactación/nueva sesión, feedback y revalidación.
- Explicación necesaria: desarrollar qué es, cuándo se usa, cómo se aplica, criterio de elección, entrada, salida, evidencia y validación cuando M1 los diferencia.
- Nivel requerido para ejecutar el paso: aplicación operativa y verificable; no implementación del producto.

### 10. Commands

```text
NO APLICA — Chat 2 es planificación; no se ejecuta ningún comando del proyecto nuevo.
```
- Ubicación desde la que se ejecuta cada comando: NO APLICA durante Chat 2.
- Resultado esperado: no existe ejecución del proyecto.
- Verificación: revisar que los comandos futuros estén marcados FUTURO/PLANIFICADO.

### 11. Code

```text
NO APLICA — no se crea código del producto durante Chat 2.
```
- Propósito: conservar la frontera entre planificación y ejecución.
- Partes relevantes: ningún código ejecutado.
- Personalización requerida: se resolverá en la ejecución futura con el repositorio real.

### 12. Action

- Acción concreta que se realizará: Definir un registro de validación y una rutina de regresión para detectar prompts ambiguos, contexto excesivo, tool/mode mismatch, fuentes desactualizadas y reglas contradictorias.
- Orden de ejecución: aplicar el contenido M1 indicado → producir artefacto futuro → validar → registrar evidencia.
- Entrada utilizada: contenido real de M1 + contexto SRE + decisiones heredadas.
- Salida producida: FUTURO: `M1_VALIDATION_REGISTER.md`.

### 13. Reason

- Por qué se realiza esta acción: convierte conocimiento de M1 en una unidad profesional reutilizable.
- Qué problema resuelve: Cobertura nominal, fuente sin fecha/procedencia, prueba incompleta o contradicción no registrada.
- Por qué corresponde a M1: deriva del contenido práctico de M1 y no de implementación posterior.

### 14. Expected result

- Resultado esperado: FUTURO: `M1_VALIDATION_REGISTER.md`. queda definido como salida futura y su contenido está especificado por el paso.
- Estado esperado: PLANIFICADO; no existe físicamente durante Chat 2.
- Evidencia esperada: M1 file 5 y su conjunto de recursos; además de OpenAI harness engineering como corroboración externa.
- Memoria incremental del paso: ZIP de memoria acumulativa FUTURO, generado solo cuando el paso sea ejecutado; durante Chat 2 se define su estructura y función, pero no se crea.

### 15. Evidence

- Evidencia que demuestra el resultado: M1 file 5 y su conjunto de recursos; además de OpenAI harness engineering como corroboración externa.
- Fuente de la evidencia: fuente M1 concreta, más decisiones Chat1 cuando limitan el proyecto.
- Cómo se conservará: en el artefacto futuro, en el plan y en la trazabilidad de memoria; no reemplaza RAW.

### 16. Validation

- Qué se debe verificar: Auditar cada capacidad de M1 contra su fuente, paso, artefacto, evidencia, validación y estado; bloquear el cierre ante cualquier FAIL.
- Cómo se verifica: revisión contra M1, matriz de cobertura, dependencias, criterios y estado PLANIFICADO.
- Resultado esperado de la validación: PASS cuando la unidad esté específica, completa y correctamente acotada.

### 17. Acceptance criteria

- Criterio 1: La unidad tiene un único objetivo profesional principal.
- Criterio 2: Todo contenido práctico de M1 que le corresponde conserva sus subcapacidades relevantes.
- Criterio 3: No se presenta ninguna acción futura como ejecutada durante Chat 2.

### 18. Tests

- ID de prueba: `T01-M1-P07`
- Capacidad/subcapacidad cubierta: indicada en la descripción de la prueba.
- Prueba: T01-M1-P07 — Capacidad: gate de cobertura/procedencia/higiene. Prueba: revisar el M1_PLAN completo y sus matrices. Entrada: plan + matriz de cobertura + fuentes. Resultado: cero capacidades prácticas sin paso, cero campos faltantes y cero afirmaciones futuras presentadas como ejecutadas. PASS si se cumple el 100% de esas condiciones.
- Entrada: plan M1, contenido de M1 y escenario correspondiente.
- Resultado esperado: evidencia observable de cobertura, coherencia y trazabilidad.
- Condición de aprobación: PASS únicamente cuando la prueba produzca el resultado indicado y no dependa de una ejecución del proyecto durante Chat 2.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors

- Error plausible: Cobertura nominal, fuente sin fecha/procedencia, prueba incompleta o contradicción no registrada.
- Cuándo podría aparecer: al redactar, revisar o ejecutar futuramente la unidad.
- Síntoma: una subcapacidad queda comprimida, no verificable o mezclada con trabajo posterior.

### 20. Detection

- Cómo detectar el error: confrontar el paso con la fuente M1, su matriz de cobertura y sus criterios de aceptación.
- Evidencia del error: fila o concepto sin actividad/artefacto/validación o una afirmación de ejecución actual.
- Señal observable: FAIL en la auditoría estructural o semántica.

### 21. Meaning

- Qué significa el error o resultado: una frontera de trabajo o una afirmación de procedencia es incorrecta.
- Qué parte del proceso afecta: calidad del paso y continuidad al siguiente.

### 22. Diagnosis

- Causa probable: compresión artificial, dependencia oculta, ambigüedad de prompt/contexto o mezcla de módulos.
- Evidencia que confirma o descarta la causa: fuente M1 → campo del paso → matriz → decisiones heredadas.
- Orden de diagnóstico: fuente → cobertura → profundidad → independencia → trazabilidad → estado.

### 23. Correction

- Corrección: ajustar contenido, separar si la independencia funcional lo exige o reclasificar como futuro/no aplica con justificación.
- Acción concreta: Corregir el plan y repetir las auditorías estructural y semántica antes del cierre.
- Verificación posterior: repetir cobertura, profundidad, independencia, integración, trazabilidad y tests.
- Riesgos de la corrección: incrementar artificialmente pasos o adelantar módulos posteriores.

### 24. Close checklist

- [ ] Objetivo cumplido.
- [ ] Dependencias satisfechas.
- [ ] Archivos comprobados.
- [ ] Validación completada.
- [ ] Criterios de aceptación cumplidos.
- [ ] Evidencia conservada.
- [ ] Trazabilidad completada.
- [ ] Estado actualizado.

### 25. Traceability

- M1 → archivo → sección/tema → concepto: `1. El modelo mental de los 3 pilares.md`, `2. Pilar 1 — La Herramienta.md`, `3. Pilar 2 — El Contexto.md`, `4. Pilar 3 — El Prompt + Integración.md`, `5. Recursos adicionales.md`. → Cobertura, procedencia, fecha de fuentes, contaminación, contradicciones, iteración, compactación/nueva sesión, feedback y revalidación..
- Concepto → actividad: Definir un registro de validación y una rutina de regresión para detectar prompts ambiguos, contexto excesivo, tool/mode mismatch, fuentes desactualizadas y reglas contradictorias..
- Actividad → paso: `M1-P07`.
- Paso → artefacto: FUTURO: `M1_VALIDATION_REGISTER.md`..
- Paso → evidencia: documental; el resultado futuro no está ejecutado.
- Paso → validación: Auditar cada capacidad de M1 contra su fuente, paso, artefacto, evidencia, validación y estado; bloquear el cierre ante cualquier FAIL..
- Paso → memoria ZIP incremental: definida como artefacto FUTURO de continuidad por ejecución.
- Paso → siguiente paso: Siguiente módulo (M3) sin ejecución.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada: OpenAI, 2026-02-11, https://openai.com/index/harness-engineering/, repository knowledge como system of record y progressive disclosure; consulta dentro del cutoff de 2026-09-11.

### 26. State

- Estado inicial: PLANIFICADO.
- Estado final esperado: salida futura definida y lista para validación/ejecución posterior.
- Estado real: durante Chat 2 se diseñó el plan; no se ejecutó la unidad sobre el producto.
- Qué queda pendiente: ejecución futura y generación del artefacto real.
- Relación con el siguiente paso: Siguiente módulo (M3) sin ejecución.
