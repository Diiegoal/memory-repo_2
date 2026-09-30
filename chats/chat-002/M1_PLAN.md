# M1_PLAN.md — Chat 2

## Status

**CONGELADO / PLANIFICADO.** Chat 2 diseñó y auditó el plan, pero no ejecutó el Paso 1 del proyecto y no modificó repositorios externos.

## Dynamic step determination

La cantidad de pasos se determinó después de leer completamente los cinco archivos de M1, realizar el inventario de capacidades/subcapacidades, revisar dependencias y resultados, contrastar las decisiones heredadas de Chat 1, leer el archivo completo de referencia del Agente SRE/DevOps, revisar el Repositorio Ejemplo 2 y ejecutar pruebas de profundidad, independencia, integración, anti-compresión y anti-fragmentación. El conjunto estable emergió en **7 unidades profesionales**. No se usó un número objetivo previo.

## Step sequence

1. M1-P01 — Caracterizar la tarea y determinar el modo de trabajo.
2. M1-P02 — Seleccionar y evaluar la herramienta mediante criterios verificables.
3. M1-P03 — Diseñar la arquitectura de contexto persistente del proyecto.
4. M1-P04 — Gestionar la ventana de contexto y prevenir context rot.
5. M1-P05 — Diseñar y aplicar prompting fundamental para trabajo de ingeniería.
6. M1-P06 — Aplicar patrones de ejecución de coding asistido por IA.
7. M1-P07 — Integrar los tres pilares y validar los cinco casos canónicos de M1.

## Hard boundaries

- M1 es la única fuente de construcción en esta sesión.
- M12 es referencia-only y no integra el orden de construcción.
- M3, M4, M2, M6, M5, M7, M8, M9, M10, M11 y M13 quedan fuera de la ejecución de M1.
- Ningún repositorio externo fue modificado.
- El Paso 1 del proyecto no fue ejecutado.
- No se creó código del proyecto para demostrar avance.
- Las rutas/archivos de proyecto descritos dentro de los pasos son FUTUROS y no afirman existencia actual.
- No se adoptó una nueva decisión sustantiva en Chat 2.

## Technology scope

| Elemento | Tratamiento en M1 | Razón |
|---|---|---|
| Claude Code | PREPARAR COMO BASE PARA FUTURO | M1 enseña herramienta/contexto/prompt y Chat 2 verificó capacidades actuales sin fijarlo como decisión histórica. |
| AGENTS.md | PREPARAR COMO BASE PARA FUTURO | Instrucciones persistentes de alto señal; mecanismo a aplicar en ejecución futura. |
| FastAPI | RESERVAR PARA MÓDULO POSTERIOR | Es parte del producto de referencia, pero M1 no lo implementa. |
| LangChain/LangGraph | RESERVAR PARA MÓDULO POSTERIOR | Contexto del producto; no convertir presencia de stack en implementación de M1. |
| PostgreSQL/pgvector | RESERVAR PARA MÓDULO POSTERIOR | Decisión DEC-0005 heredada; M1 solo respeta la arquitectura futura. |
| Redis | RESERVAR PARA MÓDULO POSTERIOR / EVALUAR | OQ-0003 sigue abierta. |
| Streamlit | PREPARAR COMO BASE PARA FUTURO | DEC-0006: opcional a nivel de producto. |
| Slack | RESERVAR PARA MÓDULO POSTERIOR | Canal operativo de referencia, no actividad de M1. |
| Kubernetes/AWS/IaC/Observabilidad | RESERVAR PARA MÓDULOS POSTERIORES | Aparecen en el stack de referencia y roadmap, no como trabajo de M1. |

# Coverage control

M1 quedó cubierto por archivo y por capacidad: modelo de tres pilares; Pilar 1 con A-D, completion/agentic, switch rules, cinco criterios, modelos/benchmarks/framework/anti-patterns; Pilar 2 con tipos de contexto, context rot, 50/70/90, AGENTS.md/alternativas, buenas prácticas y Write/Select/Compress/Isolate; Pilar 3 con anatomy completa, anti-patterns, reasoning context y los cinco patrones de ejecución; e integración A-E. Todo elemento práctico quedó en uno o más pasos; lo conceptual que no constituye actividad independiente se conserva como fundamento explícito.


# Matriz — Cobertura de M1

| Archivo M1 | Tema/sección | Concepto | Aplicación práctica | Paso | Artefacto | Validación | Estado |
|---|---|---|---|---|---|---|---|
| `1. El modelo mental de los 3 pilares.md` | modelo mental | tool/context/prompt | baseline de trabajo | P01,P03,P05,P07 | registros y baseline M1 | A-E | PLANIFICADO |
| `2. Pilar 1 — La Herramienta.md` | A-D; completion/agentic; switch | clasificación de tarea | modo de trabajo | P01 | task-mode-record | T01,T02 | PLANIFICADO |
| `2. Pilar 1 — La Herramienta.md` | cinco criterios | selección contextual | evaluación | P02 | tool-selection | T01 | PLANIFICADO |
| `2. Pilar 1 — La Herramienta.md` | benchmarks/framework/anti-patterns | señales y reglas | decisión reproducible | P02 | tool-selection | T02,T03 | PLANIFICADO |
| `3. Pilar 2 — El Contexto.md` | tipos/AGENTS/alternativas | persistencia y precedencia | arquitectura de contexto | P03 | contexto persistente | T01,T02 | PLANIFICADO |
| `3. Pilar 2 — El Contexto.md` | context rot; 50/70/90 | higiene de ventana | protocolo de operación | P04 | context-operations | T01,T02,T03 | PLANIFICADO |
| `3. Pilar 2 — El Contexto.md` | Write/Select/Compress/Isolate | operaciones sobre contexto | control de sesión | P04 | context-operations | T01 | PLANIFICADO |
| `4. Pilar 3 — El Prompt + Integración.md` | anatomy | prompt verificable | prompt kit | P05 | prompt-kit | T01,T02 | PLANIFICADO |
| `4. Pilar 3 — El Prompt + Integración.md` | cinco patrones | ejecución contextual | playbook | P06 | coding-execution-patterns | T01,T02 | PLANIFICADO |
| `4. Pilar 3 — El Prompt + Integración.md` | integración A-E | sistema integrado | baseline M1 | P07 | M1_PLAN | T01-T05 | PLANIFICADO |
| `5. Recursos adicionales.md` | recursos de harness/context/prompt | evidencia complementaria | refinamiento sin cambiar eje M1 | P02-P06 | referencias | procedencia | PLANIFICADO |


# Matriz — Dependencias

| Paso | Depende de | Habilita | Tipo de dependencia | Riesgo si se invierte | Evidencia |
|---|---|---|---|---|---|
| P01 | tarea + M1 | P02 | conceptual/decisional | herramienta elegida sin entender tarea | Pilar 1 |
| P02 | P01 | P03 | decisional | elección por moda/benchmark | Pilar 1 |
| P03 | P01,P02 | P04,P05 | estructural | persistencia mal diseñada | Pilar 2 |
| P04 | P03 | P05,P07 | operacional | context rot | Pilar 2 |
| P05 | P03,P04 | P06,P07 | instrumental | prompts ambiguos | Pilar 3 |
| P06 | P01,P05 | P07 | operacional | patrón inadecuado | Pilar 3 |
| P07 | P01-P06 | baseline M1 | integración | pilares aislados o cobertura nominal | cinco archivos M1 |


# Matriz — Concepto → actividad

| Concepto M1 | Qué significa | Cómo se aplica | Artefacto | Evidencia | Validación |
|---|---|---|---|---|---|
| completion vs agentic | grado de autonomía | clasificar antes de ejecutar | task-mode-record | M1 Pilar 1 | T01/T02 P01 |
| A-D | categorías de herramienta | mapear tarea a categoría | task-mode-record | M1 Pilar 1 | P01 |
| cinco criterios | selección contextualizada | evaluar tamaño, lenguaje, privacidad, presupuesto, estilo | tool-selection | M1 Pilar 1 | P02 T01 |
| benchmarks | señales comparativas | leer limitaciones y no ranking universal | tool-selection | M1 Pilar 1/recursos | P02 T02 |
| context rot | degradación de señal | detectar y actuar antes de perder foco | context-operations | M1 Pilar 2 | P04 T02/T03 |
| Write/Select/Compress/Isolate | operaciones de contexto | aplicar según condición | context-operations | M1 Pilar 2 | P04 T01 |
| anatomy prompt | estructura de instrucción | redactar con éxito/constraints/resources/output | prompt-kit | M1 Pilar 3 | P05 T01 |
| cinco patrones | formas de ejecutar | seleccionar según tarea | coding patterns | M1 Pilar 3 | P06 T01/T02 |
| integración A-E | aplicación combinada | usar los tres pilares | baseline M1 | Pilar 3/integración | P07 T01-T05 |


# Matriz — Paso → resultado

| Paso | Entrada | Actividad | Salida | Evidencia | Criterio de aceptación | Siguiente paso |
|---|---|---|---|---|---|---|
| P01 | tarea | clasificar modo/categoría | caracterización | ficha futura | modo + categoría + switch | P02 |
| P02 | P01 + criterios | evaluar herramienta | selección reproducible | ficha futura | 5 criterios + fuentes | P03 |
| P03 | P01/P02 | diseñar contexto | arquitectura de contexto | esquema futuro | capas/precedencia/exclusiones | P04 |
| P04 | P03 | gestionar ventana | protocolo anti-rot | pruebas futuras | W/S/C/I + 50/70/90 | P05 |
| P05 | contexto + tarea | redactar prompt | prompt operativo | ejemplos futuros | anatomy completa | P06 |
| P06 | tarea + prompt | elegir patrón | playbook | pruebas futuras | cinco patrones cubiertos | P07 |
| P07 | P01-P06 | integrar A-E y refutar plan | baseline M1 | M1_PLAN + transcript | A-E completos y trazables | INDEPENDIENTE como cierre de M1; alimenta etapas posteriores |


