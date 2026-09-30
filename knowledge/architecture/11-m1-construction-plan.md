# Plan de construcción de M1 — Chat 2

## Alcance y estado

Este documento contiene la descomposición dinámica completa del contenido práctico relevante de M1 en unidades profesionales futuras para el proyecto SRE/DevOps. Todos los pasos usan exactamente la plantilla documental obligatoria de 26 campos. Todos permanecen `PLANIFICADO`; no se ejecutó el Paso 1 del proyecto.

## Determinación dinámica del número de pasos

La cantidad final es **7 unidades profesionales**. No se eligió un número objetivo. El conjunto surgió después de contrastar cobertura, profundidad, independencia funcional, anti-compresión, anti-fragmentación, dependencias, salidas y validación. La prueba final conserva separadas las capacidades que constituyen unidades profesionales distintas y mantiene juntas las subactividades que comparten un único resultado profesional.

## Mapa de unidades

| ID | Unidad | Fundamento M1 | Dependencia | Salida futura |
|---|---|---|---|---|
| M1-P01 | Modelo de tres pilares y caracterización de trabajo | Archivos 1–2 | Fundamento | Política de modo |
| M1-P02 | Selección/evaluación de herramientas | Archivo 2 | P01 para tareas concretas | Matriz de selección |
| M1-P03 | Contexto persistente y AGENTS.md | Archivos 1–3 | Independiente de P02 | Base persistente |
| M1-P04 | Context engineering operativo | Archivo 3 | P03 | Kit de higiene contextual |
| M1-P05 | Prompting fundamental | Archivos 4–5 | Contexto de P03/P04 | Contrato de prompting |
| M1-P06 | Patrones de ejecución de coding | Archivo 4 | P05 | Playbook de ejecución/revisión |
| M1-P07 | Framework combinado y casos A–E | Archivos 2–4 | P01–P06 | Playbook aplicado |

## Cobertura práctica controlada

**Pilar 1:** categorías A–D; completion vs agentic; reglas de cambio; cinco criterios; modelos; benchmarks; framework; anti-patterns; reglas accionables.

**Pilar 2:** context rot; mecanismos; reglas prácticas de ventana; tipos de contexto; AGENTS.md; alternativas; buenas prácticas; Write / Select / Compress / Isolate; ventanas; kit operativo.

**Pilar 3:** prompting vigente/no vigente; anatomía; éxito; restricciones/recursos/formato/clarificación; anti-patterns; Spec-driven preview; Plan-then-execute; Test-first; Refactor con anclas; Critic loops; razonadores; kit; framework combinado; casos A–E; anti-patterns combinados; meta-insight.

`5. Recursos adicionales.md` actúa como soporte/procedencia y no como paso independiente. La integración del dominio SRE aparece dentro de las unidades que aplican cada capacidad; no existe un paso final de consolidación.

## Límite temporal y de ejecución

M12 se mantiene reference-only. Los comandos y código del target son futuros. Chat 2 termina en `PLANIFICADO`.

## Paso 01 — Establecer el modelo operativo de los tres pilares y caracterizar los modos de trabajo SRE

### 1. Identification
- ID del paso: `M1-P01`
- Fase: Fase A — Fundamento de M1
- Subfase: Unidad 1 — Modelo mental y caracterización de tarea
- Estado: PLANIFICADO
- Tipo de paso: Diseño y preparación

### 2. Objective
- Objetivo exacto del paso: Convertir el modelo mental en una clasificación reutilizable antes de elegir herramientas.

### 3. Direct relation to M1
- Archivo(s) de M1: `1. El modelo mental de los 3 pilares.md`; `2. Pilar 1 — La Herramienta.md`
- Sección(es)/tema(s): Modelo de tres pilares; harness; completion vs agentic; reglas para cambiar de modo.
- Concepto(s) de M1: Tres pilares como palancas co-iguales; alcance de tarea; modo de trabajo.
- Relación directa: Convertir el modelo mental en una clasificación reutilizable antes de elegir herramientas. Evitar usar un agente grande para trabajo trivial o completion para tareas multiartefacto.

### 4. Prerequisites
- Conocimientos previos: Fundamentos de desarrollo asistido por IA y lectura de M1.
- Condiciones previas: Fuentes de M1 disponibles y límites de Chat 2 verificados.
- Evidencia o artefactos necesarios: Los archivos 1 y 2 de M1; decisiones heredadas `DEC-0001`, `DEC-0002`, `DEC-0004`.

### 5. Dependencies
- Depende de: INDEPENDIENTE respecto de la herramienta concreta; produce la entrada de P02.
- Habilita: P02 y la caracterización futura de tareas.
- Tipo de dependencia: Funcional y operacional
- Riesgo si se altera el orden: Cambiar el orden sin revisar la dependencia indicada puede introducir retrabajo, pérdida de trazabilidad o compresión de la capacidad.

### 6. Preparation
- Preparación necesaria: Leer ambos archivos completos; revisar objetivo SRE y las restricciones heredadas.
- Entorno: Copia de staging independiente; repositorios externos en solo lectura.
- Información que debe estar disponible: Objetivo SRE, decisiones heredadas y evidencia de M1.

### 7. Files
- Archivos que se leerán: `1. El modelo mental de los 3 pilares.md`; `2. Pilar 1 — La Herramienta.md`
- Archivos que se crearán en la ejecución futura: art. futuro: política de clasificación y registro de modo de trabajo.
- Archivos que se modificarían en la ejecución futura: La futura guía de contexto puede incorporar estas reglas; no se modifica en Chat 2.
- Ubicación exacta de cada archivo: Directorio futuro del proyecto; ubicación exacta aún no determinada.

### 8. Directory structure
```text
Directorio futuro no fijado:
├── AGENTS.md
└── artefacto de workflow correspondiente
```

### 9. Required concepts
- Concepto: Tres pilares como palancas co-iguales; alcance de tarea; modo de trabajo.
- Explicación necesaria: Tres pilares como palancas co-iguales; alcance de tarea; modo de trabajo.. Debe poder aplicarse sin regresar a M1 para descubrir los pasos básicos.
- Nivel requerido para ejecutar el paso: Suficiente para ejecutar y validar la unidad en una sesión futura.

### 10. Commands
```text
NO APLICA en Chat 2.
```
- Ubicación desde la que se ejecuta cada comando: Solo futuro entorno del proyecto.
- Resultado esperado: La futura ejecución respeta permisos y alcance definidos.
- Verificación: Comprobar salida contra criterios de aceptación y límites de seguridad.

### 11. Code
```text
NO APLICA durante Chat 2.
```
- Propósito: Preparar workflow/documentación, no implementar producto.
- Partes relevantes: NO APLICA o, cuando corresponda, patrón/criterio que se convertirá en artefacto futuro.
- Personalización requerida: Adaptar al proyecto real solo cuando exista el entorno y sus contratos.

### 12. Action
- Acción concreta que se realizará: Caracterizar cada trabajo por alcance, exploración, comandos, riesgo y resultado; decidir completion o agentic.
- Orden de ejecución: 1) leer tarea; 2) caracterizar; 3) decidir modo; 4) registrar razón; 5) transferir a selección si aplica.
- Entrada utilizada: Tarea, contexto y restricciones de la unidad.
- Salida producida: Clasificación explícita con modo, restricciones y razón.

### 13. Reason
- Por qué se realiza esta acción: Evitar usar un agente grande para trabajo trivial o completion para tareas multiartefacto.
- Qué problema resuelve: Elección de modo desproporcionada y pérdida de control del workflow.
- Por qué corresponde a M1: Deriva del modelo mental y del eje completion/agentic del Pilar 1.

### 14. Expected result
- Resultado esperado: Cada tarea M1-driven tiene modo explícito antes de seleccionar herramienta.
- Estado esperado: PLANIFICADO
- Evidencia esperada: Solo evidencia de fuente y planificación; el resultado operativo será evidencia futura.
- Memoria incremental del paso: Se generará en una ejecución futura como snapshot acumulativo; Chat 2 no fabrica ese ZIP.

### 15. Evidence
- Evidencia que demuestra el resultado: Registro futuro del artefacto, pruebas y validación.
- Fuente de la evidencia: Los archivos 1 y 2 de M1; decisiones heredadas `DEC-0001`, `DEC-0002`, `DEC-0004`.
- Cómo se conservará: Versionar artefacto, evidencia y referencias de procedencia.

### 16. Validation
- Qué se debe verificar: Cada tarea M1-driven tiene modo explícito antes de seleccionar herramienta.
- Cómo se verifica: Recorrer la unidad con sus pruebas concretas y verificar fuente, salida y estado.
- Resultado esperado de la validación: PASS cuando la evidencia futura cumpla los criterios; en Chat 2 el estado permanece PLANIFICADO.

### 17. Acceptance criteria
- Criterio 1: PASS si la razón explica por qué no requiere agentic.
- Criterio 2: PASS si explica por qué completion no basta.
- Criterio 3: PASS si no autoriza mutación.

### 18. Tests
- ID de prueba: `M1-P01-T01`
- Capacidad/subcapacidad cubierta: completion/agentic
- Prueba: Clasificar una edición de un archivo sin comandos.
- Entrada: Una tarea de un archivo.
- Resultado esperado: completion con razón basada en alcance.
- Condición de aprobación: PASS si la razón explica por qué no requiere agentic.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P01-T02`
- Capacidad/subcapacidad cubierta: cambio de modo
- Prueba: Clasificar una tarea multiartefacto con exploración y verificaciones.
- Entrada: Varios archivos y comandos futuros.
- Resultado esperado: agentic.
- Condición de aprobación: PASS si explica por qué completion no basta.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P01-T03`
- Capacidad/subcapacidad cubierta: aplicación SRE
- Prueba: Clasificar investigación de incidente de solo lectura.
- Entrada: Varias fuentes de evidencia.
- Resultado esperado: agentic + read-only-first.
- Condición de aprobación: PASS si no autoriza mutación.
- Estado de la prueba durante Chat 2: PLANIFICADA


