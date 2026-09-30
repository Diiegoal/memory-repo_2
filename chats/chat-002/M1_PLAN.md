# Plan M1 — Secuencia canónica de siete unidades

Estado global: `PLANIFICADO`
Sesión: `chat-002`
Module: `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA`
Responsabilidad canónica: este archivo es el único lugar donde se conserva el desarrollo completo de los 26 campos de cada paso de M1.

## Final sequence

`M1-P01 → M1-P02 → M1-P03 → M1-P04 → M1-P05 → M1-P06 → M1-P07`

La descomposición en siete unidades surgió del inventario de capacidades de M1 y se contrastó después con la referencia vinculante de regresión funcional del prompt de Chat2. No apareció evidencia actual que justificara cambiar esas siete fronteras funcionales validadas. El plan es exclusivamente de planificación; el Paso 1 del proyecto objetivo no fue ejecutado.

## Cross-step quality rule

Cada paso contiene exactamente los 26 campos obligatorios y en el orden requerido. Los campos `Expected result`, `Files`, `Commands`, `Code`, `Action`, `Evidence`, `Validation`, `Tests` y `State` distinguen la ejecución futura de lo que realmente se hizo durante Chat2. Todas las pruebas están `PLANIFICADA`.

## Paso 01 — Caracterizar la tarea y determinar el modo de trabajo
### 1. Identification
- ID del paso: `M1-P01`.
- Fase: Fase 1 — Caracterización y encuadre del trabajo.
- Subfase: Subfase 1.1 — Determinación de tarea, riesgo y modo operativo.
- Estado: PLANIFICADO.
- Tipo de paso: Caracterización / decisión de workflow

### 2. Objective
- Objetivo exacto del paso: Convertir una necesidad de ingeniería del Agente SRE en una unidad de trabajo caracterizada: tipo de tarea, resultado esperado, riesgo, grado de autonomía aceptable y modo de trabajo antes de seleccionar herramienta, contexto o prompt.

### 3. Direct relation to M1
- Archivo(s) de M1:
  - `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/1. El modelo mental de los 3 pilares.md`
  - `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/4. Pilar 3 — El Prompt + Integración.md`
- Sección(es)/tema(s):
  - modelo mental de los tres pilares
  - arquitectura general del prompt
  - árbol combinado de decisión: caracterizar tarea → elegir herramienta → preparar contexto → escribir prompt → ejecutar/revisar
- Concepto(s) de M1:
  - Tool/Harness, Context y Prompt como pilares co-iguales
  - caracterización de tarea
  - resultado esperado
  - criterios de éxito
  - restricciones
  - riesgo de acciones consecuenciales
  - workflow Explore/Plan/Execute/Review
- Relación directa: M1 enseña que los tres pilares deben coordinarse alrededor de la tarea. Sin caracterización, la herramienta y el prompt se convierten en decisiones arbitrarias. En un sistema SRE, además, el nivel de riesgo cambia la autonomía permitida.

### 4. Prerequisites
- Conocimientos previos: Comprender que la tarea precede a la elección del mecanismo de interacción y que una sesión de ingeniería debe terminar en una salida verificable.
- Condiciones previas: Existe un caso de trabajo real del proyecto SRE; se dispone de la descripción del resultado que se pretende conseguir; todavía no se ha iniciado implementación del proyecto.
- Evidencia o artefactos necesarios: Ticket, objetivo de cambio, incidencia, refactor o exploración que se vaya a usar como escenario de planificación futura.

### 5. Dependencies
- Depende de: Chat 1 heredado; no depende de otro paso M1.
- Habilita: M1-P02 y, por derivación, la preparación de contexto y prompting.
- Tipo de dependencia: Fundacional / conceptual
- Riesgo si se altera el orden: Elegir herramienta o escribir prompts antes de conocer el trabajo puede llevar a usar un modo demasiado autónomo, a introducir contexto irrelevante o a omitir criterios de aceptación.

### 6. Preparation
- Preparación necesaria: Definir un escenario SRE representativo y registrar explícitamente objetivo, salida, restricciones, riesgos y nivel de intervención humana.
- Entorno: Repositorio objetivo en modo lectura durante Chat 2; la ejecución futura se realizará sobre el repositorio real sin copiar el proyecto de referencia.
- Información que debe estar disponible: Objetivo del cambio, tipo de tarea, criticidad, archivos candidatos, datos confiables/no confiables y restricciones de seguridad conocidas.

### 7. Files
- Archivos que se leerán: Fuentes de M1 indicadas en Direct relation to M1; en ejecución futura, los archivos del proyecto estrictamente necesarios.
- Archivos que se crearán en la ejecución futura: En una ejecución futura, un registro de tarea/work-mode dentro de la documentación del proyecto, según las convenciones que se adopten; NO creado en Chat 2.
- Archivos que se modificarían en la ejecución futura: NO APLICA — Chat 2 solo planifica; no modifica el proyecto.
- Ubicación exacta de cada archivo: M1 source paths: `Diiegoal/CursoIA/.../Módulo_1...`; artefacto futuro: ubicación exacta a fijar por la estructura del proyecto antes de ejecutar.

### 8. Directory structure
```text
<target-project>/
└── <future engineering-context/task record>
```

### 9. Required concepts
- Concepto: Tool/Harness, Context y Prompt como pilares co-iguales; caracterización de tarea; resultado esperado; criterios de éxito; restricciones; riesgo de acciones consecuenciales; workflow Explore/Plan/Execute/Review.
- Explicación necesaria: Distinguir intención de implementación; reconocer que Tool/Harness, Context y Prompt interactúan; traducir una tarea SRE a resultado observable; identificar si se trata de exploración, debugging, refactor, feature o review.
- Nivel requerido para ejecutar el paso: suficiente para seleccionar, ejecutar o revisar la actividad sin depender de conocimiento implícito; el paso no presupone dominio de módulos posteriores.

### 10. Commands
```text
# Future execution, from the raíz del proyecto
pwd
git status --short
git branch --show-current
```
- Ubicación: raíz del proyecto.
- Resultado esperado: ubicación y estado verificables antes de actuar.
- Verificación: no debe existir cambio accidental atribuido a esta caracterización.

### 11. Code
```text
# No se requiere código para la caracterización de planificación.
```
- Propósito: mantener la unidad en análisis/workflow y no en implementación.
- Partes relevantes: tarea, riesgo, salida y modo.
- Personalización: completar con el caso SRE real durante la ejecución futura.
- Propósito: el campo distingue claramente planificación de implementación.
- Partes relevantes: solo las necesarias para la unidad.
- Personalización requerida: completar en ejecución futura con la herramienta, lenguaje y estructura reales.

### 12. Action
- Acción concreta que se realizará: Clasificar el trabajo; explicitar resultado y criterios; registrar restricciones; determinar el modo de trabajo apropiado; marcar acciones que requieran aprobación humana.
- Orden de ejecución: 1) describir problema; 2) describir resultado; 3) identificar restricciones/riesgo; 4) elegir modo; 5) congelar la caracterización para alimentar P02.
- Entrada utilizada: Escenario real de ingeniería del producto SRE.
- Salida producida: Ficha de caracterización reproducible que permite tomar las siguientes decisiones sin adivinación.

### 13. Reason
- Por qué se realiza esta acción: M1 enseña que los tres pilares deben coordinarse alrededor de la tarea. Sin caracterización, la herramienta y el prompt se convierten en decisiones arbitrarias. En un sistema SRE, además, el nivel de riesgo cambia la autonomía permitida.
- Qué problema resuelve: Evita empezar a codificar o invocar una herramienta con un encargo ambiguo, sin criterio de éxito o con una autonomía incompatible con el riesgo.
- Por qué corresponde a M1: Es la primera aplicación práctica del modelo de los tres pilares y del árbol integrado descrito por M1.

### 14. Expected result
- Resultado esperado: Caracterización completa y específica del escenario; modo de trabajo explícito; criterios de éxito y límites identificados; estado del proyecto sigue sin implementación.
- Estado esperado: PLANIFICADO
- Evidencia esperada: Registro futuro de caracterización y su relación con el ticket/caso fuente.
- Memoria incremental del paso: ZIP de memoria acumulativa que se generará cuando este paso sea ejecutado; debe incorporar estado y evidencia acumulados hasta ese punto. No se genera durante Chat2.

### 15. Evidence
- Evidencia que demuestra el resultado: Registro futuro de caracterización y su relación con el ticket/caso fuente.
- Fuente de la evidencia: M1 §1 y §4; caso de uso real del proyecto objetivo en ejecución futura.
- Cómo se conservará: El registro se conservará dentro de la documentación/contexto del proyecto y se referenciará desde la memoria de sesión; Chat 2 no crea ese archivo.

### 16. Validation
- Qué se debe verificar: Consistencia entre tipo de tarea, objetivo, riesgo, restricciones, nivel de autonomía y modo seleccionado.
- Cómo se verifica: Revisión contra el árbol de decisión de M1 y una lista de aceptación del escenario.
- Resultado esperado de la validación: PASS solo si otra persona puede seleccionar el mismo modo a partir del registro sin información implícita.

### 17. Acceptance criteria
- Criterio 1: La tarea tiene un resultado profesional observable.
- Criterio 2: Se identifican restricciones y riesgos relevantes.
- Criterio 3: El modo de trabajo y el nivel de intervención humana están explícitos.

### 18. Tests
- ID de prueba: `M1-P01-T01`
  - Capacidad/subcapacidad cubierta: Caracterizar la tarea y determinar el modo de trabajo
  - Prueba: ejecutar posteriormente la unidad sobre su escenario representativo y observar el artefacto principal.
  - Entrada: Escenario real de ingeniería del producto SRE..
  - Resultado esperado: Ficha de caracterización reproducible que permite tomar las siguientes decisiones sin adivinación. y todos los criterios de aceptación PASS.
  - Condición de aprobación: cada criterio 1–3 PASS y la evidencia corresponde al escenario ejecutado.
  - Estado de la prueba durante Chat 2: PLANIFICADA
- ID de prueba: `M1-P01-T02`
  - Capacidad/subcapacidad cubierta: detección/corrección del error principal.
  - Prueba: introducir o seleccionar un escenario donde aparezca uno de los errores plausibles y verificar su detección, diagnóstico y corrección.
  - Entrada: escenario controlado + condición de error.
  - Resultado esperado: el error se detecta con la señal definida y la corrección restablece la aceptación.
  - Condición de aprobación: evidencia del error, causa sustentada y verificación posterior PASS.
  - Estado de la prueba durante Chat 2: PLANIFICADA