# M1 Step Records

## Paso 01 — Caracterizar la tarea y determinar el modo de trabajo

### 1. Identification
- ID del paso: `M1-P01` (01 asignado después de estabilizar el conjunto final).
- Fase: Fase A — Construcción cognitiva del plan
- Subfase: Caracterización operativa
- Estado: PLANIFICADO
- Tipo de paso: Diseño y planificación operativa

### 2. Objective
- Objetivo exacto del paso: Caracterizar la tarea y determinar el modo de trabajo.

### 3. Direct relation to M1
- Archivo(s) de M1: `Módulo_1.../1. El modelo mental de los 3 pilares.md`; `Módulo_1.../2. Pilar 1 — La Herramienta.md`
- Sección(es)/tema(s): Modelo de tres pilares; Pilar 1: categorías A-D, completion vs agentic y reglas para cambiar de modo.
- Concepto(s) de M1: Herramienta, contexto y prompt como pilares; clasificación A-D; completion; agentic.
- Relación directa: Antes de seleccionar una herramienta se caracteriza qué tipo de trabajo se realizará, qué autonomía requiere y qué modo es coherente con la tarea.

### 4. Prerequisites
- Conocimientos previos: Comprender qué es una tarea de ingeniería y la diferencia operacional entre completion y agentic.
- Condiciones previas: Existencia de un escenario real del producto que pueda describirse sin implementar nada.
- Evidencia o artefactos necesarios: M1 leído completo; descripción del producto SRE y sus tipos de tareas como contexto.

### 5. Dependencies
- Depende de: INDEPENDIENTE; constituye la entrada de P02.
- Habilita: P02: evaluación de herramienta con criterio contextual.
- Tipo de dependencia: Conceptual/decisional
- Riesgo si se altera el orden: Elegir una herramienta por moda antes de conocer la forma real de la tarea.

### 6. Preparation
- Preparación necesaria: Describir el objetivo de la tarea, restricciones, autonomía requerida y resultado observable.
- Entorno: Futura copia de trabajo del proyecto; ninguna ejecución productiva durante Chat 2.
- Información que debe estar disponible: Tarea, restricciones, riesgo de acciones, necesidad de exploración o modificación.

### 7. Files
- Archivos que se leerán: Los dos archivos M1 indicados en Direct relation; no se leerán archivos del proyecto externo en modo escritura.
- Archivos que se crearán en la ejecución futura: FUTURO: ficha `task-mode-record.md`.
- Archivos que se modificarían en la ejecución futura: NO APLICA EN CHAT 2.
- Ubicación exacta de cada archivo: FUTURO: `<PROJECT_ROOT>/docs/ai-engineering/task-mode-record.md`.

### 8. Directory structure
```text
<PROJECT_ROOT>/
└── docs/ai-engineering/
    └── task-mode-record.md  # FUTURO
```

### 9. Required concepts
- Concepto: Categorías A-D; completion vs agentic; condición explícita para cambiar de modo.
- Explicación necesaria: Antes de seleccionar una herramienta se caracteriza qué tipo de trabajo se realizará, qué autonomía requiere y qué modo es coherente con la tarea.
- Nivel requerido para ejecutar el paso: suficiente para aplicar M1 sin implementar capacidades propias de módulos posteriores.

### 10. Commands
```text
git status --short
find . -maxdepth 2 -type f -print | sort
```
Estos comandos son FUTUROS y solo se ejecutarán al iniciar el paso en el repositorio de trabajo; no se ejecutaron sobre el proyecto durante Chat 2.
- Ubicación desde la que se ejecuta cada comando: Raíz del proyecto durante la ejecución futura.
- Resultado esperado: Inventario observable del estado del proyecto antes de actuar.
- Verificación: Comparar con la evidencia registrada y confirmar que el escenario corresponde al modo elegido.

### 11. Code
```text
NO SE CREA CÓDIGO EN CHAT 2.
```
- Propósito: El plan define código futuro solo cuando M1 lo permita; aquí el producto de la actividad es la caracterización, no código.
- Partes relevantes: No aplica a implementación; la unidad es decisional.
- Personalización requerida: Personalizar el escenario y las restricciones reales del incidente o tarea.

### 12. Action
- Acción concreta que se realizará: Registrar la tarea; clasificar A-D; decidir completion o agentic; registrar cuándo cambiaría el modo.
- Orden de ejecución: 1) describir; 2) clasificar; 3) elegir modo; 4) registrar condición de cambio.
- Entrada utilizada: Escenario de trabajo del producto SRE.
- Salida producida: Caracterización de tarea verificable.

### 13. Reason
- Por qué se realiza esta acción: M1 exige que herramienta y modo respondan a la naturaleza del trabajo.
- Qué problema resuelve: Evita comenzar con una herramienta o un patrón de autonomía que no corresponde al problema.
- Por qué corresponde a M1: Es aplicación directa del Pilar 1 y no adelanta implementación posterior.

### 14. Expected result
- Resultado esperado: Ficha completa con categoría y modo justificados.
- Estado esperado: Caracterización lista para alimentar P02.
- Evidencia esperada: Registro futuro de la clasificación y su fuente M1.
- Memoria incremental del paso: ZIP incremental futuro con la ficha y evidencia acumuladas para P02.

### 15. Evidence
- Evidencia que demuestra el resultado: La evidencia futura será la ficha y el caso utilizado; no existe ejecución del paso ahora.
- Fuente de la evidencia: M1 archivo 1 y 2; escenario del producto.
- Cómo se conservará: Guardar ficha y relación de fuente en la memoria del paso.

### 16. Validation
- Qué se debe verificar: Categoría A-D, completion/agentic, condición de cambio y correspondencia con la tarea.
- Cómo se verifica: Revisión contra M1 y contra el escenario; comprobar que no se eligió modo por preferencia.
- Resultado esperado de la validación: PASS solo con clasificación completa y justificable.

### 17. Acceptance criteria
- Criterio 1: La tarea tiene categoría A-D explícita.
- Criterio 2: El modo completion/agentic está justificado.
- Criterio 3: Existe criterio para cambiar de modo si cambia la tarea.

### 18. Tests
- ID de prueba: Ver T01…T05 dentro del campo; todas están PLANIFICADAS
- Capacidad/subcapacidad cubierta: Herramienta, contexto y prompt como pilares; clasificación A-D; completion; agentic.
- Prueba: qué se hará para comprobarla: **T01 — Categorías A-D.** Prueba: clasificar cuatro escenarios (IDE, CLI agentic, cloud standalone, especializado). Entrada: cuatro descripciones de tareas. Resultado esperado: 4/4 categorías justificadas. Condición de aprobación: ninguna queda sin clasificación.
**T02 — Completion vs agentic.** Prueba: comparar una tarea dirigida y una investigación con acciones encadenadas. Entrada: dos escenarios. Resultado esperado: modo y switch correctos. Condición de aprobación: ambas justificaciones coinciden con M1.
- Entrada: datos, escenario, estado, archivo o configuración sobre la que se ejecutará: Escenario futuro definido en cada T; ninguna prueba del paso fue ejecutada durante Chat 2.
- Resultado esperado: los resultados observables indicados en cada T; PASS/FAIL determinado por la condición explícita de cada prueba.
- Condición de aprobación: se cumplen las condiciones PASS de todas las pruebas aplicables; `NO APLICA` no se usa para evitar una prueba posible.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Clasificación incorrecta del modo.
- Cuándo podría aparecer: Cuando la tarea requiera autonomía o secuencia que no se reflejó en la ficha.
- Síntoma: Herramienta/modo no corresponde al trabajo.

### 20. Detection
- Cómo detectar el error: Comparar objetivo real con la clasificación M1.
- Evidencia del error: Ficha y descripción del escenario.
- Señal observable: Desajuste entre trabajo requerido y modo.

### 21. Meaning
- Qué significa el error o resultado: La caracterización inicial no sirve como base de selección.
- Qué parte del proceso afecta: P01 y cualquier selección posterior.

### 22. Diagnosis
- Causa probable: Confundir complejidad con autonomía o ignorar la clase de herramienta.
- Evidencia que confirma o descarta la causa: Repetir clasificación con categorías y condiciones del Pilar 1.
- Orden de diagnóstico: Objetivo → autonomía → categoría → modo → switch.

### 23. Correction
- Corrección: Reclasificar antes de seleccionar herramienta.
- Acción concreta: Modificar la ficha futura y registrar el motivo.
- Verificación posterior: Revalidar clasificación con el mismo escenario.
- Riesgos de la corrección: Elegir un modo diferente puede cambiar el flujo de trabajo futuro.

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
- M1 → archivo → sección/tema → concepto: `Módulo_1.../1. El modelo mental de los 3 pilares.md`; `Módulo_1.../2. Pilar 1 — La Herramienta.md` → Modelo de tres pilares; Pilar 1: categorías A-D, completion vs agentic y reglas para cambiar de modo. → Herramienta, contexto y prompt como pilares; clasificación A-D; completion; agentic..
- Concepto → actividad: Registrar la tarea; clasificar A-D; decidir completion o agentic; registrar cuándo cambiaría el modo.
- Actividad → paso: M1-P01
- Paso → artefacto: FUTURO: ficha `task-mode-record.md`.
- Paso → evidencia: La evidencia futura será la ficha y el caso utilizado; no existe ejecución del paso ahora.
- Paso → validación: Categoría A-D, completion/agentic, condición de cambio y correspondencia con la tarea.
- Paso → memoria ZIP incremental: ZIP incremental futuro con la ficha y evidencia acumuladas para P02.
- Paso → siguiente paso: P02 depende de esta salida; no hay dependencia artificial con fases posteriores.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: ver `knowledge/facts/external-research.md` y `knowledge/references/reference-index.md`; consulta 2026-09-30 para OpenAI Harness, AGENTS.md y Claude Code.