### 19. Expected errors
- Error plausible 1: Tarea mal clasificada
- Cuándo podría aparecer: Criterios de alcance o ejecución omitidos.
- Síntoma: Modo incongruente.
- Error plausible 2: Regla contradictoria
- Cuándo podría aparecer: Reglas futuras incompatibles.
- Síntoma: Tareas equivalentes reciben modos distintos.

### 20. Detection
- Revisar la evidencia observable indicada en las pruebas.
- Comparar salida con criterios y con el estado de entrada.

### 21. Meaning
- El resultado indica si la unidad conservó la capacidad de M1 sin compresión indebida.

### 22. Diagnosis
- Causa probable: desviación respecto del procedimiento o pérdida de información crítica.
- Evidencia que confirma o descarta la causa: entrada, salida, prueba y fuente de M1.
- Orden de diagnóstico: fuente → capacidad → actividad → salida → validación.

### 23. Correction
- Corrección: Corregir el procedimiento o el artefacto que originó la desviación.
- Acción concreta: Rehacer la actividad con evidencia de M1 y volver a ejecutar las pruebas afectadas.
- Verificación posterior: Repetir la validación de la unidad y confirmar PASS.
- Riesgos de la corrección: La corrección puede afectar dependencias posteriores; debe volver a auditarse si cambia la frontera.

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
- M1 → archivo → sección/tema → concepto: ['`1. El modelo mental de los 3 pilares.md`', '`2. Pilar 1 — La Herramienta.md`'] → Modelo de tres pilares; harness; completion vs agentic; reglas para cambiar de modo. → Tres pilares como palancas co-iguales; alcance de tarea; modo de trabajo.
- Concepto → actividad: Tres pilares como palancas co-iguales; alcance de tarea; modo de trabajo. → Caracterizar cada trabajo por alcance, exploración, comandos, riesgo y resultado; decidir completion o agentic.
- Actividad → paso: Caracterizar cada trabajo por alcance, exploración, comandos, riesgo y resultado; decidir completion o agentic. → `M1-P01`
- Paso → artefacto: `M1-P01` → art. futuro: política de clasificación y registro de modo de trabajo.
- Paso → evidencia: `M1-P01` → Registro futuro del artefacto, pruebas y validación. (futura)
- Paso → validación: `M1-P01` → Cada tarea M1-driven tiene modo explícito antes de seleccionar herramienta.
- Paso → memoria ZIP incremental: `M1-P01` → Se generará en una ejecución futura como snapshot acumulativo; Chat 2 no fabrica ese ZIP.
- Paso → siguiente paso: M1-P02
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: Fuentes externas, fecha, URL/recurso y afirmación: consultar `knowledge/references/reference-index.md` y `knowledge/facts/external-research.md` cuando corresponda.

### 26. State
- Estado inicial: PLANIFICADO
- Estado final esperado: PLANIFICADO, listo para ejecución futura tras prerrequisitos.
- Estado real: PLANIFICADO; no ejecutado en Chat 2.
- Qué queda pendiente: Ejecutar posteriormente y conservar evidencia.
- Relación con el siguiente paso: M1-P02

## Paso 02 — Seleccionar y evaluar herramientas para tareas SRE según criterios explícitos

### 1. Identification
- ID del paso: `M1-P02`
- Fase: Fase A — Fundamento de M1
- Subfase: Unidad 2 — Selección y evaluación de herramienta
- Estado: PLANIFICADO
- Tipo de paso: Diseño y preparación

### 2. Objective
- Objetivo exacto del paso: Construir un proceso de selección reproducible que preserve todo el contenido práctico de herramienta de M1.

### 3. Direct relation to M1
- Archivo(s) de M1: `2. Pilar 1 — La Herramienta.md`
- Sección(es)/tema(s): Categorías A–D; completion/agentic; cinco criterios; modelos disponibles; benchmarks; framework de decisión; anti-patterns; reglas accionables.
- Concepto(s) de M1: Selección de herramienta; criterios; evidencia; disponibilidad; benchmark; alternativa; condición de cambio.
- Relación directa: Construir un proceso de selección reproducible que preserve todo el contenido práctico de herramienta de M1. M1 requiere separar el tipo de trabajo de la herramienta y usar criterios explícitos.

### 4. Prerequisites
- Conocimientos previos: Fundamentos de desarrollo asistido por IA y lectura de M1.
- Condiciones previas: Fuentes de M1 disponibles y límites de Chat 2 verificados.
- Evidencia o artefactos necesarios: Archivo 2 de M1 y P01; benchmarks deberán conservar fecha/versión.

### 5. Dependencies
- Depende de: Depende de P01 cuando existe una tarea concreta; no depende de una tecnología específica.
- Habilita: Matriz de selección y evaluación reutilizable.
- Tipo de dependencia: Funcional y operacional
- Riesgo si se altera el orden: Cambiar el orden sin revisar la dependencia indicada puede introducir retrabajo, pérdida de trazabilidad o compresión de la capacidad.

### 6. Preparation
- Preparación necesaria: Extraer los cinco criterios, categorías, reglas de benchmark y anti-patterns.
- Entorno: Copia de staging independiente; repositorios externos en solo lectura.
- Información que debe estar disponible: Objetivo SRE, decisiones heredadas y evidencia de M1.

### 7. Files
- Archivos que se leerán: `2. Pilar 1 — La Herramienta.md`
- Archivos que se crearán en la ejecución futura: Matriz de selección/evaluación de herramientas.
- Archivos que se modificarían en la ejecución futura: La matriz futura se actualizará con versiones/evidencia; Chat 2 no selecciona una herramienta productiva nueva.
- Ubicación exacta de cada archivo: Directorio futuro del proyecto; ubicación exacta aún no determinada.

### 8. Directory structure
```text
Directorio futuro no fijado:
├── AGENTS.md
└── artefacto de workflow correspondiente
```

### 9. Required concepts
- Concepto: Selección de herramienta; criterios; evidencia; disponibilidad; benchmark; alternativa; condición de cambio.
- Explicación necesaria: Selección de herramienta; criterios; evidencia; disponibilidad; benchmark; alternativa; condición de cambio.. Debe poder aplicarse sin regresar a M1 para descubrir los pasos básicos.
- Nivel requerido para ejecutar el paso: Suficiente para ejecutar y validar la unidad en una sesión futura.

### 10. Commands
```text
NO APLICA en Chat 2.
```
- Ubicación desde la que se ejecuta cada comando: Solo futuro entorno del proyecto.
- Resultado esperado: La futura ejecución respeta permisos y alcance definidos.
- Verificación: Comprobar salida contra criterios de aceptación y límites de seguridad.

### 11. Code
```text
NO APLICA durante Chat 2.
```
- Propósito: Preparar workflow/documentación, no implementar producto.
- Partes relevantes: NO APLICA o, cuando corresponda, patrón/criterio que se convertirá en artefacto futuro.
- Personalización requerida: Adaptar al proyecto real solo cuando exista el entorno y sus contratos.

### 12. Action
- Acción concreta que se realizará: Aplicar categorías y cinco criterios; revisar disponibilidad y benchmarks; registrar alternativa y condición de cambio.
- Orden de ejecución: 1) tomar clasificación; 2) criterios; 3) evidencia/versiones; 4) anti-patterns; 5) selección y alternativa.
- Entrada utilizada: Tarea, contexto y restricciones de la unidad.
- Salida producida: Selección documentada y trazable.

### 13. Reason
- Por qué se realiza esta acción: M1 requiere separar el tipo de trabajo de la herramienta y usar criterios explícitos.
- Qué problema resuelve: Evita decisiones por moda o por capacidad nominal no necesaria.
- Por qué corresponde a M1: Es aplicación directa del Pilar 1.

### 14. Expected result
- Resultado esperado: Existe un framework que puede explicar por qué una herramienta se eligió o descartó.
- Estado esperado: PLANIFICADO
- Evidencia esperada: Solo evidencia de fuente y planificación; el resultado operativo será evidencia futura.
- Memoria incremental del paso: Se generará en una ejecución futura como snapshot acumulativo; Chat 2 no fabrica ese ZIP.

### 15. Evidence
- Evidencia que demuestra el resultado: Registro futuro del artefacto, pruebas y validación.
- Fuente de la evidencia: Archivo 2 de M1 y P01; benchmarks deberán conservar fecha/versión.
- Cómo se conservará: Versionar artefacto, evidencia y referencias de procedencia.

### 16. Validation
- Qué se debe verificar: Existe un framework que puede explicar por qué una herramienta se eligió o descartó.
- Cómo se verifica: Recorrer la unidad con sus pruebas concretas y verificar fuente, salida y estado.
- Resultado esperado de la validación: PASS cuando la evidencia futura cumpla los criterios; en Chat 2 el estado permanece PLANIFICADO.

### 17. Acceptance criteria
- Criterio 1: PASS si ningún criterio queda como opinión sin evidencia.
- Criterio 2: PASS si procedencia y fecha quedan registradas.
- Criterio 3: PASS si la razón identifica el coste/complejidad.