- ID de prueba: `M1-P01-T03`
  - Capacidad/subcapacidad cubierta: trazabilidad/continuidad.
  - Prueba: reconstruir el resultado usando solo los artefactos de entrada y la evidencia registrada.
  - Entrada: artefactos del paso + referencias.
  - Resultado esperado: otro ingeniero reproduce la justificación y distingue planificado de ejecutado.
  - Condición de aprobación: ninguna afirmación esencial depende de memoria implícita.
  - Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Caracterización demasiado amplia; tarea múltiple disfrazada de una sola; ausencia de criterio de éxito; clasificación incorrecta del riesgo; confusión entre objetivo y solución.
- Cuándo podría aparecer: Al revisar la ficha antes de seleccionar herramienta.
- Síntoma: No se puede explicar qué se va a producir o qué significa PASS.

### 20. Detection
- Cómo detectar el error: Comparar objetivo con salida y criterios; buscar verbos ambiguos como “mejorar” sin condición observable.
- Evidencia del error: Campos de caracterización incompletos o inconsistentes.
- Señal observable: Dos ingenieros seleccionarían modos diferentes para el mismo encargo.

### 21. Meaning
- Qué significa el error o resultado: La tarea aún no tiene una frontera operacional suficientemente definida para consumir los otros pilares.
- Qué parte del proceso afecta: Afecta a P02-P07 porque contamina tool selection, contexto, prompt y evaluación.

### 22. Diagnosis
- Causa probable: Causa probable: objetivo ambiguo o múltiples objetivos. Evidencia: ausencia de salida única/criterios. Orden: objetivo → salida → restricciones → riesgo → modo.
- Evidencia que confirma o descarta la causa: revisar Campos de caracterización incompletos o inconsistentes. y la cadena de entrada/salida definida.
- Orden de diagnóstico: objetivo → entrada → acción → salida → evidencia → validación; retroceder al paso previo solo cuando la evidencia lo justifique.

### 23. Correction
- Corrección: Separar la intención principal de subactividades; definir salida y aceptación; marcar subtrabajos como secuencia posterior o como parte del paso si no tienen independencia profesional. Verificación: repetir la prueba de caracterización. Riesgos: sobrefragmentar artificialmente la tarea.
- Acción concreta: aplicar la corrección sobre la unidad y repetir la validación afectada.
- Verificación posterior: repetir el test fallido y confirmar PASS.
- Riesgos de la corrección: introducir cambios no relacionados, perder trazabilidad o convertir una corrección local en una ampliación de alcance.

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
- M1 → archivo → sección/tema → concepto: M1 file 1, sections sobre tres pilares/modelo mental → caracterización de tarea; M1 file 4, sección del árbol integrado → tarea antes de herramienta/contexto/prompt. Concepto→actividad: caracterizar. Actividad→paso: P01. Paso→artefacto: ficha futura. Paso→evidencia: futura/documental. Paso→validación: revisión de criterios. Paso→memoria ZIP incremental: se generará solo al ejecutar el paso. Paso→siguiente: dependencia real P02. Fuentes externas: OpenAI Harness Engineering (2026-02-11), AGENTS.md (consultado 2026-09-30) como contexto de agentic workflow, no como sustitutos de M1.
- Concepto → actividad: los conceptos enumerados se convierten en la actividad específica de este paso.
- Actividad → paso: la actividad pertenece exclusivamente a `M1-P01` dentro de la secuencia final.
- Paso → artefacto: Ficha de caracterización reproducible que permite tomar las siguientes decisiones sin adivinación..
- Paso → evidencia: la evidencia es FUTURA/DOCUMENTAL; Chat2 no la ejecuta.
- Paso → validación: PASS solo si otra persona puede seleccionar el mismo modo a partir del registro sin información implícita.
- Paso → memoria ZIP incremental: solo durante ejecución futura.
- Paso → siguiente paso: P02 consume la caracterización para elegir y evaluar la herramienta..
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada: la procedencia externa utilizada en la construcción del plan se registra en `chats/chat-002/transcript.md` y `knowledge/facts/external-research.md`.

### 26. State
- Estado inicial: Proyecto objetivo observado sin implementación; P01 no ejecutado durante Chat 2.
- Estado final esperado: El escenario quedará caracterizado y listo para P02 durante ejecución futura.
- Estado real: PLANIFICADO — no ejecutado durante Chat 2.
- Qué queda pendiente: Ejecutar la caracterización sobre un caso real del proyecto cuando se permita iniciar M1.
- Relación con el siguiente paso: P02 consume la caracterización para elegir y evaluar la herramienta.

## Paso 02 — Seleccionar y evaluar la herramienta mediante criterios verificables
### 1. Identification
- ID del paso: `M1-P02`.
- Fase: Fase 1 — Caracterización y encuadre del trabajo.
- Subfase: Subfase 1.2 — Selección de Tool/Harness.
- Estado: PLANIFICADO.
- Tipo de paso: Selección / evaluación de herramienta

### 2. Objective
- Objetivo exacto del paso: Seleccionar el Tool/Harness apropiado para el escenario caracterizado, aplicando explícitamente los cinco criterios de M1 y distinguiendo herramienta de capacidad agentic.

### 3. Direct relation to M1
- Archivo(s) de M1:
  - `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/2. Pilar 1 — La Herramienta.md`
- Sección(es)/tema(s):
  - cuatro categorías de herramientas
  - comportamiento de completion frente a agentic
  - cinco criterios de selección
  - árbol de decisión
  - anti-patrones
- Concepto(s) de M1:
  - IDE copilots
  - terminal/CLI copilots
  - standalone/autonomous/cloud
  - specialized tools
  - codebase size/shape
  - language
  - privacy/compliance
  - budget
  - developer style
  - completion vs agentic
- Relación directa: Pilar 1 no consiste en elegir “el mejor copiloto” universalmente; M1 exige ajustar la herramienta al trabajo, repositorio, lenguaje, privacidad, presupuesto y estilo.

### 4. Prerequisites
- Conocimientos previos: P01 caracterizó el trabajo; se entiende que la herramienta debe servir al modo de trabajo y no al revés.
- Condiciones previas: Se dispone de una shortlist verificable de herramientas/capacidades disponibles en el entorno que finalmente se use.
- Evidencia o artefactos necesarios: Información de herramienta, compatibilidad, acceso al repositorio, controles, costes y capacidades realmente disponibles.

### 5. Dependencies
- Depende de: M1-P01; decisiones heredadas de Chat 1 sobre seguridad/read-only-first deben actuar como restricciones, no como sustitutos de evaluación.
- Habilita: P03 y P04 porque la herramienta seleccionada determina cómo se adjunta/recupera contexto y qué operaciones existen.
- Tipo de dependencia: Técnica / workflow
- Riesgo si se altera el orden: Elegir una herramienta antes de medir privacidad, estilo y forma del trabajo puede forzar un workflow incompatible o con autonomía excesiva.

### 6. Preparation
- Preparación necesaria: Construir una matriz de criterios y evaluar cada candidata con evidencia.
- Entorno: Entorno de desarrollo futuro y documentación oficial de las herramientas; no instalar ni modificar herramientas durante Chat 2.
- Información que debe estar disponible: Características del repo, lenguaje, sensibilidad de datos, presupuesto, preferencias de flujo y necesidades de agente.

### 7. Files
- Archivos que se leerán: M1 tool source; documentación oficial actual de la herramienta elegida en la ejecución futura.
- Archivos que se crearán en la ejecución futura: Matriz futura de selección/tool decision record.
- Archivos que se modificarían en la ejecución futura: NO APLICA en Chat 2.
- Ubicación exacta de cada archivo: Futura documentación de ingeniería del proyecto; ubicación exacta a determinar en P03/P05.

### 8. Directory structure
```text
<target-project>/
└── <future context/tooling decision record>
```

### 9. Required concepts
- Concepto: IDE copilots; terminal/CLI copilots; standalone/autonomous/cloud; specialized tools; codebase size/shape; language; privacy/compliance; budget; developer style; completion vs agentic.
- Explicación necesaria: Cinco criterios, cuatro familias, diferencia completion/agentic, anti-patrones de usar una herramienta grande para todo o delegar con contexto insuficiente.
- Nivel requerido para ejecutar el paso: suficiente para seleccionar, ejecutar o revisar la actividad sin depender de conocimiento implícito; el paso no presupone dominio de módulos posteriores.

### 10. Commands
```text
# Solo ejemplos de ejecución futura
<tool> --version
<tool> --help
```
- Ubicación: entorno donde se ejecutará el copiloto.
- Resultado esperado: versión/capacidades verificables.
- Verificación: contrastar con documentación oficial de la versión realmente instalada.

### 11. Code
```text
# No implementation code.
```
- Propósito: documentar la decisión antes de automatizarla.
- Partes: criterios, evidencia, decisión.
- Personalización: completar solo con datos verificados.
- Propósito: el campo distingue claramente planificación de implementación.
- Partes relevantes: solo las necesarias para la unidad.
- Personalización requerida: completar en ejecución futura con la herramienta, lenguaje y estructura reales.

### 12. Action
- Acción concreta que se realizará: Evaluar candidatas contra los cinco criterios; decidir qué nivel de autonomía se usará; registrar por qué una alternativa queda descartada o reservada.
- Orden de ejecución: 1) tomar caracterización P01; 2) reunir candidatas; 3) aplicar criterios; 4) verificar capacidades; 5) seleccionar; 6) registrar límites.
- Entrada utilizada: Salida de P01 y evidencia de las herramientas disponibles.
- Salida producida: Decisión/registro de Tool/Harness seleccionada y sus límites.

### 13. Reason
- Por qué se realiza esta acción: Pilar 1 no consiste en elegir “el mejor copiloto” universalmente; M1 exige ajustar la herramienta al trabajo, repositorio, lenguaje, privacidad, presupuesto y estilo.
- Qué problema resuelve: Evita sobreherramientas, costes innecesarios y autonomía prematura.
- Por qué corresponde a M1: Es el desarrollo completo del Pilar 1 en una unidad profesional.