### 26. State
- Estado inicial: Estado de diseño; P01 no ejecutado.
- Estado final esperado: Ficha de caracterización lista para ejecución futura.
- Estado real: PLANIFICADO; no se ejecutó el Paso 1 del proyecto ni se modificó un repositorio externo.
- Qué queda pendiente: Aplicar la ficha a un escenario real en la ejecución futura.
- Relación con el siguiente paso: P02 depende de esta salida; no hay dependencia artificial con fases posteriores.
## Paso 02 — Seleccionar y evaluar la herramienta mediante criterios verificables

### 1. Identification
- ID del paso: `M1-P02` (02 asignado después de estabilizar el conjunto final).
- Fase: Fase A — Construcción cognitiva del plan
- Subfase: Evaluación de herramienta
- Estado: PLANIFICADO
- Tipo de paso: Evaluación y decisión operativa

### 2. Objective
- Objetivo exacto del paso: Seleccionar y evaluar la herramienta mediante criterios verificables.

### 3. Direct relation to M1
- Archivo(s) de M1: `Módulo_1.../2. Pilar 1 — La Herramienta.md`; `Módulo_1.../5. Recursos adicionales.md`
- Sección(es)/tema(s): Cinco criterios; modelos; benchmarks; framework de decisión; anti-patterns.
- Concepto(s) de M1: Tamaño/forma del codebase, lenguaje, privacidad/compliance, presupuesto, estilo; SWE-Bench Verified/Pro, Aider Polyglot, TerminalBench 2.0.
- Relación directa: Separa la selección/evaluación de la caracterización de tarea y obliga a justificar la herramienta con contexto y evidencia.

### 4. Prerequisites
- Conocimientos previos: P01 caracterizado en ejecución futura; conocimiento de los cinco criterios de M1.
- Condiciones previas: Fuentes vigentes y candidatas reales verificables durante la ejecución del paso.
- Evidencia o artefactos necesarios: M1 Pilar 1; fuentes externas consultadas por Chat 2: OpenAI Harness, AGENTS.md y Claude Code, solo como contexto de capacidades.

### 5. Dependencies
- Depende de: P01
- Habilita: P03: diseñar contexto compatible con la herramienta seleccionada.
- Tipo de dependencia: Decisional/evaluación
- Riesgo si se altera el orden: Elección basada solo en benchmark, marca o hábito.

### 6. Preparation
- Preparación necesaria: Definir candidatas y aplicar los cinco criterios uno por uno; usar benchmarks como señales, no como ranking universal.
- Entorno: Entorno futuro del proyecto y documentación actual de candidatas.
- Información que debe estar disponible: Restricciones técnicas, privacidad, presupuesto, estilo del trabajo y forma del codebase.

### 7. Files
- Archivos que se leerán: M1 Pilar 1 y recursos actuales relevantes.
- Archivos que se crearán en la ejecución futura: FUTURO: `tool-selection.md`.
- Archivos que se modificarían en la ejecución futura: NO APLICA EN CHAT 2.
- Ubicación exacta de cada archivo: FUTURO: `<PROJECT_ROOT>/docs/ai-engineering/tool-selection.md`.

### 8. Directory structure
```text
<PROJECT_ROOT>/
└── docs/ai-engineering/
    ├── task-mode-record.md
    └── tool-selection.md  # FUTURO
```

### 9. Required concepts
- Concepto: Cinco criterios; lectura de benchmarks; framework de decisión; anti-patterns.
- Explicación necesaria: Separa la selección/evaluación de la caracterización de tarea y obliga a justificar la herramienta con contexto y evidencia.
- Nivel requerido para ejecutar el paso: suficiente para aplicar M1 sin implementar capacidades propias de módulos posteriores.

### 10. Commands
```text
git status --short
```
FUTURO: no se ejecutó una selección dentro del repositorio objetivo durante Chat 2.
- Ubicación desde la que se ejecuta cada comando: Raíz del proyecto en ejecución futura.
- Resultado esperado: Estado del repo antes de crear el registro.
- Verificación: Comprobar que el registro tiene procedencia y fecha.

### 11. Code
```text
NO SE IMPLEMENTA CÓDIGO EN CHAT 2.
```
- Propósito: La salida es una evaluación reproducible, no una implementación.
- Partes relevantes: Cinco dimensiones, benchmarks y anti-patterns.
- Personalización requerida: Personalizar criterios con restricciones reales del producto.

### 12. Action
- Acción concreta que se realizará: Comparar candidatas usando los cinco criterios; consultar benchmarks; revisar anti-patterns; formular elección documentada.
- Orden de ejecución: P01 → cinco criterios → señales de benchmark → anti-patterns → decisión documentada.
- Entrada utilizada: Caracterización de P01 y candidatas verificables.
- Salida producida: Registro de selección reproducible.

### 13. Reason
- Por qué se realiza esta acción: M1 establece una selección contextual, no universal.
- Qué problema resuelve: Evita dependencia de una herramienta por moda o benchmark aislado.
- Por qué corresponde a M1: Es desarrollo práctico del Pilar 1.

### 14. Expected result
- Resultado esperado: Ficha completa con cinco criterios, señales, trade-offs y anti-patterns revisados.
- Estado esperado: Criterio de selección reproducible.
- Evidencia esperada: Registro y fuentes usadas.
- Memoria incremental del paso: ZIP incremental futuro con evaluación y fuentes para P03.

### 15. Evidence
- Evidencia que demuestra el resultado: La evidencia actual es documental: M1 y fuentes externas; la ficha de proyecto será futura.
- Fuente de la evidencia: M1 Pilar 1; referencias R01 y documentación oficial consultada.
- Cómo se conservará: Persistir ficha y URLs/versiones cuando aplique.

### 16. Validation
- Qué se debe verificar: Presencia de los cinco criterios y ausencia de una selección basada solo en benchmark.
- Cómo se verifica: Revisión criterio por criterio y anti-pattern check.
- Resultado esperado de la validación: PASS con 5/5 criterios y procedencia clara.

### 17. Acceptance criteria
- Criterio 1: Los cinco criterios aparecen explícitos.
- Criterio 2: Los benchmarks se usan como señales y no como sustituto del contexto.
- Criterio 3: La elección futura tiene trazabilidad y anti-pattern checks.

### 18. Tests
- ID de prueba: Ver T01…T05 dentro del campo; todas están PLANIFICADAS
- Capacidad/subcapacidad cubierta: Tamaño/forma del codebase, lenguaje, privacidad/compliance, presupuesto, estilo; SWE-Bench Verified/Pro, Aider Polyglot, TerminalBench 2.0.
- Prueba: qué se hará para comprobarla: **T01 — Cinco criterios.** Entrada: una candidata y restricciones del proyecto. Resultado: 5/5 dimensiones documentadas. PASS: ninguna dimensión vacía.
**T02 — Benchmarks.** Entrada: resultados disponibles de SWE-Bench/Aider/TerminalBench. Resultado: limitaciones y utilidad descritas. PASS: no se presenta benchmark como ranking universal.
**T03 — Anti-patterns.** Entrada: ficha de elección. Resultado: detectar elección por moda o marca. PASS: todos los anti-patterns aplicables quedan tratados.
- Entrada: datos, escenario, estado, archivo o configuración sobre la que se ejecutará: Escenario futuro definido en cada T; ninguna prueba del paso fue ejecutada durante Chat 2.
- Resultado esperado: los resultados observables indicados en cada T; PASS/FAIL determinado por la condición explícita de cada prueba.
- Condición de aprobación: se cumplen las condiciones PASS de todas las pruebas aplicables; `NO APLICA` no se usa para evitar una prueba posible.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Evaluación sin trazabilidad.
- Cuándo podría aparecer: Cuando falta una dimensión o fuente.
- Síntoma: No puede reconstruirse la elección.

### 20. Detection
- Cómo detectar el error: Auditar los cinco criterios y la procedencia.
- Evidencia del error: Ficha y fuentes.
- Señal observable: Campo sin evidencia.

### 21. Meaning
- Qué significa el error o resultado: La elección no es reproducible.
- Qué parte del proceso afecta: P02 y selección posterior.

### 22. Diagnosis
- Causa probable: Aplicación incompleta del framework.
- Evidencia que confirma o descarta la causa: Revisión de los cinco criterios.
- Orden de diagnóstico: Criterios → evidencia → benchmark → anti-patterns → conclusión.

### 23. Correction
- Corrección: Completar la dimensión faltante o declarar información insuficiente.
- Acción concreta: No congelar la herramienta hasta completar evidencia.
- Verificación posterior: Revalidar la ficha.
- Riesgos de la corrección: Retrasa el paso siguiente, pero evita acoplamiento prematuro.

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
- M1 → archivo → sección/tema → concepto: `Módulo_1.../2. Pilar 1 — La Herramienta.md`; `Módulo_1.../5. Recursos adicionales.md` → Cinco criterios; modelos; benchmarks; framework de decisión; anti-patterns. → Tamaño/forma del codebase, lenguaje, privacidad/compliance, presupuesto, estilo; SWE-Bench Verified/Pro, Aider Polyglot, TerminalBench 2.0..
- Concepto → actividad: Comparar candidatas usando los cinco criterios; consultar benchmarks; revisar anti-patterns; formular elección documentada.
- Actividad → paso: M1-P02
- Paso → artefacto: FUTURO: `tool-selection.md`.
- Paso → evidencia: La evidencia actual es documental: M1 y fuentes externas; la ficha de proyecto será futura.
- Paso → validación: Presencia de los cinco criterios y ausencia de una selección basada solo en benchmark.
- Paso → memoria ZIP incremental: ZIP incremental futuro con evaluación y fuentes para P03.
- Paso → siguiente paso: P03 consume las restricciones y capacidades de la herramienta seleccionada.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: ver `knowledge/facts/external-research.md` y `knowledge/references/reference-index.md`; consulta 2026-09-30 para OpenAI Harness, AGENTS.md y Claude Code.