### 18. Tests
- ID de prueba: `M1-P02-T01`
- Capacidad/subcapacidad cubierta: categorías A–D y cinco criterios de selección
- Prueba: Clasificar la tarea dentro de las categorías A–D pertinentes y después comparar dos herramientas para la misma tarea utilizando los cinco criterios de M1.
- Entrada: Una tarea SRE tipificada, dos fichas de herramienta y evidencia de disponibilidad.
- Resultado esperado: La categoría de trabajo queda explícita y los cinco criterios aparecen aplicados con evidencia o señalando la ausencia de evidencia.
- Condición de aprobación: PASS si la categoría es coherente con la tarea y ningún criterio queda como opinión sin evidencia.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P02-T02`
- Capacidad/subcapacidad cubierta: benchmarks
- Prueba: Revisar una capacidad dependiente de benchmark/versión.
- Entrada: Fuente y dato fechado.
- Resultado esperado: Se distingue dato de conclusión.
- Condición de aprobación: PASS si procedencia y fecha quedan registradas.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P02-T03`
- Capacidad/subcapacidad cubierta: anti-patterns
- Prueba: Evaluar herramienta sobredimensionada para tarea simple.
- Entrada: Tarea simple y herramienta compleja.
- Resultado esperado: Se evita sobredimensionamiento.
- Condición de aprobación: PASS si la razón identifica el coste/complejidad.
- Estado de la prueba durante Chat 2: PLANIFICADA


### 19. Expected errors
- Error plausible 1: Selección no trazable
- Cuándo podría aparecer: Se omite evidencia.
- Síntoma: Decisión no reproducible.
- Error plausible 2: Benchmark fuera de corte
- Cuándo podría aparecer: Versión/fecha incompatible.
- Síntoma: Hecho temporal no confiable.

### 20. Detection
- Revisar la evidencia observable indicada en las pruebas.
- Comparar salida con criterios y con el estado de entrada.

### 21. Meaning
- El resultado indica si la unidad conservó la capacidad de M1 sin compresión indebida.

### 22. Diagnosis
- Causa probable: desviación respecto del procedimiento o pérdida de información crítica.
- Evidencia que confirma o descarta la causa: entrada, salida, prueba y fuente de M1.
- Orden de diagnóstico: fuente → capacidad → actividad → salida → validación.

### 23. Correction
- Corrección: Corregir el procedimiento o el artefacto que originó la desviación.
- Acción concreta: Rehacer la actividad con evidencia de M1 y volver a ejecutar las pruebas afectadas.
- Verificación posterior: Repetir la validación de la unidad y confirmar PASS.
- Riesgos de la corrección: La corrección puede afectar dependencias posteriores; debe volver a auditarse si cambia la frontera.

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
- M1 → archivo → sección/tema → concepto: ['`2. Pilar 1 — La Herramienta.md`'] → Categorías A–D; completion/agentic; cinco criterios; modelos disponibles; benchmarks; framework de decisión; anti-patterns; reglas accionables. → Selección de herramienta; criterios; evidencia; disponibilidad; benchmark; alternativa; condición de cambio.
- Concepto → actividad: Selección de herramienta; criterios; evidencia; disponibilidad; benchmark; alternativa; condición de cambio. → Aplicar categorías y cinco criterios; revisar disponibilidad y benchmarks; registrar alternativa y condición de cambio.
- Actividad → paso: Aplicar categorías y cinco criterios; revisar disponibilidad y benchmarks; registrar alternativa y condición de cambio. → `M1-P02`
- Paso → artefacto: `M1-P02` → Matriz de selección/evaluación de herramientas.
- Paso → evidencia: `M1-P02` → Registro futuro del artefacto, pruebas y validación. (futura)
- Paso → validación: `M1-P02` → Existe un framework que puede explicar por qué una herramienta se eligió o descartó.
- Paso → memoria ZIP incremental: `M1-P02` → Se generará en una ejecución futura como snapshot acumulativo; Chat 2 no fabrica ese ZIP.
- Paso → siguiente paso: M1-P03
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: Fuentes externas, fecha, URL/recurso y afirmación: consultar `knowledge/references/reference-index.md` y `knowledge/facts/external-research.md` cuando corresponda.

### 26. State
- Estado inicial: PLANIFICADO
- Estado final esperado: PLANIFICADO, listo para ejecución futura tras prerrequisitos.
- Estado real: PLANIFICADO; no ejecutado en Chat 2.
- Qué queda pendiente: Ejecutar posteriormente y conservar evidencia.
- Relación con el siguiente paso: M1-P03

## Paso 03 — Diseñar la arquitectura de contexto persistente del proyecto y su AGENTS.md

### 1. Identification
- ID del paso: `M1-P03`
- Fase: Fase B — Contexto
- Subfase: Unidad 3 — Contexto persistente
- Estado: PLANIFICADO
- Tipo de paso: Diseño y preparación

### 2. Objective
- Objetivo exacto del paso: Definir qué conocimiento debe vivir con el proyecto y cómo un agente recuperará reglas sin depender del historial del chat.

### 3. Direct relation to M1
- Archivo(s) de M1: `1. El modelo mental de los 3 pilares.md`; `3. Pilar 2 — El Contexto.md`
- Sección(es)/tema(s): Context engineering; contexto persistente; AGENTS.md; estructura; tipos de contexto; alternativas; buenas prácticas.
- Concepto(s) de M1: Conocimiento persistente; instrucciones de repositorio; separación entre proyecto y sesión.
- Relación directa: Definir qué conocimiento debe vivir con el proyecto y cómo un agente recuperará reglas sin depender del historial del chat. M1 trata el contexto como palanca propia y proporciona mecanismos de persistencia como AGENTS.md.

### 4. Prerequisites
- Conocimientos previos: Fundamentos de desarrollo asistido por IA y lectura de M1.
- Condiciones previas: Fuentes de M1 disponibles y límites de Chat 2 verificados.
- Evidencia o artefactos necesarios: M1 files 1 y 3; evidencia de Chat 1 y fuente AGENTS.md verificada.

### 5. Dependencies
- Depende de: Independiente de P02 a nivel funcional; usa la caracterización de P01.
- Habilita: Arquitectura de contexto persistente y estructura futura de AGENTS.md.
- Tipo de dependencia: Funcional y operacional
- Riesgo si se altera el orden: Cambiar el orden sin revisar la dependencia indicada puede introducir retrabajo, pérdida de trazabilidad o compresión de la capacidad.

### 6. Preparation
- Preparación necesaria: Clasificar tipos de contexto y separar reglas permanentes de estado de sesión.
- Entorno: Copia de staging independiente; repositorios externos en solo lectura.
- Información que debe estar disponible: Objetivo SRE, decisiones heredadas y evidencia de M1.

### 7. Files
- Archivos que se leerán: `1. El modelo mental de los 3 pilares.md`; `3. Pilar 2 — El Contexto.md`
- Archivos que se crearán en la ejecución futura: `AGENTS.md` y archivos de conocimiento persistente futuros.
- Archivos que se modificarían en la ejecución futura: Los artefactos futuros evolucionarán con el proyecto; no se escriben en el target durante Chat 2.
- Ubicación exacta de cada archivo: Directorio futuro del proyecto; ubicación exacta aún no determinada.

### 8. Directory structure
```text
Directorio futuro no fijado:
├── AGENTS.md
└── artefacto de workflow correspondiente
```

### 9. Required concepts
- Concepto: Conocimiento persistente; instrucciones de repositorio; separación entre proyecto y sesión.
- Explicación necesaria: Conocimiento persistente; instrucciones de repositorio; separación entre proyecto y sesión.. Debe poder aplicarse sin regresar a M1 para descubrir los pasos básicos.
- Nivel requerido para ejecutar el paso: Suficiente para ejecutar y validar la unidad en una sesión futura.

### 10. Commands
```text
NO APLICA en Chat 2.
```
- Ubicación desde la que se ejecuta cada comando: Solo futuro entorno del proyecto.
- Resultado esperado: La futura ejecución respeta permisos y alcance definidos.
- Verificación: Comprobar salida contra criterios de aceptación y límites de seguridad.

### 11. Code
```text
NO APLICA durante Chat 2.
```
- Propósito: Preparar workflow/documentación, no implementar producto.
- Partes relevantes: NO APLICA o, cuando corresponda, patrón/criterio que se convertirá en artefacto futuro.
- Personalización requerida: Adaptar al proyecto real solo cuando exista el entorno y sus contratos.

### 12. Action
- Acción concreta que se realizará: Diseñar categorías, prioridad, estructura y recuperación selectiva del contexto persistente.
- Orden de ejecución: 1) identificar tipos; 2) definir reglas; 3) separar global/específico; 4) definir recuperación.
- Entrada utilizada: Tarea, contexto y restricciones de la unidad.
- Salida producida: Base persistente de contexto y reglas para agentes.

### 13. Reason
- Por qué se realiza esta acción: M1 trata el contexto como palanca propia y proporciona mecanismos de persistencia como AGENTS.md.
- Qué problema resuelve: Evita pérdida de reglas y dependencia de memoria conversacional implícita.
- Por qué corresponde a M1: Corresponde al Pilar 2.

### 14. Expected result
- Resultado esperado: Una sesión futura puede recuperar reglas críticas sin cargar toda la historia.
- Estado esperado: PLANIFICADO
- Evidencia esperada: Solo evidencia de fuente y planificación; el resultado operativo será evidencia futura.
- Memoria incremental del paso: Se generará en una ejecución futura como snapshot acumulativo; Chat 2 no fabrica ese ZIP.