### 14. Expected result
- Resultado esperado: Una selección defendible, reversible y documentada; no se instala ni usa productivamente durante Chat 2.
- Estado esperado: PLANIFICADO
- Evidencia esperada: Matriz futura con cada criterio y evidencia.
- Memoria incremental del paso: ZIP de memoria acumulativa que se generará cuando este paso sea ejecutado; debe incorporar estado y evidencia acumulados hasta ese punto. No se genera durante Chat2.

### 15. Evidence
- Evidencia que demuestra el resultado: Matriz futura con cada criterio y evidencia.
- Fuente de la evidencia: M1 Pilar 1 + documentación oficial de la herramienta que se evalúe posteriormente.
- Cómo se conservará: Decision record/context doc y referencias de versión.

### 16. Validation
- Qué se debe verificar: Que la herramienta satisface el modo de trabajo y las restricciones.
- Cómo se verifica: Revisión criterio por criterio y prueba controlada mínima en ejecución futura.
- Resultado esperado de la validación: PASS si la elección puede defenderse sin “porque es la más potente”.

### 17. Acceptance criteria
- Criterio 1: Los cinco criterios están evaluados.
- Criterio 2: La diferencia completion/agentic está documentada.
- Criterio 3: Los límites y condiciones de uso son explícitos.

### 18. Tests
- ID de prueba: `M1-P02-T01`
  - Capacidad/subcapacidad cubierta: Seleccionar y evaluar la herramienta mediante criterios verificables
  - Prueba: ejecutar posteriormente la unidad sobre su escenario representativo y observar el artefacto principal.
  - Entrada: Salida de P01 y evidencia de las herramientas disponibles..
  - Resultado esperado: Decisión/registro de Tool/Harness seleccionada y sus límites. y todos los criterios de aceptación PASS.
  - Condición de aprobación: cada criterio 1–3 PASS y la evidencia corresponde al escenario ejecutado.
  - Estado de la prueba durante Chat 2: PLANIFICADA
- ID de prueba: `M1-P02-T02`
  - Capacidad/subcapacidad cubierta: detección/corrección del error principal.
  - Prueba: introducir o seleccionar un escenario donde aparezca uno de los errores plausibles y verificar su detección, diagnóstico y corrección.
  - Entrada: escenario controlado + condición de error.
  - Resultado esperado: el error se detecta con la señal definida y la corrección restablece la aceptación.
  - Condición de aprobación: evidencia del error, causa sustentada y verificación posterior PASS.
  - Estado de la prueba durante Chat 2: PLANIFICADA
- ID de prueba: `M1-P02-T03`
  - Capacidad/subcapacidad cubierta: trazabilidad/continuidad.
  - Prueba: reconstruir el resultado usando solo los artefactos de entrada y la evidencia registrada.
  - Entrada: artefactos del paso + referencias.
  - Resultado esperado: otro ingeniero reproduce la justificación y distingue planificado de ejecutado.
  - Condición de aprobación: ninguna afirmación esencial depende de memoria implícita.
  - Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Confundir popularidad con adecuación; seleccionar por lista de features; ignorar lenguaje o privacidad; asumir capacidades no verificadas.
- Cuándo podría aparecer: Durante la comparación.
- Síntoma: La matriz contiene opiniones sin evidencia o criterios no respondidos.

### 20. Detection
- Cómo detectar el error: Solicitar evidencia por criterio; identificar filas vacías o afirmaciones sin fuente.
- Evidencia del error: Matriz incompleta o incompatibilidad con el escenario P01.
- Señal observable: La decisión cambia cuando aparece una restricción básica del proyecto.

### 21. Meaning
- Qué significa el error o resultado: La selección no está anclada al problema y puede contaminar todo el workflow.
- Qué parte del proceso afecta: Puede obligar a rehacer contexto, prompts y procedimientos.

### 22. Diagnosis
- Causa probable: Repetir evaluación desde P01; verificar repo/lenguaje/privacy/budget/style antes de comparar features.
- Evidencia que confirma o descarta la causa: revisar Matriz incompleta o incompatibilidad con el escenario P01. y la cadena de entrada/salida definida.
- Orden de diagnóstico: objetivo → entrada → acción → salida → evidencia → validación; retroceder al paso previo solo cuando la evidencia lo justifique.

### 23. Correction
- Corrección: Rehacer la comparación con evidencia verificable y explicitar alternativa/estado. Verificar de nuevo.
- Acción concreta: aplicar la corrección sobre la unidad y repetir la validación afectada.
- Verificación posterior: repetir el test fallido y confirmar PASS.
- Riesgos de la corrección: introducir cambios no relacionados, perder trazabilidad o convertir una corrección local en una ampliación de alcance.

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
- M1 → archivo → sección/tema → concepto: M1 file 2 completo → categorías + criterios + árbol; P01→P02. Paso→tool decision record futuro; evidencia futura/documental; validación por matriz. Fuentes externas actuales: AGENTS.md como referencia sobre agent instructions; OpenAI Harness Engineering (2026-02-11) como referencia de harness/repository context.
- Concepto → actividad: los conceptos enumerados se convierten en la actividad específica de este paso.
- Actividad → paso: la actividad pertenece exclusivamente a `M1-P02` dentro de la secuencia final.
- Paso → artefacto: Decisión/registro de Tool/Harness seleccionada y sus límites..
- Paso → evidencia: la evidencia es FUTURA/DOCUMENTAL; Chat2 no la ejecuta.
- Paso → validación: PASS si la elección puede defenderse sin “porque es la más potente”.
- Paso → memoria ZIP incremental: solo durante ejecución futura.
- Paso → siguiente paso: P03 diseña el contexto persistente compatible con el modo/harness..
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada: la procedencia externa utilizada en la construcción del plan se registra en `chats/chat-002/transcript.md` y `knowledge/facts/external-research.md`.

### 26. State
- Estado inicial: Sin Tool/Harness definitivo producido por Chat 2.
- Estado final esperado: Tool/Harness seleccionado para la ejecución futura.
- Estado real: PLANIFICADO — no ejecutado.
- Qué queda pendiente: Evaluación práctica y verificación de versión/capacidades.
- Relación con el siguiente paso: P03 diseña el contexto persistente compatible con el modo/harness.

## Paso 03 — Diseñar la arquitectura de contexto persistente del proyecto
### 1. Identification
- ID del paso: `M1-P03`.
- Fase: Fase 2 — Arquitectura de contexto.
- Subfase: Subfase 2.1 — Contexto persistente de alto valor.
- Estado: PLANIFICADO.
- Tipo de paso: Diseño / arquitectura documental

### 2. Objective
- Objetivo exacto del paso: Definir qué contexto persistente necesita el proyecto para que el agente/cobot opere con señales de alto valor y bajo ruido, separando instrucciones estables, hechos del proyecto, convenciones, estado y evidencia histórica.

### 3. Direct relation to M1
- Archivo(s) de M1:
  - `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/3. Pilar 2 — El Contexto.md`
- Sección(es)/tema(s):
  - contexto como bottleneck
  - tipos de contexto
  - archivos persistentes AGENTS.md / CLAUDE.md
  - high-signal context
  - subagents y context isolation
  - Write/Select/Compress/Isolate
- Concepto(s) de M1:
  - context window
  - context rot
  - contexto persistente
  - AGENTS.md
  - CLAUDE.md
  - high-signal/low-signal
  - repository knowledge
  - local instructions
  - context layers
- Relación directa: M1 presenta el contexto como cuello de botella y propone contexto persistente mínimo y de alta señal. Para un agente SRE, además, el conocimiento operacional debe ser recuperable sin contaminar instrucciones.

### 4. Prerequisites
- Conocimientos previos: P01/P02 establecieron tarea y herramienta; se dispone de fuentes del proyecto y reglas heredadas de memoria.
- Condiciones previas: La estructura de memoria/documentación del proyecto todavía es una propuesta; no se crea durante Chat 2.
- Evidencia o artefactos necesarios: Inventario de repo, README, restricciones, decisiones Chat1, M1 context source y documentación oficial del agente seleccionado.

### 5. Dependencies
- Depende de: M1-P02; decisiones de Chat1 sobre memoria externa y contaminación.
- Habilita: M1-P04 y P05.
- Tipo de dependencia: Arquitectónica / contextual
- Riesgo si se altera el orden: Sin un esquema estable de contexto, las sesiones se llenan de información repetida, contradictoria o irrelevante.

### 6. Preparation
- Preparación necesaria: Diseñar capas mínimas: instrucciones, estado, decisiones, conocimiento, preguntas y evidencias relevantes; definir qué no entra automáticamente.
- Entorno: Repositorio futuro + memoria externa separada; no modificar repositorios externos en Chat 2.
- Información que debe estar disponible: Convenciones del proyecto, comandos, testing, seguridad, arquitectura, decisiones y estado.

### 7. Files
- Archivos que se leerán: M1 context file, memoria Chat1 `STATE.md`, `DECISIONS.md`, `OPEN_QUESTIONS.md`, handoff y documentación relevante del proyecto.
- Archivos que se crearán en la ejecución futura: En ejecución futura, archivos de contexto del proyecto como `AGENTS.md` o equivalente que la herramienta elegida soporte; no creados en Chat 2.
- Archivos que se modificarían en la ejecución futura: NO APLICA en Chat 2.
- Ubicación exacta de cada archivo: Raíz del proyecto para instrucciones; subdirectorios solo si la herramienta soporta jerarquía y existe necesidad real.

### 8. Directory structure
```text
<target-project>/
├── AGENTS.md          # future project context, if adopted
├── <future source tree>
└── <future docs>
```

### 9. Required concepts
- Concepto: context window; context rot; contexto persistente; AGENTS.md; CLAUDE.md; high-signal/low-signal; repository knowledge; local instructions; context layers.
- Explicación necesaria: Context types; persistent instructions; distinction between memory and current call context; high-signal context; selective retrieval.
- Nivel requerido para ejecutar el paso: suficiente para seleccionar, ejecutar o revisar la actividad sin depender de conocimiento implícito; el paso no presupone dominio de módulos posteriores.

### 10. Commands
```text
# Future inspection examples
find . -maxdepth 2 -type f | sort
cat AGENTS.md
```
- Ubicación: raíz del proyecto.
- Resultado: inventario de contexto existente.
- Verificación: comprobar que las instrucciones no se contradicen con otras fuentes.

### 11. Code
```text
# No implementation code.
```
- Propósito: diseñar estructura de información.
- Personalización: nombres/path exactos se determinarán al iniciar implementación.
- Propósito: el campo distingue claramente planificación de implementación.
- Partes relevantes: solo las necesarias para la unidad.
- Personalización requerida: completar en ejecución futura con la herramienta, lenguaje y estructura reales.