### 26. State
- Estado inicial: P01 planificado, evaluación aún no ejecutada.
- Estado final esperado: Registro de elección reproducible listo para alimentar P03.
- Estado real: PLANIFICADO. No se seleccionó un proveedor/modelo como decisión de Chat 2.
- Qué queda pendiente: Evaluar candidatas en ejecución futura.
- Relación con el siguiente paso: P03 consume las restricciones y capacidades de la herramienta seleccionada.
## Paso 03 — Diseñar la arquitectura de contexto persistente del proyecto

### 1. Identification
- ID del paso: `M1-P03` (03 asignado después de estabilizar el conjunto final).
- Fase: Fase A — Construcción cognitiva del plan
- Subfase: Arquitectura de contexto
- Estado: PLANIFICADO
- Tipo de paso: Diseño de contexto y memoria operativa

### 2. Objective
- Objetivo exacto del paso: Diseñar la arquitectura de contexto persistente del proyecto.

### 3. Direct relation to M1
- Archivo(s) de M1: `Módulo_1.../3. Pilar 2 — El Contexto.md`; `Módulo_1.../1. El modelo mental de los 3 pilares.md`
- Sección(es)/tema(s): Tipos de contexto; contexto persistente; AGENTS.md; alternativas; buenas prácticas.
- Concepto(s) de M1: Persistente, tarea, sesión; instrucciones de repositorio; high-signal context; precedencia.
- Relación directa: Diseña el contexto antes de operar su ventana: qué debe persistir, qué pertenece a la tarea y qué es efímero.

### 4. Prerequisites
- Conocimientos previos: P01/P02 conceptualmente resueltos; comprensión básica de repositorios e instrucciones persistentes.
- Condiciones previas: Definición de qué herramienta será usada en ejecución futura; no requiere código.
- Evidencia o artefactos necesarios: M1 Pilar 2; documentación oficial actual consultada de AGENTS.md y Claude Code como corroboración de mecanismos.

### 5. Dependencies
- Depende de: P01 y P02
- Habilita: P04: higiene de ventana; P05: prompting sobre contexto controlado.
- Tipo de dependencia: Estructural
- Riesgo si se altera el orden: Mezclar estado, conocimiento, tarea y reglas en un único archivo gigante.

### 6. Preparation
- Preparación necesaria: Separar capas de contexto; definir fuente persistente y formato de alto señal; declarar exclusiones.
- Entorno: Futura copia de proyecto.
- Información que debe estar disponible: Reglas de repositorio, contexto operativo, exclusiones y límites de seguridad.

### 7. Files
- Archivos que se leerán: M1 Pilar 2 y recursos relacionados.
- Archivos que se crearán en la ejecución futura: FUTURO: `AGENTS.md` y/o archivo equivalente según herramienta realmente seleccionada.
- Archivos que se modificarían en la ejecución futura: FUTURO: instrucciones de repositorio, si la herramienta lo requiere.
- Ubicación exacta de cada archivo: FUTURO: `<PROJECT_ROOT>/AGENTS.md` o mecanismo equivalente documentado; no se crea en Chat 2.

### 8. Directory structure
```text
<PROJECT_ROOT>/
└── AGENTS.md  # FUTURO; proveedor/herramienta puede cambiar la ubicación.
```

### 9. Required concepts
- Concepto: Tipos de contexto; precedencia; high-signal; diferencia entre persistencia y contexto de tarea.
- Explicación necesaria: Diseña el contexto antes de operar su ventana: qué debe persistir, qué pertenece a la tarea y qué es efímero.
- Nivel requerido para ejecutar el paso: suficiente para aplicar M1 sin implementar capacidades propias de módulos posteriores.

### 10. Commands
```text
find . -maxdepth 2 -name "AGENTS.md" -o -name "CLAUDE.md" | sort
```
FUTURO.
- Ubicación desde la que se ejecuta cada comando: Raíz futura del proyecto.
- Resultado esperado: Detecta mecanismos de instrucciones ya existentes antes de introducir otro.
- Verificación: Comparar resultado con la política de contexto.

### 11. Code
```text
NO SE IMPLEMENTA EL PROYECTO EN CHAT 2.
```
- Propósito: La actividad produce una arquitectura de contexto, no código de negocio.
- Partes relevantes: Persistencia, tarea, sesión, instrucciones y exclusiones.
- Personalización requerida: Adaptar el archivo persistente a la herramienta realmente seleccionada.

### 12. Action
- Acción concreta que se realizará: Clasificar los artefactos por capa de contexto y diseñar el mecanismo persistente de alta señal.
- Orden de ejecución: 1) clasificar; 2) elegir mecanismo; 3) definir contenido; 4) definir exclusiones; 5) revisar precedencia.
- Entrada utilizada: Restricciones de P01/P02 y artefactos de contexto.
- Salida producida: Arquitectura de contexto persistente.

### 13. Reason
- Por qué se realiza esta acción: El Pilar 2 trata el contexto como parte del sistema de ingeniería.
- Qué problema resuelve: Evita contaminación y ambigüedad de instrucciones desde el inicio.
- Por qué corresponde a M1: Es aplicación directa del Pilar 2 sin adelantar M5.

### 14. Expected result
- Resultado esperado: Modelo de contexto con capas, precedencia y contenido de alta señal.
- Estado esperado: Contexto diseñado para operar en P04/P05.
- Evidencia esperada: Esquema y prueba futura de precedencia.
- Memoria incremental del paso: ZIP incremental futuro con arquitectura de contexto.

### 15. Evidence
- Evidencia que demuestra el resultado: La evidencia en Chat 2 es documental; el archivo de proyecto será futuro.
- Fuente de la evidencia: M1 Pilar 2 + AGENTS.md/Claude Code oficiales.
- Cómo se conservará: Persistir esquema y fuente de mecanismo.

### 16. Validation
- Qué se debe verificar: Separación persistente/tarea/sesión; mecanismo de instrucciones; ausencia de secretos.
- Cómo se verifica: Auditar categorías y precedencia.
- Resultado esperado de la validación: PASS si las capas no se mezclan.

### 17. Acceptance criteria
- Criterio 1: Cada artefacto tiene capa de contexto.
- Criterio 2: La fuente persistente y su precedencia están definidas.
- Criterio 3: El diseño evita secretos y estado efímero en instrucciones persistentes.

### 18. Tests
- ID de prueba: Ver T01…T05 dentro del campo; todas están PLANIFICADAS
- Capacidad/subcapacidad cubierta: Persistente, tarea, sesión; instrucciones de repositorio; high-signal context; precedencia.
- Prueba: qué se hará para comprobarla: **T01 — Tipos.** Entrada: lista de artefactos. Resultado: 100% clasificados como persistente/tarea/sesión. PASS: no quedan ambiguos.
**T02 — Instrucciones.** Entrada: borrador de alta señal. Resultado: solo reglas/contexto estable. PASS: no incluye secretos ni histórico efímero.
- Entrada: datos, escenario, estado, archivo o configuración sobre la que se ejecutará: Escenario futuro definido en cada T; ninguna prueba del paso fue ejecutada durante Chat 2.
- Resultado esperado: los resultados observables indicados en cada T; PASS/FAIL determinado por la condición explícita de cada prueba.
- Condición de aprobación: se cumplen las condiciones PASS de todas las pruebas aplicables; `NO APLICA` no se usa para evitar una prueba posible.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Contexto persistente sobredimensionado.
- Cuándo podría aparecer: Cuando instrucciones contienen tareas, histórico o detalle operacional cambiante.
- Síntoma: Cada llamada arrastra ruido innecesario.

### 20. Detection
- Cómo detectar el error: Revisar categorías y longitud del archivo.
- Evidencia del error: Borrador de instrucciones.
- Señal observable: Mezcla de capas.

### 21. Meaning
- Qué significa el error o resultado: La persistencia está usándose como contenedor universal.
- Qué parte del proceso afecta: P03-P05.

### 22. Diagnosis
- Causa probable: No distinguir persistencia de contexto de tarea.
- Evidencia que confirma o descarta la causa: Clasificación por capa.
- Orden de diagnóstico: Contenido → permanencia → frecuencia → ubicación.

### 23. Correction
- Corrección: Mover contenido a la capa correcta.
- Acción concreta: Reubicar en el artefacto futuro correspondiente.
- Verificación posterior: Revisar que las instrucciones permanezcan de alta señal.
- Riesgos de la corrección: Cambiar ubicación puede requerir actualizar referencias.

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
- M1 → archivo → sección/tema → concepto: `Módulo_1.../3. Pilar 2 — El Contexto.md`; `Módulo_1.../1. El modelo mental de los 3 pilares.md` → Tipos de contexto; contexto persistente; AGENTS.md; alternativas; buenas prácticas. → Persistente, tarea, sesión; instrucciones de repositorio; high-signal context; precedencia..
- Concepto → actividad: Clasificar los artefactos por capa de contexto y diseñar el mecanismo persistente de alta señal.
- Actividad → paso: M1-P03
- Paso → artefacto: FUTURO: `AGENTS.md` y/o archivo equivalente según herramienta realmente seleccionada.
- Paso → evidencia: La evidencia en Chat 2 es documental; el archivo de proyecto será futuro.
- Paso → validación: Separación persistente/tarea/sesión; mecanismo de instrucciones; ausencia de secretos.
- Paso → memoria ZIP incremental: ZIP incremental futuro con arquitectura de contexto.
- Paso → siguiente paso: P04 depende de esta arquitectura.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: ver `knowledge/facts/external-research.md` y `knowledge/references/reference-index.md`; consulta 2026-09-30 para OpenAI Harness, AGENTS.md y Claude Code.