### 15. Evidence
- Evidencia que demuestra el resultado: Registro futuro del artefacto, pruebas y validación.
- Fuente de la evidencia: M1 files 1 y 3; evidencia de Chat 1 y fuente AGENTS.md verificada.
- Cómo se conservará: Versionar artefacto, evidencia y referencias de procedencia.

### 16. Validation
- Qué se debe verificar: Una sesión futura puede recuperar reglas críticas sin cargar toda la historia.
- Cómo se verifica: Recorrer la unidad con sus pruebas concretas y verificar fuente, salida y estado.
- Resultado esperado de la validación: PASS cuando la evidencia futura cumpla los criterios; en Chat 2 el estado permanece PLANIFICADO.

### 17. Acceptance criteria
- Criterio 1: PASS si la clasificación es consistente.
- Criterio 2: PASS si ninguna restricción necesaria queda ausente.
- Criterio 3: PASS si no cambia la política.

### 18. Tests
- ID de prueba: `M1-P03-T01`
- Capacidad/subcapacidad cubierta: tipos de contexto
- Prueba: Clasificar regla de proyecto, conocimiento técnico y estado de sesión.
- Entrada: Tres ejemplos.
- Resultado esperado: Cada elemento va a su categoría.
- Condición de aprobación: PASS si la clasificación es consistente.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P03-T02`
- Capacidad/subcapacidad cubierta: AGENTS.md
- Prueba: Recuperar reglas mínimas para una tarea.
- Entrada: Tarea + AGENTS.md.
- Resultado esperado: Se recuperan solo reglas relevantes.
- Condición de aprobación: PASS si ninguna restricción necesaria queda ausente.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P03-T03`
- Capacidad/subcapacidad cubierta: contaminación
- Prueba: Introducir documento externo contradictorio.
- Entrada: Documento no confiable + regla persistente.
- Resultado esperado: La fuente externa se trata como dato.
- Condición de aprobación: PASS si no cambia la política.
- Estado de la prueba durante Chat 2: PLANIFICADA


### 19. Expected errors
- Error plausible 1: Contexto insuficiente
- Cuándo podría aparecer: Falta una regla crítica.
- Síntoma: Comportamiento incompatible.
- Error plausible 2: Contaminación
- Cuándo podría aparecer: Fuente secundaria tratada como instrucción.
- Síntoma: Regla activa alterada.

### 20. Detection
- Revisar la evidencia observable indicada en las pruebas.
- Comparar salida con criterios y con el estado de entrada.

### 21. Meaning
- El resultado indica si la unidad conservó la capacidad de M1 sin compresión indebida.

### 22. Diagnosis
- Causa probable: desviación respecto del procedimiento o pérdida de información crítica.
- Evidencia que confirma o descarta la causa: entrada, salida, prueba y fuente de M1.
- Orden de diagnóstico: fuente → capacidad → actividad → salida → validación.

### 23. Correction
- Corrección: Corregir el procedimiento o el artefacto que originó la desviación.
- Acción concreta: Rehacer la actividad con evidencia de M1 y volver a ejecutar las pruebas afectadas.
- Verificación posterior: Repetir la validación de la unidad y confirmar PASS.
- Riesgos de la corrección: La corrección puede afectar dependencias posteriores; debe volver a auditarse si cambia la frontera.

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
- M1 → archivo → sección/tema → concepto: ['`1. El modelo mental de los 3 pilares.md`', '`3. Pilar 2 — El Contexto.md`'] → Context engineering; contexto persistente; AGENTS.md; estructura; tipos de contexto; alternativas; buenas prácticas. → Conocimiento persistente; instrucciones de repositorio; separación entre proyecto y sesión.
- Concepto → actividad: Conocimiento persistente; instrucciones de repositorio; separación entre proyecto y sesión. → Diseñar categorías, prioridad, estructura y recuperación selectiva del contexto persistente.
- Actividad → paso: Diseñar categorías, prioridad, estructura y recuperación selectiva del contexto persistente. → `M1-P03`
- Paso → artefacto: `M1-P03` → `AGENTS.md` y archivos de conocimiento persistente futuros.
- Paso → evidencia: `M1-P03` → Registro futuro del artefacto, pruebas y validación. (futura)
- Paso → validación: `M1-P03` → Una sesión futura puede recuperar reglas críticas sin cargar toda la historia.
- Paso → memoria ZIP incremental: `M1-P03` → Se generará en una ejecución futura como snapshot acumulativo; Chat 2 no fabrica ese ZIP.
- Paso → siguiente paso: M1-P04
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: Fuentes externas, fecha, URL/recurso y afirmación: consultar `knowledge/references/reference-index.md` y `knowledge/facts/external-research.md` cuando corresponda.

### 26. State
- Estado inicial: PLANIFICADO
- Estado final esperado: PLANIFICADO, listo para ejecución futura tras prerrequisitos.
- Estado real: PLANIFICADO; no ejecutado en Chat 2.
- Qué queda pendiente: Ejecutar posteriormente y conservar evidencia.
- Relación con el siguiente paso: M1-P04

## Paso 04 — Gestionar contexto operativo, context rot y Write / Select / Compress / Isolate

### 1. Identification
- ID del paso: `M1-P04`
- Fase: Fase B — Contexto
- Subfase: Unidad 4 — Gestión operativa de la ventana
- Estado: PLANIFICADO
- Tipo de paso: Diseño y preparación

### 2. Objective
- Objetivo exacto del paso: Convertir la gestión de ventana/context rot en un procedimiento operativo reutilizable durante sesiones.

### 3. Direct relation to M1
- Archivo(s) de M1: `3. Pilar 2 — El Contexto.md`
- Sección(es)/tema(s): Context rot; mecanismos del rot; reglas prácticas de ventana; tipos de contexto; buenas prácticas; Write/Select/Compress/Isolate; kit operativo.
- Concepto(s) de M1: Rot; relevancia; redundancia; compresión; selección; aislamiento; ventana.
- Relación directa: Convertir la gestión de ventana/context rot en un procedimiento operativo reutilizable durante sesiones. El Pilar 2 desarrolla explícitamente estos mecanismos y deben quedar ejecutables, no nominales.

### 4. Prerequisites
- Conocimientos previos: Fundamentos de desarrollo asistido por IA y lectura de M1.
- Condiciones previas: Fuentes de M1 disponibles y límites de Chat 2 verificados.
- Evidencia o artefactos necesarios: M1 file 3; evidencia de P03 y documentación de gestión de contexto.

### 5. Dependencies
- Depende de: Depende de P03 para contexto persistente; mantiene un resultado distinto: controlar el contexto activo.
- Habilita: Kit operativo de higiene contextual.
- Tipo de dependencia: Funcional y operacional
- Riesgo si se altera el orden: Cambiar el orden sin revisar la dependencia indicada puede introducir retrabajo, pérdida de trazabilidad o compresión de la capacidad.

### 6. Preparation
- Preparación necesaria: Definir señales de rot y cuándo aplicar cada operación.
- Entorno: Copia de staging independiente; repositorios externos en solo lectura.
- Información que debe estar disponible: Objetivo SRE, decisiones heredadas y evidencia de M1.

### 7. Files
- Archivos que se leerán: `3. Pilar 2 — El Contexto.md`
- Archivos que se crearán en la ejecución futura: Kit de gestión de contexto y reglas de ventana.
- Archivos que se modificarían en la ejecución futura: El kit futuro se ajustará según resultados de uso; no se modifica en Chat 2.
- Ubicación exacta de cada archivo: Directorio futuro del proyecto; ubicación exacta aún no determinada.

### 8. Directory structure
```text
Directorio futuro no fijado:
├── AGENTS.md
└── artefacto de workflow correspondiente
```

### 9. Required concepts
- Concepto: Rot; relevancia; redundancia; compresión; selección; aislamiento; ventana.
- Explicación necesaria: Rot; relevancia; redundancia; compresión; selección; aislamiento; ventana.. Debe poder aplicarse sin regresar a M1 para descubrir los pasos básicos.
- Nivel requerido para ejecutar el paso: Suficiente para ejecutar y validar la unidad en una sesión futura.

### 10. Commands
```text
NO APLICA en Chat 2.
```
- Ubicación desde la que se ejecuta cada comando: Solo futuro entorno del proyecto.
- Resultado esperado: La futura ejecución respeta permisos y alcance definidos.
- Verificación: Comprobar salida contra criterios de aceptación y límites de seguridad.

### 11. Code
```text
NO APLICA durante Chat 2.
```
- Propósito: Preparar workflow/documentación, no implementar producto.
- Partes relevantes: NO APLICA o, cuando corresponda, patrón/criterio que se convertirá en artefacto futuro.
- Personalización requerida: Adaptar al proyecto real solo cuando exista el entorno y sus contratos.

### 12. Action
- Acción concreta que se realizará: Evaluar contexto activo; detectar rot; elegir operación; preservar restricciones; verificar resultado.
- Orden de ejecución: 1) revisar estado; 2) detectar rot; 3) operar; 4) comprobar restricciones; 5) validar relevancia.
- Entrada utilizada: Tarea, contexto y restricciones de la unidad.
- Salida producida: Contexto activo más útil, relevante y controlado.

### 13. Reason
- Por qué se realiza esta acción: El Pilar 2 desarrolla explícitamente estos mecanismos y deben quedar ejecutables, no nominales.
- Qué problema resuelve: Evita ruido, redundancia y pérdida de instrucciones por degradación del contexto.
- Por qué corresponde a M1: Es una aplicación directa del contenido operativo del Pilar 2.