### 12. Action
- Acción concreta que se realizará: Separar contexto estable de estado mutable e histórico; identificar información de alta señal; definir reglas de lectura por tarea y fuentes que no deben cargarse automáticamente.
- Orden de ejecución: 1) inventariar fuentes; 2) clasificar; 3) definir capas; 4) fijar prioridad; 5) definir política de carga; 6) validar contradicciones.
- Entrada utilizada: Fuentes de memoria/repo y contexto de la herramienta.
- Salida producida: Diseño de arquitectura de contexto persistente y política de carga.

### 13. Reason
- Por qué se realiza esta acción: M1 presenta el contexto como cuello de botella y propone contexto persistente mínimo y de alta señal. Para un agente SRE, además, el conocimiento operacional debe ser recuperable sin contaminar instrucciones.
- Qué problema resuelve: Evita “meter todo” en cada prompt y confundir histórico con estado vigente.
- Por qué corresponde a M1: Es el núcleo del Pilar 2.

### 14. Expected result
- Resultado esperado: Mapa de contexto persistente con prioridades, límites y reglas de no carga automática; no implementado durante Chat 2.
- Estado esperado: PLANIFICADO
- Evidencia esperada: Diseño documental y matriz contexto→propósito→fuente→vigencia.
- Memoria incremental del paso: ZIP de memoria acumulativa que se generará cuando este paso sea ejecutado; debe incorporar estado y evidencia acumulados hasta ese punto. No se genera durante Chat2.

### 15. Evidence
- Evidencia que demuestra el resultado: Diseño documental y matriz contexto→propósito→fuente→vigencia.
- Fuente de la evidencia: M1 Context + memory-repo actual + fuentes oficiales de agent context.
- Cómo se conservará: knowledge/context design derivado en Chat2 y artefactos del paso futuro; el diseño canónico de M1 permanece en M1_PLAN.

### 16. Validation
- Qué se debe verificar: Suficiencia, no redundancia, procedencia y separación de estados.
- Cómo se verifica: Recorrer un caso y comprobar que cada dato necesario tiene una fuente y prioridad.
- Resultado esperado de la validación: PASS si un nuevo agente puede recuperar contexto mínimo suficiente sin cargar todo el histórico.

### 17. Acceptance criteria
- Criterio 1: Cada clase de contexto tiene propósito y fuente.
- Criterio 2: La prioridad y la temporalidad están definidas.
- Criterio 3: La política de carga evita contaminación y redundancia.

### 18. Tests
- ID de prueba: `M1-P03-T01`
  - Capacidad/subcapacidad cubierta: Diseñar la arquitectura de contexto persistente del proyecto
  - Prueba: ejecutar posteriormente la unidad sobre su escenario representativo y observar el artefacto principal.
  - Entrada: Fuentes de memoria/repo y contexto de la herramienta..
  - Resultado esperado: Diseño de arquitectura de contexto persistente y política de carga. y todos los criterios de aceptación PASS.
  - Condición de aprobación: cada criterio 1–3 PASS y la evidencia corresponde al escenario ejecutado.
  - Estado de la prueba durante Chat 2: PLANIFICADA
- ID de prueba: `M1-P03-T02`
  - Capacidad/subcapacidad cubierta: detección/corrección del error principal.
  - Prueba: introducir o seleccionar un escenario donde aparezca uno de los errores plausibles y verificar su detección, diagnóstico y corrección.
  - Entrada: escenario controlado + condición de error.
  - Resultado esperado: el error se detecta con la señal definida y la corrección restablece la aceptación.
  - Condición de aprobación: evidencia del error, causa sustentada y verificación posterior PASS.
  - Estado de la prueba durante Chat 2: PLANIFICADA
- ID de prueba: `M1-P03-T03`
  - Capacidad/subcapacidad cubierta: trazabilidad/continuidad.
  - Prueba: reconstruir el resultado usando solo los artefactos de entrada y la evidencia registrada.
  - Entrada: artefactos del paso + referencias.
  - Resultado esperado: otro ingeniero reproduce la justificación y distingue planificado de ejecutado.
  - Condición de aprobación: ninguna afirmación esencial depende de memoria implícita.
  - Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Duplicación de README/AGENTS/STATE; mezcla de instrucciones con datos; persistencia excesiva; falta de procedencia; poner estado histórico como actual.
- Cuándo podría aparecer: Durante diseño/revisión.
- Síntoma: Prompts gigantescos o contradicciones entre archivos.

### 20. Detection
- Cómo detectar el error: Auditoría de overlap, vigencia, autoridad y tamaño.
- Evidencia del error: Dos documentos contienen instrucciones incompatibles o el mismo hecho sin procedencia.
- Señal observable: El agente necesita leer muchos archivos para una tarea simple.

### 21. Meaning
- Qué significa el error o resultado: El contexto persistente aún no es una interfaz estable para el agente.
- Qué parte del proceso afecta: Afecta a P04/P05 y a la mantenibilidad del proyecto.

### 22. Diagnosis
- Causa probable: Clasificar cada documento como instrucción/estado/decisión/conocimiento/histórico; resolver autoridad y vigencia; repetir la revisión.
- Evidencia que confirma o descarta la causa: revisar Dos documentos contienen instrucciones incompatibles o el mismo hecho sin procedencia. y la cadena de entrada/salida definida.
- Orden de diagnóstico: objetivo → entrada → acción → salida → evidencia → validación; retroceder al paso previo solo cuando la evidencia lo justifique.

### 23. Correction
- Corrección: Reducir a mínimo contexto suficiente, enlazar a fuentes específicas y mover histórico a recuperación bajo demanda.
- Acción concreta: aplicar la corrección sobre la unidad y repetir la validación afectada.
- Verificación posterior: repetir el test fallido y confirmar PASS.
- Riesgos de la corrección: introducir cambios no relacionados, perder trazabilidad o convertir una corrección local en una ampliación de alcance.

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
- M1 → archivo → sección/tema → concepto: M1 file 3 → context window, context types, AGENTS/CLAUDE, high-signal; M1 memory layer principles → raw/derived/context packet (supporting framework). P02→P03→P04. Sources: agents.md; OpenAI Harness Engineering.
- Concepto → actividad: los conceptos enumerados se convierten en la actividad específica de este paso.
- Actividad → paso: la actividad pertenece exclusivamente a `M1-P03` dentro de la secuencia final.
- Paso → artefacto: Diseño de arquitectura de contexto persistente y política de carga..
- Paso → evidencia: la evidencia es FUTURA/DOCUMENTAL; Chat2 no la ejecuta.
- Paso → validación: PASS si un nuevo agente puede recuperar contexto mínimo suficiente sin cargar todo el histórico.
- Paso → memoria ZIP incremental: solo durante ejecución futura.
- Paso → siguiente paso: P04 convierte el diseño en operación de ventana/context rot..
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada: la procedencia externa utilizada en la construcción del plan se registra en `chats/chat-002/transcript.md` y `knowledge/facts/external-research.md`.

### 26. State
- Estado inicial: No existe una arquitectura de contexto runtime implementada en el target repo.
- Estado final esperado: Diseño documentado y preparado para P04/P05.
- Estado real: PLANIFICADO — no implementado.
- Qué queda pendiente: Elegir estructura final y crear archivos solo durante ejecución del proyecto.
- Relación con el siguiente paso: P04 convierte el diseño en operación de ventana/context rot.

## Paso 04 — Gestionar la ventana de contexto y prevenir context rot
### 1. Identification
- ID del paso: `M1-P04`.
- Fase: Fase 2 — Arquitectura de contexto.
- Subfase: Subfase 2.2 — Higiene operativa del contexto.
- Estado: PLANIFICADO.
- Tipo de paso: Operación / control de contexto

### 2. Objective
- Objetivo exacto del paso: Aplicar las cuatro estrategias de M1 — Write, Select, Compress e Isolate — junto con las señales de context rot, mecanismos de degradación y reglas prácticas de ventana, para mantener sesiones utilizables y trazables.

### 3. Direct relation to M1
- Archivo(s) de M1:
  - `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/3. Pilar 2 — El Contexto.md`
- Sección(es)/tema(s):
  - context rot
  - lost in the middle
  - attention dilution
  - distractors
  - heurísticas de ventana
  - Write / Select / Compress / Isolate
- Concepto(s) de M1:
  - context rot
  - lost in the middle
  - attention dilution
  - irrelevant context
  - Write
  - Select
  - Compress
  - Isolate
  - compact/restart
  - subagents/context isolation
- Relación directa: M1 advierte que el contexto se degrada y no debe cargarse indiscriminadamente. Las cuatro estrategias convierten esa advertencia en mecanismos prácticos.

### 4. Prerequisites
- Conocimientos previos: P03 define las clases de contexto y qué debe entrar a una sesión.
- Condiciones previas: Debe existir un escenario de conversación suficientemente largo o con fuentes suficientes para evaluar las estrategias; la ejecución es futura.
- Evidencia o artefactos necesarios: Registro de contexto, cambios de longitud/ruido y resultados de tareas antes/después de aplicar cada estrategia.

### 5. Dependencies
- Depende de: M1-P03
- Habilita: M1-P05 y P06; también establece un patrón operativo transversal para futuras sesiones.
- Tipo de dependencia: Operativa / contextual
- Riesgo si se altera el orden: Sin control del contexto, incluso un buen prompt puede degradarse por saturación y distractores.

### 6. Preparation
- Preparación necesaria: Definir una sesión de prueba y métricas observables: relevancia, errores atribuibles a ruido, recuperación de hechos y mantenimiento de instrucciones.
- Entorno: Sesión futura con herramienta seleccionada y archivos de contexto; Chat2 no ejecuta la prueba sobre el target.
- Información que debe estar disponible: Context windows disponibles, fuentes prioritarias, historial y artifacts de P03.

### 7. Files
- Archivos que se leerán: M1 context file y, durante ejecución futura, archivos de contexto y transcript de la sesión de prueba.
- Archivos que se crearán en la ejecución futura: Registro futuro de context hygiene/compact decisions según estructura del proyecto.
- Archivos que se modificarían en la ejecución futura: NO APLICA en Chat2.
- Ubicación exacta de cada archivo: Documentación operativa futura; ubicación exacta dependerá del repo.

### 8. Directory structure
```text
<target-project>/
└── <future context-hygiene records>
```