### 26. State
- Estado inicial: P01/P02 planificados.
- Estado final esperado: Arquitectura de contexto preparada para ejecución futura.
- Estado real: PLANIFICADO; no se creó AGENTS.md en el proyecto.
- Qué queda pendiente: Aplicar el diseño a la herramienta elegida.
- Relación con el siguiente paso: P04 depende de esta arquitectura.
## Paso 04 — Gestionar la ventana de contexto y prevenir context rot

### 1. Identification
- ID del paso: `M1-P04` (04 asignado después de estabilizar el conjunto final).
- Fase: Fase A — Construcción cognitiva del plan
- Subfase: Operación de contexto
- Estado: PLANIFICADO
- Tipo de paso: Operación iterativa de contexto

### 2. Objective
- Objetivo exacto del paso: Gestionar la ventana de contexto y prevenir context rot.

### 3. Direct relation to M1
- Archivo(s) de M1: `Módulo_1.../3. Pilar 2 — El Contexto.md`
- Sección(es)/tema(s): Context rot; mecanismos; reglas 50/70/90; Write/Select/Compress/Isolate; kit operativo.
- Concepto(s) de M1: Degradación por contexto; umbrales; selección; escritura; compresión; aislamiento; reset/compactación.
- Relación directa: Convierte el diseño de contexto de P03 en una práctica recurrente para mantener señal y evitar degradación.

### 4. Prerequisites
- Conocimientos previos: P03 diseñado; comprensión de que contexto útil y tamaño de ventana deben gestionarse.
- Condiciones previas: Sesión futura que permita observar crecimiento/ruido; no se ejecuta ahora.
- Evidencia o artefactos necesarios: M1 Pilar 2 completo.

### 5. Dependencies
- Depende de: P03
- Habilita: P05 y P07; gestión repetible de sesiones.
- Tipo de dependencia: Operacional/iterativo
- Riesgo si se altera el orden: Dejar crecer el contexto hasta que el modelo pierda foco.

### 6. Preparation
- Preparación necesaria: Definir señales de ruido; aplicar 50/70/90; usar Write/Select/Compress/Isolate según condición.
- Entorno: Futura sesión de herramienta.
- Información que debe estar disponible: Estado de ventana, señal de tarea y mecanismos disponibles por herramienta.

### 7. Files
- Archivos que se leerán: M1 Pilar 2.
- Archivos que se crearán en la ejecución futura: FUTURO: `context-operations.md`.
- Archivos que se modificarían en la ejecución futura: FUTURO: protocolo de operación de contexto.
- Ubicación exacta de cada archivo: FUTURO: `<PROJECT_ROOT>/docs/ai-engineering/context-operations.md`.

### 8. Directory structure
```text
<PROJECT_ROOT>/
└── docs/ai-engineering/
    └── context-operations.md  # FUTURO
```

### 9. Required concepts
- Concepto: Context rot; 50/70/90; Write/Select/Compress/Isolate; compact/reset; context-as-code.
- Explicación necesaria: Convierte el diseño de contexto de P03 en una práctica recurrente para mantener señal y evitar degradación.
- Nivel requerido para ejecutar el paso: suficiente para aplicar M1 sin implementar capacidades propias de módulos posteriores.

### 10. Commands
```text
# FUTURO: usar el mecanismo de compactación/reset de la herramienta seleccionada.
```
El comando exacto debe verificarse en documentación vigente al ejecutar el paso; no fue ejecutado en Chat 2.
- Ubicación desde la que se ejecuta cada comando: Dentro de la sesión de la herramienta futura.
- Resultado esperado: La acción reduce o reestructura contexto sin perder el objetivo.
- Verificación: Revisar que la tarea sigue alineada y que el ruido fue reducido.

### 11. Code
```text
NO SE EJECUTA CÓDIGO DEL PROYECTO EN CHAT 2.
```
- Propósito: Definir el protocolo operacional de contexto.
- Partes relevantes: Cuatro mecanismos y reglas de ventana.
- Personalización requerida: Ajustar el comando de compactación/reset a la herramienta real.

### 12. Action
- Acción concreta que se realizará: Detectar rot; escoger Write/Select/Compress/Isolate; compactar/aislar/resetear; verificar recuperación de señal.
- Orden de ejecución: 1) detectar; 2) elegir mecanismo; 3) aplicar; 4) verificar; 5) registrar.
- Entrada utilizada: Estado de sesión y contenido relevante.
- Salida producida: Contexto operativo controlado.

### 13. Reason
- Por qué se realiza esta acción: M1 trata el control del contexto como trabajo iterativo, no como configuración estática.
- Qué problema resuelve: Evita degradación y retrabajo por sesiones saturadas.
- Por qué corresponde a M1: Corresponde directamente a Pilar 2.

### 14. Expected result
- Resultado esperado: Protocolo explícito y probado en escenarios sintéticos futuros.
- Estado esperado: Ventana operable bajo reglas preventivas.
- Evidencia esperada: Pruebas W/S/C/I y 50/70/90.
- Memoria incremental del paso: ZIP incremental futuro con el protocolo y evidencia.

### 15. Evidence
- Evidencia que demuestra el resultado: No se ejecutaron sesiones reales del proyecto; la validación es futura.
- Fuente de la evidencia: M1 Pilar 2.
- Cómo se conservará: Guardar escenarios y resultados en el artefacto de operación.

### 16. Validation
- Qué se debe verificar: Mecanismos W/S/C/I, umbrales y recuperación de foco.
- Cómo se verifica: Ejecutar escenarios sintéticos y revisar antes/después.
- Resultado esperado de la validación: PASS cuando cada mecanismo y umbral tiene respuesta.

### 17. Acceptance criteria
- Criterio 1: W/S/C/I se aplican a escenarios distintos.
- Criterio 2: 50/70/90 produce acción preventiva correspondiente.
- Criterio 3: El contexto recupera el objetivo sin reintroducir ruido.

### 18. Tests
- ID de prueba: Ver T01…T05 dentro del campo; todas están PLANIFICADAS
- Capacidad/subcapacidad cubierta: Degradación por contexto; umbrales; selección; escritura; compresión; aislamiento; reset/compactación.
- Prueba: qué se hará para comprobarla: **T01 — W/S/C/I.** Entrada: cuatro contextos sintéticos. Resultado: cada mecanismo aplicado a su caso. PASS: 4/4.
**T02 — 50/70/90.** Entrada: sesión con crecimiento 50%, 70%, 90%. Resultado: acción preventiva en cada umbral. PASS: ningún umbral sin acción.
**T03 — Context rot.** Entrada: sesión contaminada. Resultado: recuperación de foco. PASS: objetivo se mantiene y ruido disminuye.
- Entrada: datos, escenario, estado, archivo o configuración sobre la que se ejecutará: Escenario futuro definido en cada T; ninguna prueba del paso fue ejecutada durante Chat 2.
- Resultado esperado: los resultados observables indicados en cada T; PASS/FAIL determinado por la condición explícita de cada prueba.
- Condición de aprobación: se cumplen las condiciones PASS de todas las pruebas aplicables; `NO APLICA` no se usa para evitar una prueba posible.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Context rot no detectado.
- Cuándo podría aparecer: Cuando la sesión acumula información irrelevante/excesiva.
- Síntoma: Respuestas se desvían o pierden precisión.

### 20. Detection
- Cómo detectar el error: Comparar objetivo con contenido dominante.
- Evidencia del error: Estado de la sesión y artefactos seleccionados.
- Señal observable: Desalineación entre contexto y tarea.

### 21. Meaning
- Qué significa el error o resultado: La higiene de contexto falló.
- Qué parte del proceso afecta: Prompting y tool use.

### 22. Diagnosis
- Causa probable: No activar Write/Select/Compress/Isolate a tiempo.
- Evidencia que confirma o descarta la causa: Simulación de ventana y revisión de señal.
- Orden de diagnóstico: Volumen → relevancia → mecanismo → recuperación.

### 23. Correction
- Corrección: Aplicar mecanismo correcto y, si procede, reset/compactación.
- Acción concreta: Corregir el protocolo futuro.
- Verificación posterior: Repetir escenario y comprobar recuperación.
- Riesgos de la corrección: Un reset puede perder información si no se preservó lo esencial.

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
- M1 → archivo → sección/tema → concepto: `Módulo_1.../3. Pilar 2 — El Contexto.md` → Context rot; mecanismos; reglas 50/70/90; Write/Select/Compress/Isolate; kit operativo. → Degradación por contexto; umbrales; selección; escritura; compresión; aislamiento; reset/compactación..
- Concepto → actividad: Detectar rot; escoger Write/Select/Compress/Isolate; compactar/aislar/resetear; verificar recuperación de señal.
- Actividad → paso: M1-P04
- Paso → artefacto: FUTURO: `context-operations.md`.
- Paso → evidencia: No se ejecutaron sesiones reales del proyecto; la validación es futura.
- Paso → validación: Mecanismos W/S/C/I, umbrales y recuperación de foco.
- Paso → memoria ZIP incremental: ZIP incremental futuro con el protocolo y evidencia.
- Paso → siguiente paso: P05 usa esta higiene para diseñar prompts sobre contexto bajo control.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: ver `knowledge/facts/external-research.md` y `knowledge/references/reference-index.md`; consulta 2026-09-30 para OpenAI Harness, AGENTS.md y Claude Code.