### 14. Expected result
- Resultado esperado: Existe una rutina para detectar rot y mantener contexto mínimo suficiente.
- Estado esperado: PLANIFICADO
- Evidencia esperada: Solo evidencia de fuente y planificación; el resultado operativo será evidencia futura.
- Memoria incremental del paso: Se generará en una ejecución futura como snapshot acumulativo; Chat 2 no fabrica ese ZIP.

### 15. Evidence
- Evidencia que demuestra el resultado: Registro futuro del artefacto, pruebas y validación.
- Fuente de la evidencia: M1 file 3; evidencia de P03 y documentación de gestión de contexto.
- Cómo se conservará: Versionar artefacto, evidencia y referencias de procedencia.

### 16. Validation
- Qué se debe verificar: Existe una rutina para detectar rot y mantener contexto mínimo suficiente.
- Cómo se verifica: Recorrer la unidad con sus pruebas concretas y verificar fuente, salida y estado.
- Resultado esperado de la validación: PASS cuando la evidencia futura cumpla los criterios; en Chat 2 el estado permanece PLANIFICADO.

### 17. Acceptance criteria
- Criterio 1: PASS si se conserva lo crítico.
- Criterio 2: PASS si conserva requisitos y evidencia.
- Criterio 3: PASS si decisiones activas sobreviven.