### 9. Required concepts
- Concepto: context rot; lost in the middle; attention dilution; irrelevant context; Write; Select; Compress; Isolate; compact/restart; subagents/context isolation.
- Explicación necesaria: Context rot, lost-in-the-middle, dilution, distractors; Write = externalize; Select = retrieve only needed; Compress = summarize carefully; Isolate = separate subtasks/contexts.
- Nivel requerido para ejecutar el paso: suficiente para seleccionar, ejecutar o revisar la actividad sin depender de conocimiento implícito; el paso no presupone dominio de módulos posteriores.

### 10. Commands
```text
# Solo ejemplos de ejecución futura
<tool> compact
<tool> --help
```
- Ubicación: sesión/harness futuro.
- Resultado: mecanismo de compactación o sesión aislada disponible.
- Verificación: comparar contenido utilizable antes/después; verificar que las instrucciones críticas permanecen.

### 11. Code
```text
# Sin código.
```
- Propósito: operacionalizar contexto, no implementar runtime.
- Propósito: el campo distingue claramente planificación de implementación.
- Partes relevantes: solo las necesarias para la unidad.
- Personalización requerida: completar en ejecución futura con la herramienta, lenguaje y estructura reales.

### 12. Action
- Acción concreta que se realizará: Evaluar por separado Write, Select, Compress e Isolate; asociar cada estrategia a su condición de uso; aplicar la estrategia mínima que resuelva el problema; registrar lo descartado.
- Orden de ejecución: 1) detectar rot; 2) localizar causa; 3) aplicar Write; 4) Select; 5) Compress; 6) Isolate cuando proceda; 7) verificar recuperación.
- Entrada utilizada: Una sesión futura con contexto real y un resultado de prueba definido.
- Salida producida: Procedimiento de higiene contextual reproducible.

### 13. Reason
- Por qué se realiza esta acción: M1 advierte que el contexto se degrada y no debe cargarse indiscriminadamente. Las cuatro estrategias convierten esa advertencia en mecanismos prácticos.
- Qué problema resuelve: Evita prompts cada vez más largos, errores por información antigua y pérdida de instrucciones relevantes.
- Por qué corresponde a M1: Desarrollo completo y explícito del Pilar 2 y de sus mecanismos operativos.

### 14. Expected result
- Resultado esperado: Cada estrategia está definida por propósito, condición de uso, aplicación y validación. No ejecutado.
- Estado esperado: PLANIFICADO
- Evidencia esperada: Registros comparativos y decisiones de compaction/isolation futuras.
- Memoria incremental del paso: ZIP de memoria acumulativa que se generará cuando este paso sea ejecutado; debe incorporar estado y evidencia acumulados hasta ese punto. No se genera durante Chat2.

### 15. Evidence
- Evidencia que demuestra el resultado: Registros comparativos y decisiones de compaction/isolation futuras.
- Fuente de la evidencia: M1 Context; futura evidencia de sesión/harness.
- Cómo se conservará: Registro de experimento, captura de entradas/salidas y decisión de contexto.

### 16. Validation
- Qué se debe verificar: Que cada una de W/S/C/I cumple su función sin perder información de alta señal.
- Cómo se verifica: Pruebas independientes por estrategia y una prueba integrada de recuperación.
- Resultado esperado de la validación: PASS si las cuatro estrategias pueden justificarse y una sesión posterior puede reconstruir el contexto mínimo suficiente.

### 17. Acceptance criteria
- Criterio 1: Context rot y sus mecanismos están identificados.
- Criterio 2: Write, Select, Compress e Isolate se desarrollan individualmente.
- Criterio 3: Cada estrategia tiene condición de uso y criterio de PASS/FAIL.

### 18. Tests
- ID de prueba: `M1-P04-T01`
  - Capacidad/subcapacidad cubierta: Gestionar la ventana de contexto y prevenir context rot
  - Prueba: ejecutar posteriormente la unidad sobre su escenario representativo y observar el artefacto principal.
  - Entrada: Una sesión futura con contexto real y un resultado de prueba definido..
  - Resultado esperado: Procedimiento de higiene contextual reproducible. y todos los criterios de aceptación PASS.
  - Condición de aprobación: cada criterio 1–3 PASS y la evidencia corresponde al escenario ejecutado.
  - Estado de la prueba durante Chat 2: PLANIFICADA
- ID de prueba: `M1-P04-T02`
  - Capacidad/subcapacidad cubierta: detección/corrección del error principal.
  - Prueba: introducir o seleccionar un escenario donde aparezca uno de los errores plausibles y verificar su detección, diagnóstico y corrección.
  - Entrada: escenario controlado + condición de error.
  - Resultado esperado: el error se detecta con la señal definida y la corrección restablece la aceptación.
  - Condición de aprobación: evidencia del error, causa sustentada y verificación posterior PASS.
  - Estado de la prueba durante Chat 2: PLANIFICADA
- ID de prueba: `M1-P04-T03`
  - Capacidad/subcapacidad cubierta: trazabilidad/continuidad.
  - Prueba: reconstruir el resultado usando solo los artefactos de entrada y la evidencia registrada.
  - Entrada: artefactos del paso + referencias.
  - Resultado esperado: otro ingeniero reproduce la justificación y distingue planificado de ejecutado.
  - Condición de aprobación: ninguna afirmación esencial depende de memoria implícita.
  - Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Comprimir demasiado; seleccionar contexto sin autoridad; aislar una tarea que necesita estado compartido; escribir estado en un lugar no recuperable.
- Cuándo podría aparecer: Durante compactación/reinicio/retrieval.
- Síntoma: Pérdida de decisiones, comandos o hechos críticos.

### 20. Detection
- Cómo detectar el error: Comparar contexto antes/después y ejecutar una tarea de recuperación controlada.
- Evidencia del error: Dato requerido ausente o instrucción importante degradada.
- Señal observable: Resultado diferente después de compactar sin cambio de objetivo.

### 21. Meaning
- Qué significa el error o resultado: La estrategia de gestión contextual está eliminando señales necesarias o no está aislando correctamente.
- Qué parte del proceso afecta: Riesgo de errores y retrabajo en pasos posteriores.

### 22. Diagnosis
- Causa probable: Determinar si falla Write, Select, Compress o Isolate; comparar procedencia y prioridad; revisar el tamaño/context mix.
- Evidencia que confirma o descarta la causa: revisar Dato requerido ausente o instrucción importante degradada. y la cadena de entrada/salida definida.
- Orden de diagnóstico: objetivo → entrada → acción → salida → evidencia → validación; retroceder al paso previo solo cuando la evidencia lo justifique.

### 23. Correction
- Corrección: Reducir/componer de nuevo con estrategia específica; recuperar la fuente primaria; aislar subtask; verificar que los datos críticos sobreviven.
- Acción concreta: aplicar la corrección sobre la unidad y repetir la validación afectada.
- Verificación posterior: repetir el test fallido y confirmar PASS.
- Riesgos de la corrección: introducir cambios no relacionados, perder trazabilidad o convertir una corrección local en una ampliación de alcance.

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
- M1 → archivo → sección/tema → concepto: M1 file 3 → sections on context rot/lost middle/attention dilution/window/Write-Select-Compress-Isolate. P03→P04. Supporting framework: external memory context layers. Each W/S/C/I appears individually in this step. Evidence future.
- Concepto → actividad: los conceptos enumerados se convierten en la actividad específica de este paso.
- Actividad → paso: la actividad pertenece exclusivamente a `M1-P04` dentro de la secuencia final.
- Paso → artefacto: Procedimiento de higiene contextual reproducible..
- Paso → evidencia: la evidencia es FUTURA/DOCUMENTAL; Chat2 no la ejecuta.
- Paso → validación: PASS si las cuatro estrategias pueden justificarse y una sesión posterior puede reconstruir el contexto mínimo suficiente.
- Paso → memoria ZIP incremental: solo durante ejecución futura.
- Paso → siguiente paso: P05 usa el contexto higienizado como entrada del prompt..
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada: la procedencia externa utilizada en la construcción del plan se registra en `chats/chat-002/transcript.md` y `knowledge/facts/external-research.md`.

### 26. State
- Estado inicial: No se ejecutó manejo operativo de contexto en Chat2.
- Estado final esperado: Procedimiento y criterios listos para ejecución futura.
- Estado real: PLANIFICADO.
- Qué queda pendiente: Ejecutar cuatro pruebas y documentar resultados reales.
- Relación con el siguiente paso: P05 usa el contexto higienizado como entrada del prompt.

## Paso 05 — Diseñar y aplicar prompting fundamental para trabajo de ingeniería
### 1. Identification
- ID del paso: `M1-P05`.
- Fase: Fase 3 — Prompting de ingeniería.
- Subfase: Subfase 3.1 — Contrato de prompt y criterios de éxito.
- Estado: PLANIFICADO.
- Tipo de paso: Diseño / ejecución controlada de prompts

### 2. Objective
- Objetivo exacto del paso: Aplicar la arquitectura de prompt de M1 a tareas de ingeniería: contexto corto, tarea, criterios de éxito, restricciones, recursos/referencias, formato de salida y aclaraciones cuando sean necesarias.

### 3. Direct relation to M1
- Archivo(s) de M1:
  - `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/4. Pilar 3 — El Prompt + Integración.md`
- Sección(es)/tema(s):
  - anatomía del prompt
  - criterios de éxito
  - restricciones
  - resources/references
  - output format
  - clarification
  - Markdown/XML
  - few-shot/zero-shot
  - reasoning models
  - anti-patrones
- Concepto(s) de M1:
  - Goal/Task
  - Context
  - Instructions
  - Constraints
  - Success criteria
  - Resources
  - Output
  - clarification
  - few-shot
  - zero-shot
  - delimiters
  - XML
  - positive framing
  - prompt size
- Relación directa: M1 define el prompt como tercer pilar y explica una arquitectura con objetivo, tarea, criterios y límites. La guía de prompts materializada refuerza especificidad, delimitación y evaluación iterativa.

### 4. Prerequisites
- Conocimientos previos: P04 entrega un contexto limpio; P01 entrega objetivo; P02 herramienta/harness.
- Condiciones previas: Se ejecuta sobre un caso representativo futuro y con información de fuentes delimitadas.
- Evidencia o artefactos necesarios: Task brief, relevant context, expected output and acceptance criteria.