### 26. State
- Estado inicial: P03 diseñado; operación no ejecutada.
- Estado final esperado: Protocolo listo para ejecución futura.
- Estado real: PLANIFICADO.
- Qué queda pendiente: Aplicar a sesiones reales al ejecutar M1.
- Relación con el siguiente paso: P05 usa esta higiene para diseñar prompts sobre contexto bajo control.
## Paso 05 — Diseñar y aplicar prompting fundamental para trabajo de ingeniería

### 1. Identification
- ID del paso: `M1-P05` (05 asignado después de estabilizar el conjunto final).
- Fase: Fase A — Construcción cognitiva del plan
- Subfase: Prompting fundamental
- Estado: PLANIFICADO
- Tipo de paso: Diseño de instrucciones verificables

### 2. Objective
- Objetivo exacto del paso: Diseñar y aplicar prompting fundamental para trabajo de ingeniería.

### 3. Direct relation to M1
- Archivo(s) de M1: `Módulo_1.../4. Pilar 3 — El Prompt + Integración.md`
- Sección(es)/tema(s): Anatomía del prompt; criterios de éxito; restricciones; recursos; salida; aclaración; anti-patterns y modos.
- Concepto(s) de M1: Rol/contexto, objetivo, success criteria, constraints, resources, output format, clarification; vaguedad, mega-prompt, tareas mixtas y criterios ausentes.
- Relación directa: Transforma una tarea ya caracterizada y contextualizada en una instrucción ejecutable y evaluable.

### 4. Prerequisites
- Conocimientos previos: P03 y P04 conceptualizados; objetivo y contexto de tarea disponibles.
- Condiciones previas: Tarea futura concreta; no se ejecuta el prompt de producto durante Chat 2.
- Evidencia o artefactos necesarios: M1 Pilar 3.

### 5. Dependencies
- Depende de: P03,P04
- Habilita: P06 y P07
- Tipo de dependencia: Instrumental
- Riesgo si se altera el orden: Pedir una tarea vaga o intentar resolver un epic completo con un mega-prompt.

### 6. Preparation
- Preparación necesaria: Elegir modo; redactar contexto; objetivo; success criteria; constraints; resources; output; manejo de aclaración; anti-pattern review.
- Entorno: Herramienta futura con contexto previamente controlado.
- Información que debe estar disponible: Tarea, artefactos, restricciones y forma de aceptar/rechazar el resultado.

### 7. Files
- Archivos que se leerán: M1 Pilar 3 y recursos.
- Archivos que se crearán en la ejecución futura: FUTURO: `prompt-kit.md`.
- Archivos que se modificarían en la ejecución futura: FUTURO: versiones del prompt operacional.
- Ubicación exacta de cada archivo: FUTURO: `<PROJECT_ROOT>/docs/ai-engineering/prompt-kit.md`.

### 8. Directory structure
```text
<PROJECT_ROOT>/
└── docs/ai-engineering/
    └── prompt-kit.md  # FUTURO
```

### 9. Required concepts
- Concepto: Anatomía completa y anti-patterns de M1; prompting como parte integrada con tool/context.
- Explicación necesaria: Transforma una tarea ya caracterizada y contextualizada en una instrucción ejecutable y evaluable.
- Nivel requerido para ejecutar el paso: suficiente para aplicar M1 sin implementar capacidades propias de módulos posteriores.

### 10. Commands
```text
# FUTURO: ejecutar el prompt en la herramienta seleccionada.
```
No se ejecuta en Chat 2.
- Ubicación desde la que se ejecuta cada comando: Dentro de la herramienta futura.
- Resultado esperado: El comando/entrada produce un resultado evaluable contra los success criteria.
- Verificación: Comprobar los criterios de éxito y la salida.

### 11. Code
```text
NO SE CREA NI SE EJECUTA CÓDIGO DEL PROYECTO EN CHAT 2.
```
- Propósito: El artefacto es el prompt operacional.
- Partes relevantes: Contexto/rol, objetivo, éxito, constraints, resources, output, aclaración.
- Personalización requerida: Adaptar a la tarea real y a la herramienta.

### 12. Action
- Acción concreta que se realizará: Construir prompts completos y revisar anti-patterns antes de ejecutarlos en el futuro.
- Orden de ejecución: 1) modo; 2) contexto; 3) objetivo; 4) éxito; 5) constraints; 6) resources; 7) output; 8) aclaración; 9) revisión.
- Entrada utilizada: Tarea y contexto controlados.
- Salida producida: Prompt operativo verificable.

### 13. Reason
- Por qué se realiza esta acción: M1 presenta el prompt como una interfaz de trabajo verificable, no como texto libre.
- Qué problema resuelve: Evita ambigüedad y reduce iteraciones por instrucciones incompletas.
- Por qué corresponde a M1: Es el núcleo práctico del Pilar 3.

### 14. Expected result
- Resultado esperado: Prompt con estructura y criterios de aceptación observables.
- Estado esperado: Listo para aplicar un patrón de ejecución.
- Evidencia esperada: Ejemplos y revisión anti-pattern.
- Memoria incremental del paso: ZIP incremental futuro con prompts y criterios.

### 15. Evidence
- Evidencia que demuestra el resultado: Solo diseño en Chat 2; ningún prompt se ejecutó contra el proyecto externo.
- Fuente de la evidencia: M1 Pilar 3.
- Cómo se conservará: Versionar prompt y checklist en el proyecto futuro.

### 16. Validation
- Qué se debe verificar: Completitud de anatomy y detección de anti-patterns.
- Cómo se verifica: Revisión campo por campo y cinco defectos controlados.
- Resultado esperado de la validación: PASS con campos esenciales presentes.

### 17. Acceptance criteria
- Criterio 1: Success criteria observables.
- Criterio 2: Constraints y resources explícitos.
- Criterio 3: Output y aclaración definidos; no mega-prompt innecesario.

### 18. Tests
- ID de prueba: Ver T01…T05 dentro del campo; todas están PLANIFICADAS
- Capacidad/subcapacidad cubierta: Rol/contexto, objetivo, success criteria, constraints, resources, output format, clarification; vaguedad, mega-prompt, tareas mixtas y criterios ausentes.
- Prueba: qué se hará para comprobarla: **T01 — Anatomy.** Entrada: tarea de debugging. Resultado: prompt completo. PASS: todos los elementos obligatorios están presentes.
**T02 — Anti-patterns.** Entrada: cinco prompts defectuosos (vago, mega, mixed, sin éxito, repetición de AGENTS). Resultado: cada defecto identificado. PASS: 100% detectados.
- Entrada: datos, escenario, estado, archivo o configuración sobre la que se ejecutará: Escenario futuro definido en cada T; ninguna prueba del paso fue ejecutada durante Chat 2.
- Resultado esperado: los resultados observables indicados en cada T; PASS/FAIL determinado por la condición explícita de cada prueba.
- Condición de aprobación: se cumplen las condiciones PASS de todas las pruebas aplicables; `NO APLICA` no se usa para evitar una prueba posible.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Prompt ambiguo.
- Cuándo podría aparecer: Cuando no existe condición observable de éxito.
- Síntoma: No puede determinarse PASS/FAIL.

### 20. Detection
- Cómo detectar el error: Revisar anatomy y success criteria.
- Evidencia del error: Prompt y checklist.
- Señal observable: Criterio de éxito ausente.

### 21. Meaning
- Qué significa el error o resultado: La instrucción no delimita el resultado.
- Qué parte del proceso afecta: P05-P07.

### 22. Diagnosis
- Causa probable: Anatomía incompleta o tarea mixta.
- Evidencia que confirma o descarta la causa: Checklist de M1.
- Orden de diagnóstico: Objetivo → éxito → constraints → resources → output.

### 23. Correction
- Corrección: Completar la anatomy o solicitar aclaración antes de ejecutar.
- Acción concreta: Reescribir el prompt futuro.
- Verificación posterior: Volver a pasar la revisión.
- Riesgos de la corrección: Una aclaración adicional puede introducir una iteración, pero es preferible a ejecutar ambiguamente.

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
- M1 → archivo → sección/tema → concepto: `Módulo_1.../4. Pilar 3 — El Prompt + Integración.md` → Anatomía del prompt; criterios de éxito; restricciones; recursos; salida; aclaración; anti-patterns y modos. → Rol/contexto, objetivo, success criteria, constraints, resources, output format, clarification; vaguedad, mega-prompt, tareas mixtas y criterios ausentes..
- Concepto → actividad: Construir prompts completos y revisar anti-patterns antes de ejecutarlos en el futuro.
- Actividad → paso: M1-P05
- Paso → artefacto: FUTURO: `prompt-kit.md`.
- Paso → evidencia: Solo diseño en Chat 2; ningún prompt se ejecutó contra el proyecto externo.
- Paso → validación: Completitud de anatomy y detección de anti-patterns.
- Paso → memoria ZIP incremental: ZIP incremental futuro con prompts y criterios.
- Paso → siguiente paso: P06 consume el prompt y la caracterización para elegir patrón.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: ver `knowledge/facts/external-research.md` y `knowledge/references/reference-index.md`; consulta 2026-09-30 para OpenAI Harness, AGENTS.md y Claude Code.

### 26. State
- Estado inicial: P03/P04 planificados.
- Estado final esperado: Prompt operativo futuro listo.
- Estado real: PLANIFICADO.
- Qué queda pendiente: Aplicar en ejecución real de M1.
- Relación con el siguiente paso: P06 consume el prompt y la caracterización para elegir patrón.
## Paso 06 — Aplicar patrones de ejecución de coding asistido por IA

### 1. Identification
- ID del paso: `M1-P06` (06 asignado después de estabilizar el conjunto final).
- Fase: Fase A — Construcción cognitiva del plan
- Subfase: Patrones de ejecución
- Estado: PLANIFICADO
- Tipo de paso: Selección y ejecución de patrón

### 2. Objective
- Objetivo exacto del paso: Aplicar patrones de ejecución de coding asistido por IA.