### 18. Tests
- ID de prueba: `M1-P04-T01`
- Capacidad/subcapacidad cubierta: detectar rot
- Prueba: Evaluar contexto con duplicados y material obsoleto.
- Entrada: Contexto largo + tarea actual.
- Resultado esperado: Se detecta rot.
- Condición de aprobación: PASS si se conserva lo crítico.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P04-T02`
- Capacidad/subcapacidad cubierta: Write/Select
- Prueba: Reducir contexto al conjunto relevante.
- Entrada: Contexto mixto.
- Resultado esperado: Queda mínimo suficiente.
- Condición de aprobación: PASS si conserva requisitos y evidencia.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P04-T03`
- Capacidad/subcapacidad cubierta: Compress
- Prueba: Comprimir histórico sin perder decisiones activas.
- Entrada: Histórico con decisiones.
- Resultado esperado: Estado útil preservado.
- Condición de aprobación: PASS si decisiones activas sobreviven.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P04-T04`
- Capacidad/subcapacidad cubierta: Isolate
- Prueba: Aislar investigación lateral no confiable.
- Entrada: Tarea + material lateral.
- Resultado esperado: No contamina contexto principal.
- Condición de aprobación: PASS si las reglas no cambian.
- Estado de la prueba durante Chat 2: PLANIFICADA


### 19. Expected errors
- Error plausible 1: Rot no detectado
- Cuándo podría aparecer: No se limpia contexto largo.
- Síntoma: Información obsoleta domina.
- Error plausible 2: Pérdida de restricción
- Cuándo podría aparecer: Compresión excesiva.
- Síntoma: Falta una regla activa.

### 20. Detection
- Revisar la evidencia observable indicada en las pruebas.
- Comparar salida con criterios y con el estado de entrada.

### 21. Meaning
- El resultado indica si la unidad conservó la capacidad de M1 sin compresión indebida.

### 22. Diagnosis
- Causa probable: desviación respecto del procedimiento o pérdida de información crítica.
- Evidencia que confirma o descarta la causa: entrada, salida, prueba y fuente de M1.
- Orden de diagnóstico: fuente → capacidad → actividad → salida → validación.

### 23. Correction
- Corrección: Corregir el procedimiento o el artefacto que originó la desviación.
- Acción concreta: Rehacer la actividad con evidencia de M1 y volver a ejecutar las pruebas afectadas.
- Verificación posterior: Repetir la validación de la unidad y confirmar PASS.
- Riesgos de la corrección: La corrección puede afectar dependencias posteriores; debe volver a auditarse si cambia la frontera.

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
- M1 → archivo → sección/tema → concepto: ['`3. Pilar 2 — El Contexto.md`'] → Context rot; mecanismos del rot; reglas prácticas de ventana; tipos de contexto; buenas prácticas; Write/Select/Compress/Isolate; kit operativo. → Rot; relevancia; redundancia; compresión; selección; aislamiento; ventana.
- Concepto → actividad: Rot; relevancia; redundancia; compresión; selección; aislamiento; ventana. → Evaluar contexto activo; detectar rot; elegir operación; preservar restricciones; verificar resultado.
- Actividad → paso: Evaluar contexto activo; detectar rot; elegir operación; preservar restricciones; verificar resultado. → `M1-P04`
- Paso → artefacto: `M1-P04` → Kit de gestión de contexto y reglas de ventana.
- Paso → evidencia: `M1-P04` → Registro futuro del artefacto, pruebas y validación. (futura)
- Paso → validación: `M1-P04` → Existe una rutina para detectar rot y mantener contexto mínimo suficiente.
- Paso → memoria ZIP incremental: `M1-P04` → Se generará en una ejecución futura como snapshot acumulativo; Chat 2 no fabrica ese ZIP.
- Paso → siguiente paso: M1-P05
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: Fuentes externas, fecha, URL/recurso y afirmación: consultar `knowledge/references/reference-index.md` y `knowledge/facts/external-research.md` cuando corresponda.

### 26. State
- Estado inicial: PLANIFICADO
- Estado final esperado: PLANIFICADO, listo para ejecución futura tras prerrequisitos.
- Estado real: PLANIFICADO; no ejecutado en Chat 2.
- Qué queda pendiente: Ejecutar posteriormente y conservar evidencia.
- Relación con el siguiente paso: M1-P05

## Paso 05 — Construir prompting fundamental orientado a resultados y criterios de éxito

### 1. Identification
- ID del paso: `M1-P05`
- Fase: Fase C — Prompting
- Subfase: Unidad 5 — Prompting fundamental
- Estado: PLANIFICADO
- Tipo de paso: Diseño y preparación

### 2. Objective
- Objetivo exacto del paso: Convertir el Pilar 3 en un contrato de prompting reutilizable y evaluable.

### 3. Direct relation to M1
- Archivo(s) de M1: `4. Pilar 3 — El Prompt + Integración.md`; `5. Recursos adicionales.md`
- Sección(es)/tema(s): Prompting vigente/no vigente; anatomía; criterios de éxito; restricciones; recursos; formato; clarificación; anti-patterns; razonadores.
- Concepto(s) de M1: Objetivo; contexto; instrucciones; límites; formato; éxito; incertidumbre.
- Relación directa: Convertir el Pilar 3 en un contrato de prompting reutilizable y evaluable. El prompting de M1 exige precisión, verificabilidad y límites; no una petición vaga.

### 4. Prerequisites
- Conocimientos previos: Fundamentos de desarrollo asistido por IA y lectura de M1.
- Condiciones previas: Fuentes de M1 disponibles y límites de Chat 2 verificados.
- Evidencia o artefactos necesarios: M1 files 4–5; referencia de prompting de Chat 1 como soporte.

### 5. Dependencies
- Depende de: Usa el contexto de P03/P04 y la clasificación de P01; es independiente del patrón de coding de P06.
- Habilita: Contrato/kit de prompting.
- Tipo de dependencia: Funcional y operacional
- Riesgo si se altera el orden: Cambiar el orden sin revisar la dependencia indicada puede introducir retrabajo, pérdida de trazabilidad o compresión de la capacidad.

### 6. Preparation
- Preparación necesaria: Definir plantilla, campos obligatorios, criterios de éxito y reglas de clarificación.
- Entorno: Copia de staging independiente; repositorios externos en solo lectura.
- Información que debe estar disponible: Objetivo SRE, decisiones heredadas y evidencia de M1.

### 7. Files
- Archivos que se leerán: `4. Pilar 3 — El Prompt + Integración.md`; `5. Recursos adicionales.md`
- Archivos que se crearán en la ejecución futura: Kit/contrato de prompting futuro.
- Archivos que se modificarían en la ejecución futura: Los prompts futuros se versionarán con sus resultados; no se ejecutan prompts de producto en Chat 2.
- Ubicación exacta de cada archivo: Directorio futuro del proyecto; ubicación exacta aún no determinada.

### 8. Directory structure
```text
Directorio futuro no fijado:
├── AGENTS.md
└── artefacto de workflow correspondiente
```

### 9. Required concepts
- Concepto: Objetivo; contexto; instrucciones; límites; formato; éxito; incertidumbre.
- Explicación necesaria: Objetivo; contexto; instrucciones; límites; formato; éxito; incertidumbre.. Debe poder aplicarse sin regresar a M1 para descubrir los pasos básicos.
- Nivel requerido para ejecutar el paso: Suficiente para ejecutar y validar la unidad en una sesión futura.

### 10. Commands
```text
NO APLICA en Chat 2.
```
- Ubicación desde la que se ejecuta cada comando: Solo futuro entorno del proyecto.
- Resultado esperado: La futura ejecución respeta permisos y alcance definidos.
- Verificación: Comprobar salida contra criterios de aceptación y límites de seguridad.

### 11. Code
```text
NO APLICA durante Chat 2.
```
- Propósito: Preparar workflow/documentación, no implementar producto.
- Partes relevantes: NO APLICA o, cuando corresponda, patrón/criterio que se convertirá en artefacto futuro.
- Personalización requerida: Adaptar al proyecto real solo cuando exista el entorno y sus contratos.

### 12. Action
- Acción concreta que se realizará: Construir prompts para análisis, documentación y planificación SRE con objetivo, contexto, límites, formato y éxito.
- Orden de ejecución: 1) objetivo; 2) contexto; 3) instrucciones/límites; 4) formato; 5) éxito; 6) anti-patterns/clarificación.
- Entrada utilizada: Tarea, contexto y restricciones de la unidad.
- Salida producida: Prompt estructurado y evaluable.

### 13. Reason
- Por qué se realiza esta acción: El prompting de M1 exige precisión, verificabilidad y límites; no una petición vaga.
- Qué problema resuelve: Reduce ambigüedad y outputs sin criterio de aceptación.
- Por qué corresponde a M1: Corresponde al Pilar 3 y sus prácticas vigentes.

### 14. Expected result
- Resultado esperado: Existe un contrato que permite decidir si la salida cumple.
- Estado esperado: PLANIFICADO
- Evidencia esperada: Solo evidencia de fuente y planificación; el resultado operativo será evidencia futura.
- Memoria incremental del paso: Se generará en una ejecución futura como snapshot acumulativo; Chat 2 no fabrica ese ZIP.

### 15. Evidence
- Evidencia que demuestra el resultado: Registro futuro del artefacto, pruebas y validación.
- Fuente de la evidencia: M1 files 4–5; referencia de prompting de Chat 1 como soporte.
- Cómo se conservará: Versionar artefacto, evidencia y referencias de procedencia.

### 16. Validation
- Qué se debe verificar: Existe un contrato que permite decidir si la salida cumple.
- Cómo se verifica: Recorrer la unidad con sus pruebas concretas y verificar fuente, salida y estado.
- Resultado esperado de la validación: PASS cuando la evidencia futura cumpla los criterios; en Chat 2 el estado permanece PLANIFICADO.

### 17. Acceptance criteria
- Criterio 1: PASS si objetivo/evidencia/límites/formato están separados.
- Criterio 2: PASS si permiten PASS/FAIL.
- Criterio 3: PASS si desaparece ambigüedad material.

### 18. Tests
- ID de prueba: `M1-P05-T01`
- Capacidad/subcapacidad cubierta: anatomía
- Prueba: Construir prompt para resumir evidencia de incidente.
- Entrada: Contexto limitado + formato.
- Resultado esperado: Partes identificables.
- Condición de aprobación: PASS si objetivo/evidencia/límites/formato están separados.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P05-T02`
- Capacidad/subcapacidad cubierta: éxito
- Prueba: Solicitar análisis read-only basado en evidencia.
- Entrada: Incidente sintético + restricciones.
- Resultado esperado: Criterios observables.
- Condición de aprobación: PASS si permiten PASS/FAIL.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P05-T03`
- Capacidad/subcapacidad cubierta: anti-patterns
- Prueba: Corregir prompt ambiguo.
- Entrada: Prompt sin formato ni límites.
- Resultado esperado: Versión precisa.
- Condición de aprobación: PASS si desaparece ambigüedad material.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P05-T04`
- Capacidad/subcapacidad cubierta: clarificación
- Prueba: Probar tarea con dato faltante.
- Entrada: Entrada incompleta.
- Resultado esperado: Solicita aclaración o declara incertidumbre.
- Condición de aprobación: PASS si no inventa el dato.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P05-T05`
- Capacidad/subcapacidad cubierta: investigación sobre razonadores
- Prueba: Comparar una afirmación sobre comportamiento de razonadores usando una fuente fechada y un benchmark o resultado reproducible cuando esté disponible.
- Entrada: Fuente primaria, fecha de consulta y resultado de evaluación disponible.
- Resultado esperado: La afirmación distingue capacidad observada, evidencia experimental y conclusión, sin atribuir propiedades no verificadas al modelo.
- Condición de aprobación: PASS si la afirmación queda trazable a la fuente/medición y cualquier incertidumbre se mantiene explícita.
- Estado de la prueba durante Chat 2: PLANIFICADA


### 19. Expected errors
- Error plausible 1: Prompt subespecificado
- Cuándo podría aparecer: Faltan límites/éxito.
- Síntoma: Salida difícil de evaluar.
- Error plausible 2: Contexto excesivo
- Cuándo podría aparecer: Se carga material no priorizado.
- Síntoma: Ruido y pérdida de foco.

### 20. Detection
- Revisar la evidencia observable indicada en las pruebas.
- Comparar salida con criterios y con el estado de entrada.

### 21. Meaning
- El resultado indica si la unidad conservó la capacidad de M1 sin compresión indebida.

### 22. Diagnosis
- Causa probable: desviación respecto del procedimiento o pérdida de información crítica.
- Evidencia que confirma o descarta la causa: entrada, salida, prueba y fuente de M1.
- Orden de diagnóstico: fuente → capacidad → actividad → salida → validación.

### 23. Correction
- Corrección: Corregir el procedimiento o el artefacto que originó la desviación.
- Acción concreta: Rehacer la actividad con evidencia de M1 y volver a ejecutar las pruebas afectadas.
- Verificación posterior: Repetir la validación de la unidad y confirmar PASS.
- Riesgos de la corrección: La corrección puede afectar dependencias posteriores; debe volver a auditarse si cambia la frontera.

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
- M1 → archivo → sección/tema → concepto: ['`4. Pilar 3 — El Prompt + Integración.md`', '`5. Recursos adicionales.md`'] → Prompting vigente/no vigente; anatomía; criterios de éxito; restricciones; recursos; formato; clarificación; anti-patterns; razonadores. → Objetivo; contexto; instrucciones; límites; formato; éxito; incertidumbre.
- Concepto → actividad: Objetivo; contexto; instrucciones; límites; formato; éxito; incertidumbre. → Construir prompts para análisis, documentación y planificación SRE con objetivo, contexto, límites, formato y éxito.
- Actividad → paso: Construir prompts para análisis, documentación y planificación SRE con objetivo, contexto, límites, formato y éxito. → `M1-P05`
- Paso → artefacto: `M1-P05` → Kit/contrato de prompting futuro.
- Paso → evidencia: `M1-P05` → Registro futuro del artefacto, pruebas y validación. (futura)
- Paso → validación: `M1-P05` → Existe un contrato que permite decidir si la salida cumple.
- Paso → memoria ZIP incremental: `M1-P05` → Se generará en una ejecución futura como snapshot acumulativo; Chat 2 no fabrica ese ZIP.
- Paso → siguiente paso: M1-P06
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: Fuentes externas, fecha, URL/recurso y afirmación: consultar `knowledge/references/reference-index.md` y `knowledge/facts/external-research.md` cuando corresponda.

### 26. State
- Estado inicial: PLANIFICADO
- Estado final esperado: PLANIFICADO, listo para ejecución futura tras prerrequisitos.
- Estado real: PLANIFICADO; no ejecutado en Chat 2.
- Qué queda pendiente: Ejecutar posteriormente y conservar evidencia.
- Relación con el siguiente paso: M1-P06

## Paso 06 — Aplicar patrones de ejecución de coding con gates, pruebas y revisión

### 1. Identification
- ID del paso: `M1-P06`
- Fase: Fase C — Prompting y ejecución
- Subfase: Unidad 6 — Patrones de ejecución de coding
- Estado: PLANIFICADO
- Tipo de paso: Diseño y preparación

### 2. Objective
- Objetivo exacto del paso: Convertir los cinco patrones de ejecución de coding en un workflow de selección, ejecución, prueba y revisión.

### 3. Direct relation to M1
- Archivo(s) de M1: `4. Pilar 3 — El Prompt + Integración.md`
- Sección(es)/tema(s): Spec-driven preview; Plan-then-execute; Test-first; Refactor con anclas; Critic loops.
- Concepto(s) de M1: Patrones de ejecución; gates; preview; plan; test; refactor; crítica.
- Relación directa: Convertir los cinco patrones de ejecución de coding en un workflow de selección, ejecución, prueba y revisión. El Pilar 3 cubre patrones de ejecución además del prompting; fusionarlos haría perder su función de control.

### 4. Prerequisites
- Conocimientos previos: Fundamentos de desarrollo asistido por IA y lectura de M1.
- Condiciones previas: Fuentes de M1 disponibles y límites de Chat 2 verificados.
- Evidencia o artefactos necesarios: M1 file 4; decisiones de workflow heredadas de Chat 1.

### 5. Dependencies
- Depende de: Depende de P05 para prompting; consume specs/tests cuando existan. Es distinto del contrato de prompt.
- Habilita: Playbook de ejecución y revisión.
- Tipo de dependencia: Funcional y operacional
- Riesgo si se altera el orden: Cambiar el orden sin revisar la dependencia indicada puede introducir retrabajo, pérdida de trazabilidad o compresión de la capacidad.

### 6. Preparation
- Preparación necesaria: Definir entrada, propósito, salida y criterio de cierre de cada patrón.
- Entorno: Copia de staging independiente; repositorios externos en solo lectura.
- Información que debe estar disponible: Objetivo SRE, decisiones heredadas y evidencia de M1.

### 7. Files
- Archivos que se leerán: `4. Pilar 3 — El Prompt + Integración.md`
- Archivos que se crearán en la ejecución futura: Playbook de ejecución/revisión de coding.
- Archivos que se modificarían en la ejecución futura: El playbook se ajustará con regresiones futuras; no se ejecuta código del target.
- Ubicación exacta de cada archivo: Directorio futuro del proyecto; ubicación exacta aún no determinada.

### 8. Directory structure
```text
Directorio futuro no fijado:
├── AGENTS.md
└── artefacto de workflow correspondiente
```

### 9. Required concepts
- Concepto: Patrones de ejecución; gates; preview; plan; test; refactor; crítica.
- Explicación necesaria: Patrones de ejecución; gates; preview; plan; test; refactor; crítica.. Debe poder aplicarse sin regresar a M1 para descubrir los pasos básicos.
- Nivel requerido para ejecutar el paso: Suficiente para ejecutar y validar la unidad en una sesión futura.

### 10. Commands
```text
NO APLICA en Chat 2.
```
- Ubicación desde la que se ejecuta cada comando: Solo futuro entorno del proyecto.
- Resultado esperado: La futura ejecución respeta permisos y alcance definidos.
- Verificación: Comprobar salida contra criterios de aceptación y límites de seguridad.

### 11. Code
```text
NO APLICA durante Chat 2.
```
- Propósito: Preparar workflow/documentación, no implementar producto.
- Partes relevantes: NO APLICA o, cuando corresponda, patrón/criterio que se convertirá en artefacto futuro.
- Personalización requerida: Adaptar al proyecto real solo cuando exista el entorno y sus contratos.

### 12. Action
- Acción concreta que se realizará: Seleccionar patrón según cambio, aplicar gate, producir cambio, ejecutar tests y revisión, conservar evidencia.
- Orden de ejecución: 1) objetivo; 2) patrón; 3) gate; 4) cambio; 5) tests; 6) crítica/revisión; 7) cierre.
- Entrada utilizada: Tarea, contexto y restricciones de la unidad.
- Salida producida: Workflow auditable con patrón explícito y evidencia.

### 13. Reason
- Por qué se realiza esta acción: El Pilar 3 cubre patrones de ejecución además del prompting; fusionarlos haría perder su función de control.
- Qué problema resuelve: Reduce cambios grandes, no verificables o difíciles de revisar.
- Por qué corresponde a M1: Corresponde al bloque práctico de integración/coding de M1.

### 14. Expected result
- Resultado esperado: Cada patrón tiene condición de uso, salida y prueba concreta.
- Estado esperado: PLANIFICADO
- Evidencia esperada: Solo evidencia de fuente y planificación; el resultado operativo será evidencia futura.
- Memoria incremental del paso: Se generará en una ejecución futura como snapshot acumulativo; Chat 2 no fabrica ese ZIP.

### 15. Evidence
- Evidencia que demuestra el resultado: Registro futuro del artefacto, pruebas y validación.
- Fuente de la evidencia: M1 file 4; decisiones de workflow heredadas de Chat 1.
- Cómo se conservará: Versionar artefacto, evidencia y referencias de procedencia.

### 16. Validation
- Qué se debe verificar: Cada patrón tiene condición de uso, salida y prueba concreta.
- Cómo se verifica: Recorrer la unidad con sus pruebas concretas y verificar fuente, salida y estado.
- Resultado esperado de la validación: PASS cuando la evidencia futura cumpla los criterios; en Chat 2 el estado permanece PLANIFICADO.

### 17. Acceptance criteria
- Criterio 1: PASS si existe criterio de aceptación.
- Criterio 2: PASS si dependencias aparecen en el plan y diff posterior.
- Criterio 3: PASS si falla por razón correcta y luego pasa.

### 18. Tests
- ID de prueba: `M1-P06-T01`
- Capacidad/subcapacidad cubierta: Spec-driven preview
- Prueba: Preparar un cambio cuya incertidumbre está en la intención/spec.
- Entrada: Spec + cambio.
- Resultado esperado: Preview detecta desalineación antes de ejecutar.
- Condición de aprobación: PASS si existe criterio de aceptación.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P06-T02`
- Capacidad/subcapacidad cubierta: Plan-then-execute
- Prueba: Preparar cambio multiartefacto.
- Entrada: Objetivo + archivos.
- Resultado esperado: Existe plan antes de editar.
- Condición de aprobación: PASS si dependencias aparecen en el plan y diff posterior.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P06-T03`
- Capacidad/subcapacidad cubierta: Test-first
- Prueba: Cambiar regla crítica.
- Entrada: Regla + test.
- Resultado esperado: Test precede implementación.
- Condición de aprobación: PASS si falla por razón correcta y luego pasa.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P06-T04`
- Capacidad/subcapacidad cubierta: Refactor con anclas
- Prueba: Refactor sin cambiar comportamiento.
- Entrada: Código + tests/anclas.
- Resultado esperado: Comportamiento preservado.
- Condición de aprobación: PASS si anclas/tests permanecen verdes.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P06-T05`
- Capacidad/subcapacidad cubierta: Critic loop
- Prueba: Revisar implementación candidata.
- Entrada: Diff + aceptación.
- Resultado esperado: Crítica produce defectos concretos o confirma criterios.
- Condición de aprobación: PASS si existe cierre explícito.
- Estado de la prueba durante Chat 2: PLANIFICADA


### 19. Expected errors
- Error plausible 1: Patrón incorrecto
- Cuándo podría aparecer: Se elige por costumbre.
- Síntoma: Workflow desproporcionado.
- Error plausible 2: Loop sin salida
- Cuándo podría aparecer: Critic loop sin criterio.
- Síntoma: Iteración sin cierre.
- Error plausible 3: Test ornamental
- Cuándo podría aparecer: Prueba no cubre unidad real.
- Síntoma: Falsa confianza.

### 20. Detection
- Revisar la evidencia observable indicada en las pruebas.
- Comparar salida con criterios y con el estado de entrada.

### 21. Meaning
- El resultado indica si la unidad conservó la capacidad de M1 sin compresión indebida.

### 22. Diagnosis
- Causa probable: desviación respecto del procedimiento o pérdida de información crítica.
- Evidencia que confirma o descarta la causa: entrada, salida, prueba y fuente de M1.
- Orden de diagnóstico: fuente → capacidad → actividad → salida → validación.

### 23. Correction
- Corrección: Corregir el procedimiento o el artefacto que originó la desviación.
- Acción concreta: Rehacer la actividad con evidencia de M1 y volver a ejecutar las pruebas afectadas.
- Verificación posterior: Repetir la validación de la unidad y confirmar PASS.
- Riesgos de la corrección: La corrección puede afectar dependencias posteriores; debe volver a auditarse si cambia la frontera.

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
- M1 → archivo → sección/tema → concepto: ['`4. Pilar 3 — El Prompt + Integración.md`'] → Spec-driven preview; Plan-then-execute; Test-first; Refactor con anclas; Critic loops. → Patrones de ejecución; gates; preview; plan; test; refactor; crítica.
- Concepto → actividad: Patrones de ejecución; gates; preview; plan; test; refactor; crítica. → Seleccionar patrón según cambio, aplicar gate, producir cambio, ejecutar tests y revisión, conservar evidencia.
- Actividad → paso: Seleccionar patrón según cambio, aplicar gate, producir cambio, ejecutar tests y revisión, conservar evidencia. → `M1-P06`
- Paso → artefacto: `M1-P06` → Playbook de ejecución/revisión de coding.
- Paso → evidencia: `M1-P06` → Registro futuro del artefacto, pruebas y validación. (futura)
- Paso → validación: `M1-P06` → Cada patrón tiene condición de uso, salida y prueba concreta.
- Paso → memoria ZIP incremental: `M1-P06` → Se generará en una ejecución futura como snapshot acumulativo; Chat 2 no fabrica ese ZIP.
- Paso → siguiente paso: M1-P07
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: Fuentes externas, fecha, URL/recurso y afirmación: consultar `knowledge/references/reference-index.md` y `knowledge/facts/external-research.md` cuando corresponda.

### 26. State
- Estado inicial: PLANIFICADO
- Estado final esperado: PLANIFICADO, listo para ejecución futura tras prerrequisitos.
- Estado real: PLANIFICADO; no ejecutado en Chat 2.
- Qué queda pendiente: Ejecutar posteriormente y conservar evidencia.
- Relación con el siguiente paso: M1-P07

## Paso 07 — Integrar el framework de M1 mediante los casos canónicos A–E y una aplicación SRE nueva

### 1. Identification
- ID del paso: `M1-P07`
- Fase: Fase D — Integración aplicada de M1
- Subfase: Unidad 7 — Framework combinado y casos canónicos
- Estado: PLANIFICADO
- Tipo de paso: Diseño, integración y validación futura

### 2. Objective
- Objetivo exacto del paso: Integrar las capacidades de M1 mediante los casos A–E y una aplicación SRE read-only sin convertir el paso en simple resumen.

### 3. Direct relation to M1
- Archivo(s) de M1: `2. Pilar 1 — La Herramienta.md`; `3. Pilar 2 — El Contexto.md`; `4. Pilar 3 — El Prompt + Integración.md`
- Sección(es)/tema(s): Framework combinado; casos canónicos A–E; anti-patterns combinados; meta-insight; integración tool/context/prompt.
- Concepto(s) de M1: Decisión conjunta de herramienta, contexto y prompt; loops integrados.
- Relación directa: Integrar las capacidades de M1 mediante los casos A–E y una aplicación SRE read-only sin convertir el paso en simple resumen. La integración es una capacidad propia de M1; sin ella los tres pilares quedarían aislados.

### 4. Prerequisites
- Conocimientos previos: Fundamentos de desarrollo asistido por IA y lectura de M1.
- Condiciones previas: Fuentes de M1 disponibles y límites de Chat 2 verificados.
- Evidencia o artefactos necesarios: M1 files 2–4; contexto SRE de referencia y límites heredados.

### 5. Dependencies
- Depende de: Depende de P01–P06.
- Habilita: Playbook combinado y registros de casos.
- Tipo de dependencia: Funcional y operacional
- Riesgo si se altera el orden: Cambiar el orden sin revisar la dependencia indicada puede introducir retrabajo, pérdida de trazabilidad o compresión de la capacidad.

### 6. Preparation
- Preparación necesaria: Definir cómo cada caso usa tarea, modo, herramienta, contexto, prompt, patrón y validación.
- Entorno: Copia de staging independiente; repositorios externos en solo lectura.
- Información que debe estar disponible: Objetivo SRE, decisiones heredadas y evidencia de M1.

### 7. Files
- Archivos que se leerán: `2. Pilar 1 — La Herramienta.md`; `3. Pilar 2 — El Contexto.md`; `4. Pilar 3 — El Prompt + Integración.md`
- Archivos que se crearán en la ejecución futura: Playbook combinado y registros futuros de A–E.
- Archivos que se modificarían en la ejecución futura: Los registros futuros se versionarán; Chat 2 no ejecuta los casos del proyecto.
- Ubicación exacta de cada archivo: Directorio futuro del proyecto; ubicación exacta aún no determinada.

### 8. Directory structure
```text
Directorio futuro no fijado:
├── AGENTS.md
└── artefacto de workflow correspondiente
```

### 9. Required concepts
- Concepto: Decisión conjunta de herramienta, contexto y prompt; loops integrados.
- Explicación necesaria: Decisión conjunta de herramienta, contexto y prompt; loops integrados.. Debe poder aplicarse sin regresar a M1 para descubrir los pasos básicos.
- Nivel requerido para ejecutar el paso: Suficiente para ejecutar y validar la unidad en una sesión futura.

### 10. Commands
```text
NO APLICA en Chat 2.
```
- Ubicación desde la que se ejecuta cada comando: Solo futuro entorno del proyecto.
- Resultado esperado: La futura ejecución respeta permisos y alcance definidos.
- Verificación: Comprobar salida contra criterios de aceptación y límites de seguridad.

### 11. Code
```text
NO APLICA durante Chat 2.
```
- Propósito: Preparar workflow/documentación, no implementar producto.
- Partes relevantes: NO APLICA o, cuando corresponda, patrón/criterio que se convertirá en artefacto futuro.
- Personalización requerida: Adaptar al proyecto real solo cuando exista el entorno y sus contratos.

### 12. Action
- Acción concreta que se realizará: Resolver A–E y una tarea SRE mediante el framework completo y conservar trazabilidad.
- Orden de ejecución: 1) caracterizar; 2) herramienta; 3) contexto; 4) prompt; 5) patrón; 6) validar; 7) aprender.
- Entrada utilizada: Tarea, contexto y restricciones de la unidad.
- Salida producida: Registro integrado por caso + playbook combinado.

### 13. Reason
- Por qué se realiza esta acción: La integración es una capacidad propia de M1; sin ella los tres pilares quedarían aislados.
- Qué problema resuelve: Evita decisiones desconectadas y permite comprobar el workflow completo.
- Por qué corresponde a M1: Corresponde al bloque de integración y casos A–E del Pilar 3.

### 14. Expected result
- Resultado esperado: Los cinco casos quedan desarrollados y una aplicación SRE produce una salida nueva y verificable.
- Estado esperado: PLANIFICADO
- Evidencia esperada: Solo evidencia de fuente y planificación; el resultado operativo será evidencia futura.
- Memoria incremental del paso: Se generará en una ejecución futura como snapshot acumulativo; Chat 2 no fabrica ese ZIP.

### 15. Evidence
- Evidencia que demuestra el resultado: Registro futuro del artefacto, pruebas y validación.
- Fuente de la evidencia: M1 files 2–4; contexto SRE de referencia y límites heredados.
- Cómo se conservará: Versionar artefacto, evidencia y referencias de procedencia.

### 16. Validation
- Qué se debe verificar: Los cinco casos quedan desarrollados y una aplicación SRE produce una salida nueva y verificable.
- Cómo se verifica: Recorrer la unidad con sus pruebas concretas y verificar fuente, salida y estado.
- Resultado esperado de la validación: PASS cuando la evidencia futura cumpla los criterios; en Chat 2 el estado permanece PLANIFICADO.

### 17. Acceptance criteria
- Criterio 1: PASS si están conectados.
- Criterio 2: PASS si no se saltan fronteras.
- Criterio 3: PASS si se distingue hecho de inferencia.

### 18. Tests
- ID de prueba: `M1-P07-T01`
- Capacidad/subcapacidad cubierta: Caso A
- Prueba: Resolver A completo.
- Entrada: Caso A + fuentes permitidas.
- Resultado esperado: Registro de tool/context/prompt/patrón/validación.
- Condición de aprobación: PASS si están conectados.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P07-T02`
- Capacidad/subcapacidad cubierta: Caso B
- Prueba: Resolver B completo.
- Entrada: Caso B + contexto.
- Resultado esperado: Trazabilidad completa.
- Condición de aprobación: PASS si no se saltan fronteras.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P07-T03`
- Capacidad/subcapacidad cubierta: Caso C
- Prueba: Resolver C completo.
- Entrada: Caso C + restricciones.
- Resultado esperado: Adaptación del framework.
- Condición de aprobación: PASS si se distingue hecho de inferencia.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P07-T04`
- Capacidad/subcapacidad cubierta: Caso D
- Prueba: Resolver D completo.
- Entrada: Caso D + contexto.
- Resultado esperado: Salida verificable.
- Condición de aprobación: PASS si existe criterio de aprobación.
- Estado de la prueba durante Chat 2: PLANIFICADA