### 5. Dependencies
- Depende de: M1-P04
- Habilita: M1-P06 and P07
- Tipo de dependencia: Aplicativa / contractual
- Riesgo si se altera el orden: Un prompt sin salida ni criterios verificables produce resultados difíciles de revisar y convierte la evaluación en opinión.

### 6. Preparation
- Preparación necesaria: Construir un prompt inicial mínimo; separar instrucciones de datos; identificar qué información es recurso y qué es instrucción; definir formato de salida.
- Entorno: Tool/Harness seleccionado y contexto P03/P04.
- Información que debe estar disponible: Caso real, contexto mínimo, constraints, expected output.

### 7. Files
- Archivos que se leerán: M1 prompt file; future project context files; official model/tool prompt docs when needed.
- Archivos que se crearán en la ejecución futura: Artefacto futuro de prompt/registro versionado, cuando esté justificado.
- Archivos que se modificarían en la ejecución futura: NO APLICA en Chat2.
- Ubicación exacta de cada archivo: Ubicación futura de prompt/documentación; la política de versionado será seleccionada por el proyecto.

### 8. Directory structure
```text
<target-project>/
└── <future prompt artifacts>
```

### 9. Required concepts
- Concepto: Goal/Task; Context; Instructions; Constraints; Success criteria; Resources; Output; clarification; few-shot; zero-shot; delimiters; XML; positive framing; prompt size.
- Explicación necesaria: Explicit success criteria; concise context; delimiters; Markdown/XML only where useful; few-shot selectively; direct prompting for reasoning models; avoid vague, micro-spec and megaprompt anti-patterns.
- Nivel requerido para ejecutar el paso: suficiente para seleccionar, ejecutar o revisar la actividad sin depender de conocimiento implícito; el paso no presupone dominio de módulos posteriores.

### 10. Commands
```text
# Future prompt run
<tool> run <prompt-file>
```
- Ubicación: harness seleccionado.
- Resultado: response aligned with contract.
- Verificación: acceptance criteria and output schema/format.

### 11. Code
```text
# Future prompt pseudo-structure
Goal
Context
Task
Constraints
Success criteria
Resources
Output
```
- Propósito: plantilla conceptual, no implementación.
- Propósito: el campo distingue claramente planificación de implementación.
- Partes relevantes: solo las necesarias para la unidad.
- Personalización requerida: completar en ejecución futura con la herramienta, lenguaje y estructura reales.

### 12. Action
- Acción concreta que se realizará: Redactar prompt; ejecutar en caso futuro; revisar resultado; ajustar solo las partes necesarias; conservar versión evaluada.
- Orden de ejecución: 1) objetivo; 2) contexto mínimo; 3) tarea; 4) constraints; 5) success criteria; 6) resources; 7) output; 8) execute/review/iterate.
- Entrada utilizada: Caso P01 + contexto P03/P04.
- Salida producida: Prompt ejecutable y versionable con criterios de aceptación.

### 13. Reason
- Por qué se realiza esta acción: M1 define el prompt como tercer pilar y explica una arquitectura con objetivo, tarea, criterios y límites. La guía de prompts materializada refuerza especificidad, delimitación y evaluación iterativa.
- Qué problema resuelve: Evita “magic prompts”, prompting ambiguo y resultados sin contrato.
- Por qué corresponde a M1: Es la unidad del Pilar 3.

### 14. Expected result
- Resultado esperado: Prompt profesional preparado y prueba futura planificada; no ejecución en Chat2.
- Estado esperado: PLANIFICADO
- Evidencia esperada: Prompt/version record + output real + aceptación en ejecución futura.
- Memoria incremental del paso: ZIP de memoria acumulativa que se generará cuando este paso sea ejecutado; debe incorporar estado y evidencia acumulados hasta ese punto. No se genera durante Chat2.

### 15. Evidence
- Evidencia que demuestra el resultado: Prompt/version record + output real + aceptación en ejecución futura.
- Fuente de la evidencia: M1 prompt source; future run.
- Cómo se conservará: Prompt version + run record in project documentation/revision system.

### 16. Validation
- Qué se debe verificar: Completitud del contrato y separación instrucciones/datos.
- Cómo se verifica: Checklist contra anatomía del prompt + replay del caso con los mismos inputs.
- Resultado esperado de la validación: PASS si el resultado satisface criterios y el prompt puede re-ejecutarse con trazabilidad.

### 17. Acceptance criteria
- Criterio 1: La tarea está delimitada y tiene criterio de éxito.
- Criterio 2: Las restricciones y recursos están separados de las instrucciones.
- Criterio 3: El formato de salida permite revisión objetiva.

### 18. Tests
- ID de prueba: `M1-P05-T01`
  - Capacidad/subcapacidad cubierta: Diseñar y aplicar prompting fundamental para trabajo de ingeniería
  - Prueba: ejecutar posteriormente la unidad sobre su escenario representativo y observar el artefacto principal.
  - Entrada: Caso P01 + contexto P03/P04..
  - Resultado esperado: Prompt ejecutable y versionable con criterios de aceptación. y todos los criterios de aceptación PASS.
  - Condición de aprobación: cada criterio 1–3 PASS y la evidencia corresponde al escenario ejecutado.
  - Estado de la prueba durante Chat 2: PLANIFICADA
- ID de prueba: `M1-P05-T02`
  - Capacidad/subcapacidad cubierta: detección/corrección del error principal.
  - Prueba: introducir o seleccionar un escenario donde aparezca uno de los errores plausibles y verificar su detección, diagnóstico y corrección.
  - Entrada: escenario controlado + condición de error.
  - Resultado esperado: el error se detecta con la señal definida y la corrección restablece la aceptación.
  - Condición de aprobación: evidencia del error, causa sustentada y verificación posterior PASS.
  - Estado de la prueba durante Chat 2: PLANIFICADA
- ID de prueba: `M1-P05-T03`
  - Capacidad/subcapacidad cubierta: trazabilidad/continuidad.
  - Prueba: reconstruir el resultado usando solo los artefactos de entrada y la evidencia registrada.
  - Entrada: artefactos del paso + referencias.
  - Resultado esperado: otro ingeniero reproduce la justificación y distingue planificado de ejecutado.
  - Condición de aprobación: ninguna afirmación esencial depende de memoria implícita.
  - Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Megaprompt; micro-spec; múltiples tareas; falta de criteria; contexto irrelevante; roleplay decorativo; pedir CoT como regla.
- Cuándo podría aparecer: Al revisar el prompt o sus resultados.
- Síntoma: Prompt enorme, salida ambigua o esfuerzo para interpretar qué era obligatorio.

### 20. Detection
- Cómo detectar el error: Comparación contra plantilla M1 y guía de prompts; replay con caso de prueba.
- Evidencia del error: Campo ausente o resultado no evaluable.
- Señal observable: La respuesta “suena bien” pero no existe criterio de PASS.

### 21. Meaning
- Qué significa el error o resultado: El prompt no funciona como contrato operativo.
- Qué parte del proceso afecta: Afecta a P06/P07 y a cualquier evaluación de output.

### 22. Diagnosis
- Causa probable: Revisar objetivo→contexto→task→constraints→success→resources→output; eliminar ruido.
- Evidencia que confirma o descarta la causa: revisar Campo ausente o resultado no evaluable. y la cadena de entrada/salida definida.
- Orden de diagnóstico: objetivo → entrada → acción → salida → evidencia → validación; retroceder al paso previo solo cuando la evidencia lo justifique.

### 23. Correction
- Corrección: Reescribir con mínima información suficiente; mantener instrucciones claras; añadir ejemplos solo si aportan control; repetir prueba.
- Acción concreta: aplicar la corrección sobre la unidad y repetir la validación afectada.
- Verificación posterior: repetir el test fallido y confirmar PASS.
- Riesgos de la corrección: introducir cambios no relacionados, perder trazabilidad o convertir una corrección local en una ampliación de alcance.

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
- M1 → archivo → sección/tema → concepto: M1 file 4 → prompt anatomy, success criteria, constraints, resources, output, clarification, few-shot/zero-shot, reasoning, anti-patterns. Supporting guide prompt sections 1–16 and evaluation sections. P04→P05→P06.
- Concepto → actividad: los conceptos enumerados se convierten en la actividad específica de este paso.
- Actividad → paso: la actividad pertenece exclusivamente a `M1-P05` dentro de la secuencia final.
- Paso → artefacto: Prompt ejecutable y versionable con criterios de aceptación..
- Paso → evidencia: la evidencia es FUTURA/DOCUMENTAL; Chat2 no la ejecuta.
- Paso → validación: PASS si el resultado satisface criterios y el prompt puede re-ejecutarse con trazabilidad.
- Paso → memoria ZIP incremental: solo durante ejecución futura.
- Paso → siguiente paso: P06 aplica patrones de ejecución sobre prompts/contexto/tool elegidos..
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada: la procedencia externa utilizada en la construcción del plan se registra en `chats/chat-002/transcript.md` y `knowledge/facts/external-research.md`.

### 26. State
- Estado inicial: No prompt runtime creado por Chat2.
- Estado final esperado: Contrato de prompt listo para ejecución futura.
- Estado real: PLANIFICADO.
- Qué queda pendiente: Ejecutar y evaluar prompt con caso real.
- Relación con el siguiente paso: P06 aplica patrones de ejecución sobre prompts/contexto/tool elegidos.

## Paso 06 — Aplicar patrones de ejecución de coding asistido por IA
### 1. Identification
- ID del paso: `M1-P06`.
- Fase: Fase 4 — Ejecución asistida y feedback.
- Subfase: Subfase 4.1 — Patrones de coding.
- Estado: PLANIFICADO.
- Tipo de paso: Ejecución controlada / feedback loop

### 2. Objective
- Objetivo exacto del paso: Aplicar y validar individualmente los cinco patrones de coding de M1 dentro de una misma unidad profesional: Spec-driven preview, Plan-then-execute, Test-first, Refactor con anclas y Critic loops.

### 3. Direct relation to M1
- Archivo(s) de M1:
  - `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/4. Pilar 3 — El Prompt + Integración.md`
- Sección(es)/tema(s):
  - cinco patrones de ejecución de coding
  - relación del patrón con tipo de tarea
  - preview/spec
  - plan/execute
  - test-first
  - anchors/refactor
  - critic loops
- Concepto(s) de M1:
  - Spec-driven preview
  - Plan-then-execute
  - Test-first
  - Refactor con anclas
  - Critic loops
  - feedback loop
  - small verifiable changes