### 3. Direct relation to M1
- Archivo(s) de M1: `Módulo_1.../4. Pilar 3 — El Prompt + Integración.md`
- Sección(es)/tema(s): Spec-driven preview; plan-then-execute; test-first; refactor with anchors; critic loops.
- Concepto(s) de M1: Cinco patrones y condición de uso.
- Relación directa: Conecta la tarea/prompt con una forma de ejecutar coding que preserve checkpoints y validación, sin convertir M1 en M2, M7 o M11 completos.

### 4. Prerequisites
- Conocimientos previos: P01 y P05; comprensión de que patrón depende del tipo de tarea.
- Condiciones previas: Escenarios de coding futuros; no se modifica código ahora.
- Evidencia o artefactos necesarios: M1 Pilar 3.

### 5. Dependencies
- Depende de: P01,P05
- Habilita: P07
- Tipo de dependencia: Operacional/selección
- Riesgo si se altera el orden: Usar siempre un mismo patrón o adelantar prácticas de módulos posteriores.

### 6. Preparation
- Preparación necesaria: Mapear tarea a patrón; definir entrada, salida y validación.
- Entorno: Futura herramienta de coding.
- Información que debe estar disponible: Tipo de tarea, restricciones, prompt y criterio de éxito.

### 7. Files
- Archivos que se leerán: M1 Pilar 3.
- Archivos que se crearán en la ejecución futura: FUTURO: `coding-execution-patterns.md`.
- Archivos que se modificarían en la ejecución futura: FUTURO: ejemplos/registro de uso de patrones.
- Ubicación exacta de cada archivo: FUTURO: `<PROJECT_ROOT>/docs/ai-engineering/coding-execution-patterns.md`.

### 8. Directory structure
```text
<PROJECT_ROOT>/
└── docs/ai-engineering/
    └── coding-execution-patterns.md  # FUTURO
```

### 9. Required concepts
- Concepto: Los cinco patrones y sus condiciones de uso; diferencia entre plan/patrón y módulos posteriores.
- Explicación necesaria: Conecta la tarea/prompt con una forma de ejecutar coding que preserve checkpoints y validación, sin convertir M1 en M2, M7 o M11 completos.
- Nivel requerido para ejecutar el paso: suficiente para aplicar M1 sin implementar capacidades propias de módulos posteriores.

### 10. Commands
```text
# FUTURO: aplicar el patrón en la herramienta seleccionada.
```
Sintaxis exacta por verificar en la ejecución futura; no se ejecutó en Chat 2.
- Ubicación desde la que se ejecuta cada comando: Herramienta futura.
- Resultado esperado: La ejecución mantiene checkpoints y criterios del patrón.
- Verificación: Comparar resultado con la condición de uso del patrón.

### 11. Code
```text
NO SE CREA NI EJECUTA CÓDIGO EN CHAT 2.
```
- Propósito: Documentar cómo aplicar cinco patrones.
- Partes relevantes: Preview, plan, test, anchors, critic.
- Personalización requerida: Adaptar el comando y secuencia a la herramienta actual.

### 12. Action
- Acción concreta que se realizará: Seleccionar un patrón según la tarea y definir cómo se comprobará.
- Orden de ejecución: 1) caracterizar; 2) seleccionar patrón; 3) preparar entrada; 4) ejecutar futuro; 5) verificar.
- Entrada utilizada: Escenario y prompt.
- Salida producida: Playbook de ejecución por patrón.

### 13. Reason
- Por qué se realiza esta acción: M1 propone varios patrones porque no existe una única forma profesional de ejecutar coding asistido.
- Qué problema resuelve: Evita megatareas monolíticas y ausencia de checkpoints.
- Por qué corresponde a M1: Directamente derivado del Pilar 3.

### 14. Expected result
- Resultado esperado: Cinco patrones con criterio de uso, entrada, salida y validación.
- Estado esperado: Playbook reutilizable.
- Evidencia esperada: Cinco pruebas futuras.
- Memoria incremental del paso: ZIP incremental futuro con playbook y resultados.

### 15. Evidence
- Evidencia que demuestra el resultado: Planificado, no ejecutado.
- Fuente de la evidencia: M1 Pilar 3.
- Cómo se conservará: Persistir relación patrón→escenario→resultado.

### 16. Validation
- Qué se debe verificar: Los cinco patrones deben estar explícitos y seleccionables por condición.
- Cómo se verifica: Probar un escenario por patrón y un mismatch.
- Resultado esperado de la validación: PASS con 5/5 patrones y cambio justificable.

### 17. Acceptance criteria
- Criterio 1: Cada patrón tiene condición de uso.
- Criterio 2: Cada patrón tiene entrada/salida y validación.
- Criterio 3: No se usa un patrón como sustituto de un módulo posterior.

### 18. Tests
- ID de prueba: Ver T01…T05 dentro del campo; todas están PLANIFICADAS
- Capacidad/subcapacidad cubierta: Cinco patrones y condición de uso.
- Prueba: qué se hará para comprobarla: **T01 — Cinco patrones.** Entrada: cinco escenarios sintéticos. Resultado: cada escenario selecciona un patrón. PASS: 5/5 con justificación.
**T02 — Mismatch.** Entrada: escenario con patrón inadecuado. Resultado: desajuste detectado y patrón alternativo propuesto. PASS: cambio justificado.
- Entrada: datos, escenario, estado, archivo o configuración sobre la que se ejecutará: Escenario futuro definido en cada T; ninguna prueba del paso fue ejecutada durante Chat 2.
- Resultado esperado: los resultados observables indicados en cada T; PASS/FAIL determinado por la condición explícita de cada prueba.
- Condición de aprobación: se cumplen las condiciones PASS de todas las pruebas aplicables; `NO APLICA` no se usa para evitar una prueba posible.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Patrón de ejecución incorrecto.
- Cuándo podría aparecer: Cuando la forma de tarea no coincide con el patrón elegido.
- Síntoma: Checkpoint/validación insuficiente.

### 20. Detection
- Cómo detectar el error: Comparar condición de uso del patrón con tarea.
- Evidencia del error: Registro de selección.
- Señal observable: Mismatched pattern.

### 21. Meaning
- Qué significa el error o resultado: El flujo elegido no es adecuado.
- Qué parte del proceso afecta: P06 y resultado de coding.

### 22. Diagnosis
- Causa probable: Selección por costumbre.
- Evidencia que confirma o descarta la causa: Volver al criterio de uso de M1.
- Orden de diagnóstico: Tarea → condición del patrón → entrada → validación.

### 23. Correction
- Corrección: Cambiar de patrón antes de ejecutar.
- Acción concreta: Actualizar playbook futuro.
- Verificación posterior: Repetir escenario de validación.
- Riesgos de la corrección: Puede aumentar una iteración, pero evita ejecución inadecuada.

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
- M1 → archivo → sección/tema → concepto: `Módulo_1.../4. Pilar 3 — El Prompt + Integración.md` → Spec-driven preview; plan-then-execute; test-first; refactor with anchors; critic loops. → Cinco patrones y condición de uso..
- Concepto → actividad: Seleccionar un patrón según la tarea y definir cómo se comprobará.
- Actividad → paso: M1-P06
- Paso → artefacto: FUTURO: `coding-execution-patterns.md`.
- Paso → evidencia: Planificado, no ejecutado.
- Paso → validación: Los cinco patrones deben estar explícitos y seleccionables por condición.
- Paso → memoria ZIP incremental: ZIP incremental futuro con playbook y resultados.
- Paso → siguiente paso: P07 integra los patrones en A-E.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: ver `knowledge/facts/external-research.md` y `knowledge/references/reference-index.md`; consulta 2026-09-30 para OpenAI Harness, AGENTS.md y Claude Code.

### 26. State
- Estado inicial: P05 planificado.
- Estado final esperado: Cinco patrones documentados y listos para aplicar.
- Estado real: PLANIFICADO.
- Qué queda pendiente: Ensayar patrones en ejecución futura.
- Relación con el siguiente paso: P07 integra los patrones en A-E.
## Paso 07 — Integrar los tres pilares y validar los cinco casos canónicos de M1

### 1. Identification
- ID del paso: `M1-P07` (07 asignado después de estabilizar el conjunto final).
- Fase: Fase B — Auditoría semántica y reparación
- Subfase: Integración y validación final de M1
- Estado: PLANIFICADO
- Tipo de paso: Integración, refutación y gate de calidad

### 2. Objective
- Objetivo exacto del paso: Integrar los tres pilares y validar los cinco casos canónicos de M1.

### 3. Direct relation to M1
- Archivo(s) de M1: Los cinco archivos de M1: modelo mental, Pilar 1, Pilar 2, Pilar 3 e Recursos adicionales.
- Sección(es)/tema(s): Integración de pilares; casos A-E: gran refactor, greenfield feature, debugging, exploration, code review.
- Concepto(s) de M1: Tool + context + prompt; patrones; evidencia; validación; anti-patterns.
- Relación directa: Demuestra que M1 funciona como un sistema integrado: cada caso selecciona modo/herramienta/contexto/prompt/patrón y conserva resultado/evidencia/validación.

### 4. Prerequisites
- Conocimientos previos: P01-P06 estabilizados y auditados.
- Condiciones previas: No requiere ejecutar el proyecto; puede validarse con escenarios sintéticos y documentación.
- Evidencia o artefactos necesarios: M1 completo; matrices y pruebas previas.

### 5. Dependencies
- Depende de: P01-P06
- Habilita: Baseline M1 para fases posteriores; no ejecuta módulos posteriores.
- Tipo de dependencia: Integración/validación
- Riesgo si se altera el orden: Dejar un caso con cobertura nominal o esconder información práctica en matrices.