- ID de prueba: `M1-P07-T05`
- Capacidad/subcapacidad cubierta: Caso E + SRE
- Prueba: Resolver E y aplicar framework a tarea SRE read-only.
- Entrada: E + tarea SRE.
- Resultado esperado: Decisión operacional nueva sin mutación.
- Condición de aprobación: PASS si la salida es trazable y read-only.
- Estado de la prueba durante Chat 2: PLANIFICADA


### 19. Expected errors
- Error plausible 1: Cobertura nominal
- Cuándo podría aparecer: Solo enumerar casos.
- Síntoma: No existe desarrollo integrado.
- Error plausible 2: Pérdida de integración
- Cuándo podría aparecer: Pilares tratados por separado.
- Síntoma: No hay decisión conjunta.
- Error plausible 3: Aplicación inventada
- Cuándo podría aparecer: Se agregan requisitos no respaldados.
- Síntoma: Escenario sin procedencia.

### 20. Detection
- Revisar la evidencia observable indicada en las pruebas.
- Comparar salida con criterios y con el estado de entrada.

### 21. Meaning
- El resultado indica si la unidad conservó la capacidad de M1 sin compresión indebida.

### 22. Diagnosis
- Causa probable: desviación respecto del procedimiento o pérdida de información crítica.
- Evidencia que confirma o descarta la causa: entrada, salida, prueba y fuente de M1.
- Orden de diagnóstico: fuente → capacidad → actividad → salida → validación.