- Relación directa: M1 treats coding patterns as executable feedback mechanisms, not names. The project is agent-assisted, so preview, planning, tests, anchors and critic loops provide control against uncontrolled edits.

### 4. Prerequisites
- Conocimientos previos: P05 provee un prompt con tarea/criterios; P04 controla contexto.
- Condiciones previas: Los patrones se ejecutan en escenarios controlados futuros sobre el proyecto real cuando se habilite M1.
- Evidencia o artefactos necesarios: Diffs, plans, tests, review outputs, iteration records.

### 5. Dependencies
- Depende de: M1-P05
- Habilita: Casos integrados de P07 y futuros workflows de M2/M7/M9/M10.
- Tipo de dependencia: Ejecución / workflow
- Riesgo si se altera el orden: Codificar sin patrón de control puede ocultar drift, fallos y retrabajo; aplicar patrones sin distinguir su uso puede producir sobreproceso.

### 6. Preparation
- Preparación necesaria: Seleccionar una tarea pequeña y definir qué patrón corresponde a qué riesgo.
- Entorno: Tool/Harness real; tests disponibles when applicable.
- Información que debe estar disponible: Task, prompt, context, codebase and acceptance criteria.

### 7. Files
- Archivos que se leerán: Archivos fuente/pruebas futuros y fuente de prompt de M1.
- Archivos que se crearán en la ejecución futura: Future code/tests/spec or review artifacts as the selected pattern requires.
- Archivos que se modificarían en la ejecución futura: Future source/test/doc files; none in Chat2.
- Ubicación exacta de cada archivo: Project source tree determined during execution.

### 8. Directory structure
```text
<target-project>/
├── <source>
├── <tests>
└── <future specs/review artifacts>
```

### 9. Required concepts
- Concepto: Spec-driven preview; Plan-then-execute; Test-first; Refactor con anclas; Critic loops; feedback loop; small verifiable changes.
- Explicación necesaria: Understand each pattern and condition: preview before changes; plan before multi-step execution; test-first when behavior can be specified; anchors for safe refactor; critic loops for independent review.
- Nivel requerido para ejecutar el paso: suficiente para seleccionar, ejecutar o revisar la actividad sin depender de conocimiento implícito; el paso no presupone dominio de módulos posteriores.

### 10. Commands
```text
# Solo ejemplos de ejecución futura
git diff --check
<test-command>
git diff --stat
```
- Ubicación: raíz del proyecto.
- Resultado: cambios/pruebas observables.
- Verificación: criterios de aceptación + estado de pruebas + evidencia de revisión.

### 11. Code
```text
# No project code is created in Chat2.
# El código futuro solo se produce después de ejecutar el patrón seleccionado.
```
- Propósito: preserve future boundary.
- Propósito: el campo distingue claramente planificación de implementación.
- Partes relevantes: solo las necesarias para la unidad.
- Personalización requerida: completar en ejecución futura con la herramienta, lenguaje y estructura reales.

### 12. Action
- Acción concreta que se realizará: For each pattern: choose scenario; state purpose; define input; execute; review output; capture evidence; determine PASS/FAIL. Do not merge patterns into a nominal checklist.
- Orden de ejecución: 1) map task to pattern; 2) execute one pattern; 3) observe; 4) test/review; 5) adjust; 6) repeat for other patterns as justified.
- Entrada utilizada: Future task + P05 prompt + P04 context.
- Salida producida: Procedimientos de patrones respaldados por evidencia y resultados futuros de código/pruebas/revisión.

### 13. Reason
- Por qué se realiza esta acción: M1 treats coding patterns as executable feedback mechanisms, not names. The project is agent-assisted, so preview, planning, tests, anchors and critic loops provide control against uncontrolled edits.
- Qué problema resuelve: Reduce unsafe changes, hidden assumptions and regressions.
- Por qué corresponde a M1: The prompt expressly requires all cinco patrones to remain and be developed individually.

### 14. Expected result
- Resultado esperado: Five pattern records/tests prepared; no code run in Chat2.
- Estado esperado: PLANIFICADO
- Evidencia esperada: For each pattern, future run record/diff/test/review.
- Memoria incremental del paso: ZIP de memoria acumulativa que se generará cuando este paso sea ejecutado; debe incorporar estado y evidencia acumulados hasta ese punto. No se genera durante Chat2.

### 15. Evidence
- Evidencia que demuestra el resultado: For each pattern, future run record/diff/test/review.
- Fuente de la evidencia: M1 prompt integration section and five-pattern material.
- Cómo se conservará: Project Git history + test/review artifact + memory step ZIP in future execution.

### 16. Validation
- Qué se debe verificar: Each of cinco patrones has a concrete condition of use and observable validation.
- Cómo se verifica: Run per-pattern scenario; compare against acceptance.
- Resultado esperado de la validación: PASS only when each pattern is distinguishable and produces evidence.

### 17. Acceptance criteria
- Criterio 1: All cinco patrones are developed individually.
- Criterio 2: Each pattern has input, action and observable validation.
- Criterio 3: No pattern is represented only by its name.

### 18. Tests
- ID de prueba: `M1-P06-T01`
  - Capacidad/subcapacidad cubierta: Aplicar patrones de ejecución de coding asistido por IA
  - Prueba: ejecutar posteriormente la unidad sobre su escenario representativo y observar el artefacto principal.
  - Entrada: Future task + P05 prompt + P04 context..
  - Resultado esperado: Procedimientos de patrones respaldados por evidencia y resultados futuros de código/pruebas/revisión. y todos los criterios de aceptación PASS.
  - Condición de aprobación: cada criterio 1–3 PASS y la evidencia corresponde al escenario ejecutado.
  - Estado de la prueba durante Chat 2: PLANIFICADA
- ID de prueba: `M1-P06-T02`
  - Capacidad/subcapacidad cubierta: detección/corrección del error principal.
  - Prueba: introducir o seleccionar un escenario donde aparezca uno de los errores plausibles y verificar su detección, diagnóstico y corrección.
  - Entrada: escenario controlado + condición de error.
  - Resultado esperado: el error se detecta con la señal definida y la corrección restablece la aceptación.
  - Condición de aprobación: evidencia del error, causa sustentada y verificación posterior PASS.
  - Estado de la prueba durante Chat 2: PLANIFICADA
- ID de prueba: `M1-P06-T03`
  - Capacidad/subcapacidad cubierta: trazabilidad/continuidad.
  - Prueba: reconstruir el resultado usando solo los artefactos de entrada y la evidencia registrada.
  - Entrada: artefactos del paso + referencias.
  - Resultado esperado: otro ingeniero reproduce la justificación y distingue planificado de ejecutado.
  - Condición de aprobación: ninguna afirmación esencial depende de memoria implícita.
  - Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Using plan as substitute for execution; test-first without behavior definition; refactor without anchors; critic loop with no acceptance target; preview that is ignored.
- Cuándo podría aparecer: During pattern execution.
- Síntoma: Diffs cannot be explained against the intended result or reviews are purely textual.

### 20. Detection
- Cómo detectar el error: Compare planned action, diff, tests and criteria.
- Evidencia del error: Mismatch or missing artifact.
- Señal observable: Pattern step produces no independently reviewable evidence.

### 21. Meaning
- Qué significa el error o resultado: The pattern is being treated as ceremony instead of control.
- Qué parte del proceso afecta: Reduces trust in agent-assisted changes.

### 22. Diagnosis
- Causa probable: Verify task-pattern mapping; inspect prompt/context; inspect actual diff/tests; identify weakest feedback link.
- Evidencia que confirma o descarta la causa: revisar Mismatch or missing artifact. y la cadena de entrada/salida definida.
- Orden de diagnóstico: objetivo → entrada → acción → salida → evidencia → validación; retroceder al paso previo solo cuando la evidencia lo justifique.

### 23. Correction
- Corrección: Choose smaller scope; add test or preview; define anchors; add independent critic; rerun checks.
- Acción concreta: aplicar la corrección sobre la unidad y repetir la validación afectada.
- Verificación posterior: repetir el test fallido y confirmar PASS.
- Riesgos de la corrección: introducir cambios no relacionados, perder trazabilidad o convertir una corrección local en una ampliación de alcance.

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
- M1 → archivo → sección/tema → concepto: M1 file 4 → five coding patterns. P05→P06→P07. Each pattern explicitly named and individually validated per prompt invariants. Future evidence includes diff/tests/review. External OpenAI harness article supports feedback-loop orientation but does not define M1 patterns.
- Concepto → actividad: los conceptos enumerados se convierten en la actividad específica de este paso.
- Actividad → paso: la actividad pertenece exclusivamente a `M1-P06` dentro de la secuencia final.
- Paso → artefacto: Procedimientos de patrones respaldados por evidencia y resultados futuros de código/pruebas/revisión..
- Paso → evidencia: la evidencia es FUTURA/DOCUMENTAL; Chat2 no la ejecuta.
- Paso → validación: PASS only when each pattern is distinguishable and produces evidence.
- Paso → memoria ZIP incremental: solo durante ejecución futura.
- Paso → siguiente paso: P07 integra los tres pilares en los casos canónicos..
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada: la procedencia externa utilizada en la construcción del plan se registra en `chats/chat-002/transcript.md` y `knowledge/facts/external-research.md`.

### 26. State
- Estado inicial: No se ejecutó ningún patrón de coding en Chat2.
- Estado final esperado: Procedimientos de patrones listos para ejecución futura.
- Estado real: PLANIFICADO.
- Qué queda pendiente: Ejecutar los patrones sobre tareas representativas del proyecto.
- Relación con el siguiente paso: P07 integra los tres pilares en los casos canónicos.

## Paso 07 — Integrar los tres pilares y validar los cinco casos canónicos de M1
### 1. Identification
- ID del paso: `M1-P07`.
- Fase: Fase 5 — Integración y validación.
- Subfase: Subfase 5.1 — Integrated Tool → Context → Prompt → Pattern workflow.
- Estado: PLANIFICADO.
- Tipo de paso: Integración / validación end-to-end del método M1

### 2. Objective
- Objetivo exacto del paso: Integrar Tool/Harness, Context y Prompt con el patrón de ejecución apropiado y validar el flujo completo en los cinco casos canónicos: A gran refactor, B greenfield feature, C debugging, D exploration y E code review.