### 6. Preparation
- Preparación necesaria: Aplicar prueba anti-compresión, anti-fragmentación, cobertura y trazabilidad a A-E.
- Entorno: Staging/documentación futura.
- Información que debe estar disponible: Resultados de P01-P06 y cinco escenarios canónicos.

### 7. Files
- Archivos que se leerán: Los cinco archivos M1 y la evidencia derivada de P01-P06.
- Archivos que se crearán en la ejecución futura: FUTURO: baseline M1 y matriz de casos; en Chat 2 la matriz ya vive en `M1_PLAN.md`.
- Archivos que se modificarían en la ejecución futura: `M1_PLAN.md` puede modificarse solo durante el diseño/auditoría de Chat 2; el proyecto externo no se modifica.
- Ubicación exacta de cada archivo: `memory-repo/chats/chat-002/M1_PLAN.md` en Chat 2; artefactos de proyecto solo FUTUROS.

### 8. Directory structure
```text
memory-repo/chats/chat-002/
├── M1_PLAN.md
├── META.md
├── transcript.md
└── HANDOFF.md
```

### 9. Required concepts
- Concepto: Integración de los tres pilares y cinco casos A-E; refutación contra cobertura nominal, megapropting y fragmentación.
- Explicación necesaria: Demuestra que M1 funciona como un sistema integrado: cada caso selecciona modo/herramienta/contexto/prompt/patrón y conserva resultado/evidencia/validación.
- Nivel requerido para ejecutar el paso: suficiente para aplicar M1 sin implementar capacidades propias de módulos posteriores.

### 10. Commands
```text
# No aplica un comando de proyecto: la actividad de Chat 2 es planificación/auditoría.
```
- Ubicación desde la que se ejecuta cada comando: Staging de memoria.
- Resultado esperado: No se inicia el proyecto objetivo.
- Verificación: Auditar estructura, campos, matrices y gates.

### 11. Code
```text
NO SE EJECUTA EL PROYECTO NI SE CREA CÓDIGO PARA DEMOSTRAR AVANCE.
```
- Propósito: El artefacto es el plan congelado y su evidencia documental.
- Partes relevantes: Casos A-E; integración tool/context/prompt; patrón; resultado y validación.
- Personalización requerida: Futuro: sustituir escenarios sintéticos por escenarios del proyecto sin cambiar el método.

### 12. Action
- Acción concreta que se realizará: Auditar cada caso A-E; comprobar cobertura y profundidad; reparar defectos; congelar plan.
- Orden de ejecución: 1) revisar A; 2) B; 3) C; 4) D; 5) E; 6) refutar plan; 7) congelar.
- Entrada utilizada: P01-P06 y contenido completo de M1.
- Salida producida: Baseline M1 aplicado y plan final congelado.

### 13. Reason
- Por qué se realiza esta acción: La integración evita que los tres pilares se conviertan en listas separadas.
- Qué problema resuelve: Detecta huecos semánticos que una matriz nominal puede ocultar.
- Por qué corresponde a M1: Es la aplicación final de la integración de M1.

### 14. Expected result
- Resultado esperado: Cinco casos completos y coherentes con tool/context/prompt/pattern.
- Estado esperado: PLANIFICADO y listo para ejecución futura.
- Evidencia esperada: Casos y resultados de auditoría en M1_PLAN/transcript.
- Memoria incremental del paso: ZIP incremental futuro de memoria cuando P07 sea ejecutado; no se genera durante esta sesión.

### 15. Evidence
- Evidencia que demuestra el resultado: La evidencia actual es el plan congelado y las fuentes; no hay ejecución del proyecto.
- Fuente de la evidencia: M1 cinco archivos; fuentes externas R01 y documentación actual.
- Cómo se conservará: M1_PLAN, transcript, handoff y memoria acumulativa futura.

### 16. Validation
- Qué se debe verificar: Cobertura A-E, integración de tres pilares, ausencia de mención nominal y todos los gates.
- Cómo se verifica: Auditoría estructural + semántica; revisar cada campo y cada caso.
- Resultado esperado de la validación: PASS con todos los gates en PASS.

### 17. Acceptance criteria
- Criterio 1: A-E cubiertos con tool/context/prompt.
- Criterio 2: Cada caso tiene patrón, resultado, evidencia y validación.
- Criterio 3: No quedan capacidades prácticas de M1 solo en una matriz o resumen.

### 18. Tests
- ID de prueba: Ver T01…T05 dentro del campo; todas están PLANIFICADAS
- Capacidad/subcapacidad cubierta: Tool + context + prompt; patrones; evidencia; validación; anti-patterns.
- Prueba: qué se hará para comprobarla: **T01 — Caso A, gran refactor.** Entrada: codebase futuro + restricción de regresión. Resultado: modo/herramienta/context/prompt/patrón y validación completos. PASS: trazabilidad total.
**T02 — Caso B, greenfield feature.** Entrada: feature futura. Resultado: flujo completo. PASS: salida y aceptación definidas.
**T03 — Caso C, debugging.** Entrada: fallo reproducible futuro. Resultado: hipótesis/validación bajo contexto y critic/test pattern. PASS: resultado verificable.
**T04 — Caso D, exploration.** Entrada: pregunta técnica. Resultado: exploración delimitada sin implementar innecesariamente. PASS: se distingue exploración de implementación.
**T05 — Caso E, code review.** Entrada: cambio futuro. Resultado: hallazgos trazables sin inventarlos. PASS: toda observación apunta a evidencia.
- Entrada: datos, escenario, estado, archivo o configuración sobre la que se ejecutará: Escenario futuro definido en cada T; ninguna prueba del paso fue ejecutada durante Chat 2.
- Resultado esperado: los resultados observables indicados en cada T; PASS/FAIL determinado por la condición explícita de cada prueba.
- Condición de aprobación: se cumplen las condiciones PASS de todas las pruebas aplicables; `NO APLICA` no se usa para evitar una prueba posible.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Hueco de integración o cobertura nominal.
- Cuándo podría aparecer: Cuando un caso usa un pilar solo como palabra paraguas.
- Síntoma: Matriz parece completa pero no explica ejecución.

### 20. Detection
- Cómo detectar el error: Auditar cada caso contra los 26 campos y el inventario de M1.
- Evidencia del error: M1_PLAN y matriz de cobertura.
- Señal observable: Capacidad sin actividad o validación.

### 21. Meaning
- Qué significa el error o resultado: La aplicación práctica de M1 es insuficiente.
- Qué parte del proceso afecta: Plan completo.

### 22. Diagnosis
- Causa probable: Sobre-compresión o dependencia de resúmenes.
- Evidencia que confirma o descarta la causa: Prueba anti-compresión y trazabilidad M1→actividad→paso→artefacto→validación.
- Orden de diagnóstico: Cobertura → profundidad → independencia → integración → trazabilidad.

### 23. Correction
- Corrección: Expandir el paso afectado o separar solo si existe unidad profesional independiente.
- Acción concreta: Reparar M1_PLAN y reauditar.
- Verificación posterior: Volver a ejecutar ambas capas de auditoría.
- Riesgos de la corrección: Modificar fronteras puede cambiar N; repetir pruebas hasta estabilización.

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
- M1 → archivo → sección/tema → concepto: Los cinco archivos de M1: modelo mental, Pilar 1, Pilar 2, Pilar 3 e Recursos adicionales. → Integración de pilares; casos A-E: gran refactor, greenfield feature, debugging, exploration, code review. → Tool + context + prompt; patrones; evidencia; validación; anti-patterns..
- Concepto → actividad: Auditar cada caso A-E; comprobar cobertura y profundidad; reparar defectos; congelar plan.
- Actividad → paso: M1-P07
- Paso → artefacto: FUTURO: baseline M1 y matriz de casos; en Chat 2 la matriz ya vive en `M1_PLAN.md`.
- Paso → evidencia: La evidencia actual es el plan congelado y las fuentes; no hay ejecución del proyecto.
- Paso → validación: Cobertura A-E, integración de tres pilares, ausencia de mención nominal y todos los gates.
- Paso → memoria ZIP incremental: ZIP incremental futuro de memoria cuando P07 sea ejecutado; no se genera durante esta sesión.
- Paso → siguiente paso: El plan alimenta la continuidad; no constituye ejecución de módulos posteriores.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: ver `knowledge/facts/external-research.md` y `knowledge/references/reference-index.md`; consulta 2026-09-30 para OpenAI Harness, AGENTS.md y Claude Code.

### 26. State
- Estado inicial: P01-P06 diseñados.
- Estado final esperado: Plan M1 congelado; siete pasos PLANIFICADOS.
- Estado real: PLANIFICADO. No se ejecutó el Paso 1 del proyecto ni se modificó ningún repositorio externo.
- Qué queda pendiente: Futura ejecución de M1 bajo el plan congelado.
- Relación con el siguiente paso: El plan alimenta la continuidad; no constituye ejecución de módulos posteriores.

# Hard quality-gate result

- G1 Source coverage: PASS.
- G2 Semantic depth: PASS.
- G3 Language invariant: PASS.
- G4 Direct traceability: PASS.
- G5 Internal test coverage: PASS.
- G6 Field quality: PASS — cada paso contiene los 26 campos.
- G7 State integrity: PASS — todos PLANIFICADOS; el Paso 1 del proyecto no se ejecutó.
- G8 Step boundary quality: PASS — siete unidades funcionales sin compresión/fragmentación artificial.
- G9 Integration quality: PASS.
- G10 Source discovery != verified evidence: PASS.
- G11 Anti-megaprompt: PASS.
- G12 Prior-output regression only: PASS.
- G13 No artificial decisions: PASS — 0 decisiones nuevas sustantivas.

## Final dynamic count

**N = 7.** Es consecuencia del inventario, dependencias, independencia funcional, profundidad, integración y pruebas anti-compresión/anti-fragmentación.