### 23. Correction
- Corrección: Corregir el procedimiento o el artefacto que originó la desviación.
- Acción concreta: Rehacer la actividad con evidencia de M1 y volver a ejecutar las pruebas afectadas.
- Verificación posterior: Repetir la validación de la unidad y confirmar PASS.
- Riesgos de la corrección: La corrección puede afectar dependencias posteriores; debe volver a auditarse si cambia la frontera.

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
- M1 → archivo → sección/tema → concepto: ['`2. Pilar 1 — La Herramienta.md`', '`3. Pilar 2 — El Contexto.md`', '`4. Pilar 3 — El Prompt + Integración.md`'] → Framework combinado; casos canónicos A–E; anti-patterns combinados; meta-insight; integración tool/context/prompt. → Decisión conjunta de herramienta, contexto y prompt; loops integrados.
- Concepto → actividad: Decisión conjunta de herramienta, contexto y prompt; loops integrados. → Resolver A–E y una tarea SRE mediante el framework completo y conservar trazabilidad.
- Actividad → paso: Resolver A–E y una tarea SRE mediante el framework completo y conservar trazabilidad. → `M1-P07`
- Paso → artefacto: `M1-P07` → Playbook combinado y registros futuros de A–E.
- Paso → evidencia: `M1-P07` → Registro futuro del artefacto, pruebas y validación. (futura)
- Paso → validación: `M1-P07` → Los cinco casos quedan desarrollados y una aplicación SRE produce una salida nueva y verificable.
- Paso → memoria ZIP incremental: `M1-P07` → Se generará en una ejecución futura como snapshot acumulativo; Chat 2 no fabrica ese ZIP.
- Paso → siguiente paso: FIN DEL PLAN M1 — continuar en ejecución futura según roadmap.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: Fuentes externas, fecha, URL/recurso y afirmación: consultar `knowledge/references/reference-index.md` y `knowledge/facts/external-research.md` cuando corresponda.

### 26. State
- Estado inicial: PLANIFICADO
- Estado final esperado: PLANIFICADO, listo para ejecución futura tras prerrequisitos.
- Estado real: PLANIFICADO; no ejecutado en Chat 2.
- Qué queda pendiente: Ejecutar posteriormente y conservar evidencia.
- Relación con el siguiente paso: FIN DEL PLAN M1 — continuar en ejecución futura según roadmap.