### 3. Direct relation to M1
- Archivo(s) de M1:
  - `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/1. El modelo mental de los 3 pilares.md`
  - `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/2. Pilar 1 — La Herramienta.md`
  - `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/3. Pilar 2 — El Contexto.md`
  - `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/4. Pilar 3 — El Prompt + Integración.md`
- Sección(es)/tema(s):
  - integración de los tres pilares
  - árbol integrado
  - casos A–E: refactor, greenfield, debugging, exploration, code review
- Concepto(s) de M1:
  - tool → context → prompt → pattern → result → evidence → validation
  - case selection
  - review loop
  - fit-for-purpose workflow
- Relación directa: M1 is not complete when the pillars are merely described; its value comes from coordinated use. The prompt requires explicit A-E coverage and the chain of tool/context/prompt/pattern/result/evidence/validation.

### 4. Prerequisites
- Conocimientos previos: P01-P06 conceptually complete; patterns and hygiene procedures defined.
- Condiciones previas: Scenarios future and may use controlled project tasks; Chat2 does not execute them.
- Evidencia o artefactos necesarios: One scenario record per case, selected tool, context package, prompt, pattern, output, evidence and validation.

### 5. Dependencies
- Depende de: M1-P06; integra todas las unidades anteriores de M1.
- Habilita: A reusable Agentic SDLC operating procedure for later modules.
- Tipo de dependencia: Integración / validación
- Riesgo si se altera el orden: Sin integración, los tres pilares permanecen como teoría separada y no se prueba la coherencia del método.

### 6. Preparation
- Preparación necesaria: Define canonical scenario and acceptance criteria for A-E; ensure read-only-first where actions are consequential.
- Entorno: Proyecto objetivo futuro + harness seleccionado.
- Información que debe estar disponible: Case descriptions, safe fixtures/test data and acceptance criteria.

### 7. Files
- Archivos que se leerán: M1 four source files; future project docs/context and test fixtures.
- Archivos que se crearán en la ejecución futura: Registros futuros de evidencia por caso y, cuando corresponda, artefactos de revisión/pruebas; ninguno creado en Chat2.
- Archivos que se modificarían en la ejecución futura: Archivos del proyecto solo durante la ejecución futura.
- Ubicación exacta de cada archivo: Scenario evidence location to be determined by project documentation convention.

### 8. Directory structure
```text
<target-project>/
├── <source>
├── <tests>
├── <docs/context>
└── <future case evidence>
```

### 9. Required concepts
- Concepto: tool → context → prompt → pattern → result → evidence → validation; case selection; review loop; fit-for-purpose workflow.
- Explicación necesaria: All three pillars; case-specific tool choice; context selection; prompt contract; matching coding pattern; evidence chain; validation.
- Nivel requerido para ejecutar el paso: suficiente para seleccionar, ejecutar o revisar la actividad sin depender de conocimiento implícito; el paso no presupone dominio de módulos posteriores.

### 10. Commands
```text
# Future integration checks only
git status --short
git diff --check
<test-command>
```
- Ubicación: raíz del proyecto.
- Result: estado limpio y verificado después de cada caso.
- Verification: aceptación del caso + cadena de evidencia.

### 11. Code
```text
# No project implementation in Chat2.
```
- Propósito: integrated workflow is validated later on real cases.
- Propósito: el campo distingue claramente planificación de implementación.
- Partes relevantes: solo las necesarias para la unidad.
- Personalización requerida: completar en ejecución futura con la herramienta, lenguaje y estructura reales.

### 12. Action
- Acción concreta que se realizará: Run A-E in controlled future sessions. For each: characterize, select tool, prepare context, write prompt, select pattern, execute/review, capture result/evidence, validate. Compare failure modes across cases.
- Orden de ejecución: A) large refactor; B) greenfield feature; C) debugging; D) exploration; E) code review — cada uno usa la misma cadena con distinto énfasis/patrón.
- Entrada utilizada: Five canonical cases and outputs of P01-P06.
- Salida producida: Método operativo integrado de M1 con evidencia específica por caso y criterios de aceptación reutilizables.

### 13. Reason
- Por qué se realiza esta acción: M1 is not complete when the pillars are merely described; its value comes from coordinated use. The prompt requires explicit A-E coverage and the chain of tool/context/prompt/pattern/result/evidence/validation.
- Qué problema resuelve: Detects mismatches that single-pillar validation would miss.
- Por qué corresponde a M1: Final integration of the module and canonical cases.

### 14. Expected result
- Resultado esperado: Five case procedures and evaluation plans; no case executed in Chat2.
- Estado esperado: PLANIFICADO
- Evidencia esperada: Paquetes de evidencia futuros para A-E.
- Memoria incremental del paso: ZIP de memoria acumulativa que se generará cuando este paso sea ejecutado; debe incorporar estado y evidencia acumulados hasta ese punto. No se genera durante Chat2.

### 15. Evidence
- Evidencia que demuestra el resultado: Paquetes de evidencia futuros para A-E.
- Fuente de la evidencia: M1 integration/canonical case section.
- Cómo se conservará: Project docs/test/review evidence plus future incremental memory ZIP.

### 16. Validation
- Qué se debe verificar: Each case completes the full chain and is independently reviewable.
- Cómo se verifica: Case-by-case checklist plus cross-case comparison.
- Resultado esperado de la validación: PASS if A-E each produce the complete chain and reveal no unresolved workflow gap.

### 17. Acceptance criteria
- Criterio 1: Cases A, B, C, D and E are each represented.
- Criterio 2: Each case explicitly maps tool→context→prompt→pattern→result→evidence→validation.
- Criterio 3: The integrated workflow remains bounded by safety/read-only-first constraints.

### 18. Tests
- ID de prueba: `M1-P07-T01`
  - Capacidad/subcapacidad cubierta: Integrar los tres pilares y validar los cinco casos canónicos de M1
  - Prueba: ejecutar posteriormente la unidad sobre su escenario representativo y observar el artefacto principal.
  - Entrada: Five canonical cases and outputs of P01-P06..
  - Resultado esperado: Método operativo integrado de M1 con evidencia específica por caso y criterios de aceptación reutilizables. y todos los criterios de aceptación PASS.
  - Condición de aprobación: cada criterio 1–3 PASS y la evidencia corresponde al escenario ejecutado.
  - Estado de la prueba durante Chat 2: PLANIFICADA
- ID de prueba: `M1-P07-T02`
  - Capacidad/subcapacidad cubierta: detección/corrección del error principal.
  - Prueba: introducir o seleccionar un escenario donde aparezca uno de los errores plausibles y verificar su detección, diagnóstico y corrección.
  - Entrada: escenario controlado + condición de error.
  - Resultado esperado: el error se detecta con la señal definida y la corrección restablece la aceptación.
  - Condición de aprobación: evidencia del error, causa sustentada y verificación posterior PASS.
  - Estado de la prueba durante Chat 2: PLANIFICADA
- ID de prueba: `M1-P07-T03`
  - Capacidad/subcapacidad cubierta: trazabilidad/continuidad.
  - Prueba: reconstruir el resultado usando solo los artefactos de entrada y la evidencia registrada.
  - Entrada: artefactos del paso + referencias.
  - Resultado esperado: otro ingeniero reproduce la justificación y distingue planificado de ejecutado.
  - Condición de aprobación: ninguna afirmación esencial depende de memoria implícita.
  - Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Usar un prompt/herramienta genérico para todos los casos; missing evidence; choosing pattern by habit; confusing exploration with implementation; applying reviewer pattern to a refactor without adequate tests.
- Cuándo podría aparecer: Durante las ejecuciones integradas de casos.
- Síntoma: Se reutiliza un workflow sin adaptación ni evidencia.

### 20. Detection
- Cómo detectar el error: Compare each case against its own objective and pattern fit.
- Evidencia del error: Missing chain link or unsupported claim.
- Señal observable: Same context/prompt/pattern appears despite materially different task type without justification.

### 21. Meaning
- Qué significa el error o resultado: The integration is not task-sensitive and therefore not faithful to M1.
- Qué parte del proceso afecta: Reduces reuse quality and creates agentic workflow risk.

### 22. Diagnosis
- Causa probable: Trace from case objective backward: if mismatch, revisit P01/P02/P04/P05; inspect whether context or prompt is the actual fault.
- Evidencia que confirma o descarta la causa: revisar Missing chain link or unsupported claim. y la cadena de entrada/salida definida.
- Orden de diagnóstico: objetivo → entrada → acción → salida → evidencia → validación; retroceder al paso previo solo cuando la evidencia lo justifique.

### 23. Correction
- Corrección: Re-characterize task; change tool or context; adjust prompt/pattern; rerun and preserve evidence.
- Acción concreta: aplicar la corrección sobre la unidad y repetir la validación afectada.
- Verificación posterior: repetir el test fallido y confirmar PASS.
- Riesgos de la corrección: introducir cambios no relacionados, perder trazabilidad o convertir una corrección local en una ampliación de alcance.

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
- M1 → archivo → sección/tema → concepto: M1 files 1–4 → three-pillar model + tool + context + prompt/integration. P01→P07. Cases A/B/C/D/E explicitly remain in this step. Evidence future; validation case-by-case. This completes the required chain tool→context→prompt→pattern→result→evidence→validation.
- Concepto → actividad: los conceptos enumerados se convierten en la actividad específica de este paso.
- Actividad → paso: la actividad pertenece exclusivamente a `M1-P07` dentro de la secuencia final.
- Paso → artefacto: Método operativo integrado de M1 con evidencia específica por caso y criterios de aceptación reutilizables..
- Paso → evidencia: la evidencia es FUTURA/DOCUMENTAL; Chat2 no la ejecuta.
- Paso → validación: PASS if A-E each produce the complete chain and reveal no unresolved workflow gap.
- Paso → memoria ZIP incremental: solo durante ejecución futura.
- Paso → siguiente paso: Los módulos posteriores consumen este método operativo; M1 se cierra como planificado..
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada: la procedencia externa utilizada en la construcción del plan se registra en `chats/chat-002/transcript.md` y `knowledge/facts/external-research.md`.

### 26. State
- Estado inicial: No integrated case executed during Chat2.
- Estado final esperado: Método operativo integrado de M1 listo para aplicación futura.
- Estado real: PLANIFICADO.
- Qué queda pendiente: Execute A-E on representative project work after project Step 1 is authorized.
- Relación con el siguiente paso: Los módulos posteriores consumen este método operativo; M1 se cierra como planificado.
