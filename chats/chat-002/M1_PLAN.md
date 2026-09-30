# Plan M1 — Chat 002

## Estado del plan

**CONGELADO — PLANIFICADO**. La ejecución de Chat 2 terminó en diseño, auditoría y preparación de memoria. El Paso 1 del proyecto nuevo no se ejecutó.

## Determinación dinámica del conjunto

La cantidad final es consecuencia del análisis del contenido completo de M1 y de sus unidades profesionales: caracterización de tarea, selección/evaluación de herramienta, contexto persistente, operación de contexto, prompting, patrones de ejecución e integración. La referencia a una descomposición previa se utilizó solo como regresión de calidad, no como objetivo numérico.

## Secuencia estabilizada

`M1-P01 → M1-P02 → M1-P03 → M1-P04 → M1-P05 → M1-P06 → M1-P07`

## Control de alcance

| Tratamiento | Elementos |
|---|---|
| APLICAR AHORA POR MÓDULO 1 | caracterización, decisión de modo, criterios de herramienta, arquitectura de contexto, operación de contexto, prompting y patrones de ejecución |
| PREPARAR COMO BASE PARA FUTURO | `AGENTS.md`, contratos de prompt, playbooks, pruebas y documentación de workflow |
| RESERVAR PARA MÓDULO POSTERIOR | implementación completa de LangChain/LangGraph, RAG, PostgreSQL/Redis, FastAPI, Streamlit/React, Prometheus/Loki/OTel, GitHub/AWS/Kubernetes/Slack/Alertmanager, CI/CD/IaC |
| HUECO / EVIDENCIA PENDIENTE | modelo/proveedor exacto, SRE operating model, executor isolation detallado, corpus de incidentes, rúbrica de evaluación y otros OQ heredados |

## Integración con el objetivo SRE

M1 no implementa intake, deduplicación, estado durable, RAG, remediación, recuperación, observabilidad ni despliegue. Prepara la forma profesional en que una IA asistida por harness, contexto y prompts trabajará sobre esas capacidades después.

## Regla temporal

`DiiegoA/Agente_SRE_DevOps_para_respuesta_a_incidentes` fue observado vacío y quedó intacto. No se creó código, archivo ni commit allí. Todo artefacto del proyecto que aparece en los pasos es futuro y se generará solamente en una copia de trabajo independiente cuando el paso sea ejecutado.

## Resultado

Plan M1 congelado, todos los pasos en `PLANIFICADO`, y auditorías estructural/semántica en PASS.


---

## Paso 01 — Caracterizar la tarea y seleccionar el modo de trabajo

### 1. Identification
- ID del paso: `M1-P01`
- Fase: Fase A — Construcción cognitiva del plan
- Subfase: Caracterización operativa
- Estado: PLANIFICADO
- Tipo de paso: Unidad de trabajo profesional de M1; preparación futura, no ejecución productiva.

### 2. Objective
- Objetivo exacto del paso: Convertir solicitudes de ingeniería del proyecto SRE en un perfil de tarea y decidir explícitamente cuándo corresponde completion o agentic.

### 3. Direct relation to M1
- Archivo(s) de M1: `1. El modelo mental de los 3 pilares.md`; `2. Pilar 1 — La Herramienta.md`
- Sección(es)/tema(s): Modelo mental de los tres pilares; Categorías A-D; Diferencia completion vs agentic; reglas para cambiar de modo
- Concepto(s) de M1: harness, unidad de trabajo, control humano, completion, agentic, tareas multi-archivo y ejecución de comandos
- Relación directa: M1 exige caracterizar la tarea antes de elegir herramienta. El resultado se aplica a escenarios reales del agente SRE, no a un ejercicio genérico.

### 4. Prerequisites
- Conocimientos previos: Comprender el modelo mental de M1 y disponer del objetivo SRE heredado.
- Condiciones previas: Conocer el flujo del proyecto y no confundir escenario de referencia con estado implementado.
- Evidencia o artefactos necesarios: M1 auditado y `knowledge/facts/chat-002-sre-reference.md`.

### 5. Dependencies
- Depende de: INDEPENDIENTE dentro de M1
- Habilita: M1-P02
- Tipo de dependencia: Dependencia funcional de clasificación
- Riesgo si se altera el orden: Elegir modo incorrecto produce overhead innecesario o inconsistencias de edición/validación.

### 6. Preparation
- Preparación necesaria: Registrar escenarios representativos: cambio aislado, cambio multi-archivo, tarea con comandos/tests y exploración.
- Entorno: Copia de trabajo independiente; repositorios externos en modo lectura.
- Información que debe estar disponible: Estado de Chat 1, fuente M1 y SRE reference del objetivo.

### 7. Files
- Archivos que se leerán: M1 archivos 1-2; estado/decisiones de Chat 1; SRE reference summary.
- Archivos que se crearán en la ejecución futura: `docs/m1/task-characterization.md`
- Archivos que se modificarían en la ejecución futura: NO APLICA en Chat 2; la creación futura ocurre solo en la copia del proyecto.
- Ubicación exacta de cada archivo: `docs/m1/task-characterization.md`

### 8. Directory structure
```text
docs/m1/task-characterization.md
```

### 9. Required concepts
- Concepto: Categorías A-D; unidad de trabajo; completion; agentic; cuándo cambiar de modo; latencia y tamaño de tarea.
- Explicación necesaria: Desarrollar cada elemento sin esconder partes diferenciadas tras una palabra paraguas.
- Nivel requerido para ejecutar el paso: Aplicación práctica con validación humana.

### 10. Commands
NO APLICA: la actividad puede resolverse mediante artefacto de clasificación y pruebas futuras.
- Ubicación desde la que se ejecuta cada comando: Raíz del proyecto de trabajo futuro.
- Resultado esperado: Resultado futuro debe coincidir con el artefacto y criterios del paso.
- Verificación: Revisión contra criterios de aceptación y prueba concreta.

### 11. Code
NO APLICA: no se implementa código productivo.
- Propósito: Mecanismo de validación futura, cuando corresponda.
- Partes relevantes: Partes de la comprobación necesarias para el objetivo del paso.
- Personalización requerida: Adaptar rutas/configuración al proyecto real en ejecución futura.

### 12. Action
- Acción concreta que se realizará: Crear una ficha de caracterización con alcance, número de archivos/capas, necesidad de comandos, exploración y tiempo; aplicarla a escenarios SRE.
- Orden de ejecución: Reclasificar desde las cuatro dimensiones antes de continuar.
- Entrada utilizada: Tres escenarios textuales definidos para el proyecto SRE.
- Salida producida: Una ficha reproducible que distingue completion de agentic y deja trazada la razón en cada escenario.

### 13. Reason
- Por qué se realiza esta acción: M1 establece que primero se determina la tarea y el nivel de control humano; la herramienta cae como consecuencia.
- Qué problema resuelve: Reduce improvisación, contaminación o trabajo no verificable.
- Por qué corresponde a M1: Transforma directamente una capacidad de M1 en una práctica.

### 14. Expected result
- Resultado esperado: Una ficha reproducible que distingue completion de agentic y deja trazada la razón en cada escenario.
- Estado esperado: PLANIFICADO y listo para ejecución futura.
- Evidencia esperada: Evidencia futura especificada en Evidence/Tests.
- Memoria incremental del paso: ZIP incremental del paso: se generará únicamente cuando el paso sea ejecutado en una sesión futura; NO se genera en Chat 2.

### 15. Evidence
- Evidencia que demuestra el resultado: M1 como evidencia documental observada; ficha y pruebas como evidencia futura.
- Fuente de la evidencia: M1 auditado + SRE reference + continuidad de Chat 1.
- Cómo se conservará: En el repositorio de trabajo cuando se ejecute; en memoria acumulativa después de ejecución.

### 16. Validation
- Qué se debe verificar: Aplicar dos veces la misma ficha al mismo escenario y comprobar clasificación y justificación estables.
- Cómo se verifica: Revisión documental + prueba definida en Tests.
- Resultado esperado de la validación: PASS solo con cumplimiento concreto; FAIL requiere corrección y repetición.

### 17. Acceptance criteria
- Criterio 1: Cada escenario tiene modo recomendado y razón.
- Criterio 2: La clasificación sigue reglas concretas de M1.
- Criterio 3: No se fija proveedor o modelo como decisión.

### 18. Tests
- ID de prueba: M1-T01-01
- Capacidad/subcapacidad cubierta: Clasificación de modo
- Prueba: Aplicar la ficha a un cambio aislado, un cambio multi-archivo y una tarea con migración/tests.
- Entrada: Tres escenarios textuales definidos para el proyecto SRE.
- Resultado esperado: Aislado → completion; multi-archivo y con comandos → agentic, justificando por alcance y ejecución.
- Condición de aprobación: PASS si las tres salidas siguen las reglas de modo de M1 y la justificación es específica.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Clasificar todo como agentic por ser un proyecto SRE.
- Cuándo podría aparecer: Al completar la matriz.
- Síntoma: La salida ignora alcance y necesidad de comandos.

### 20. Detection
- Cómo detectar el error: Comparar cada fila con las reglas de M1.
- Evidencia del error: Modo asignado sin correspondencia con la tarea.
- Señal observable: Clasificación idéntica para tareas con complejidad distinta.

### 21. Meaning
- Qué significa el error o resultado: Indica traducción nominal del pilar Herramienta.
- Qué parte del proceso afecta: Selección del harness y workflow posterior.

### 22. Diagnosis
- Causa probable: Uso de etiqueta de proyecto en lugar de criterios de M1.
- Evidencia que confirma o descarta la causa: Revisar alcance, archivos, comandos y tiempo.
- Orden de diagnóstico: Reclasificar desde las cuatro dimensiones antes de continuar.

### 23. Correction
- Corrección: Reescribir la fila según criterios de M1; repetir M1-T01-01.
- Acción concreta: No crear código ni cambiar repos externos.
- Verificación posterior: PASS solo tras consistencia.
- Riesgos de la corrección: Generalizar puede crear una dependencia artificial con P02.

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
- M1 → archivo → sección/tema → concepto: M1 archivo 1 → tres pilares co-iguales; M1 archivo 2 → categorías A-D y completion/agentic.
- Concepto → actividad: Conceptos de modo → ficha de caracterización.
- Actividad → paso: ficha → M1-P01.
- Paso → artefacto: M1-P01 → `docs/m1/task-characterization.md`.
- Paso → evidencia: Observada: contenido de M1; futura: ficha/test.
- Paso → validación: Validación por M1-T01-01.
- Paso → memoria ZIP incremental: Planificado; no generado durante Chat 2.
- Paso → siguiente paso: M1-P02 consume la clasificación.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: 2026-09-30; `Diiegoal/CursoIA`/main; fuente M1 consultada en Chat 2.

### 26. State
- Estado inicial: Conocimiento de Chat 1 recuperado; paso no iniciado.
- Estado final esperado: Ficha de caracterización lista para alimentar selección de herramienta.
- Estado real: PLANIFICADO; no ejecutado.
- Qué queda pendiente: Ejecución futura y captura de evidencia real.
- Relación con el siguiente paso: Ficha de caracterización lista para alimentar selección de herramienta.

---

## Paso 02 — Seleccionar y evaluar la herramienta con los criterios de M1

### 1. Identification
- ID del paso: `M1-P02`
- Fase: Fase A — Construcción cognitiva del plan
- Subfase: Selección de harness
- Estado: PLANIFICADO
- Tipo de paso: Unidad de trabajo profesional de M1; preparación futura, no ejecución productiva.

### 2. Objective
- Objetivo exacto del paso: Aplicar categorías A-D y los cinco criterios de M1 para definir el perfil de herramienta/harness requerido por el proyecto, sin convertir el modelo o vendor en la decisión.

### 3. Direct relation to M1
- Archivo(s) de M1: `2. Pilar 1 — La Herramienta.md`
- Sección(es)/tema(s): Categorías A-D; completion vs agentic; cinco criterios; modelos; benchmarks; decision tree; anti-patterns
- Concepto(s) de M1: tamaño/forma del codebase, lenguaje, privacidad/compliance, presupuesto, estilo del developer, benchmarks y harness
- Relación directa: M1 aporta una matriz práctica de selección. Se usa sobre el perfil producido en P01 y sobre el contexto real del proyecto.

### 4. Prerequisites
- Conocimientos previos: M1-P01 y conocimiento del objetivo SRE.
- Condiciones previas: Mantener separadas categoría, modelo y proveedor.
- Evidencia o artefactos necesarios: M1 archivo 2 y estado/decisiones de Chat 1.

### 5. Dependencies
- Depende de: M1-P01
- Habilita: M1-P03
- Tipo de dependencia: Dependencia de decisión
- Riesgo si se altera el orden: Seleccionar por benchmark único o por modelo puede producir un harness inadecuado.

### 6. Preparation
- Preparación necesaria: Aplicar los cinco criterios al proyecto y registrar datos desconocidos como abiertos.
- Entorno: Copia de trabajo independiente; repositorios externos en modo lectura.
- Información que debe estar disponible: Estado de Chat 1, fuente M1 y SRE reference del objetivo.

### 7. Files
- Archivos que se leerán: M1 archivo 2; P01; SRE reference summary; DEC-0001..0006.
- Archivos que se crearán en la ejecución futura: `docs/m1/tool-selection-matrix.md`
- Archivos que se modificarían en la ejecución futura: NO APLICA.
- Ubicación exacta de cada archivo: `docs/m1/tool-selection-matrix.md`

### 8. Directory structure
```text
docs/m1/tool-selection-matrix.md
```

### 9. Required concepts
- Concepto: Categoría A IDE-integrated (visual + diff inline); Categoría B terminal/CLI agentic; Categoría C standalone autonomous agents; Categoría D especializados; completion vs agentic; cinco criterios (tamaño/forma del codebase, lenguaje, privacidad/compliance, presupuesto, estilo del developer); snapshot de modelos (Claude Code, Cursor, GitHub Copilot, Windsurf, Cline/Aider/OpenCode y los modelos citados por M1); benchmarks SWE-Bench Verified, SWE-Bench Pro, Aider Polyglot y Terminal-Bench 2.0; árbol de decisión; anti-patterns documentados.
- Explicación necesaria: Cada categoría se conserva con su modo de interacción, unidad de trabajo, latencia tolerable, mejor uso y ejemplos; los cinco criterios se contestan uno por uno; la disponibilidad de modelos se registra como snapshot temporal y no como criterio suficiente; los benchmarks se usan como evidencia auxiliar y no como selector único; los anti-patterns se traducen a reglas accionables.
- Nivel requerido para ejecutar el paso: Aplicación práctica con validación humana.

### 10. Commands
NO APLICA: selección documental en Chat 2.
- Ubicación desde la que se ejecuta cada comando: Raíz del proyecto de trabajo futuro.
- Resultado esperado: Resultado futuro debe coincidir con el artefacto y criterios del paso.
- Verificación: Revisión contra criterios de aceptación y prueba concreta.

### 11. Code
NO APLICA: no hay implementación productiva.
- Propósito: Mecanismo de validación futura, cuando corresponda.
- Partes relevantes: Partes de la comprobación necesarias para el objetivo del paso.
- Personalización requerida: Adaptar rutas/configuración al proyecto real en ejecución futura.

### 12. Action
- Acción concreta que se realizará: Construir una matriz por escenario que primero clasifique el modo completion/agentic, después compare las cuatro categorías A-D y finalmente aplique, en este orden operativo, tamaño/forma del codebase → lenguaje → privacidad/compliance → presupuesto → estilo del developer; registrar el snapshot de modelos solo como disponibilidad y usar SWE-Bench Verified, SWE-Bench Pro, Aider Polyglot y Terminal-Bench 2.0 como señales comparativas.
- Orden de ejecución: Caracterizar tarea → elegir modo/categoría → filtrar privacidad/compliance → contrastar codebase/lenguaje → contrastar presupuesto/estilo → interpretar benchmarks → aplicar anti-patterns → dejar explícita la decisión o cuestión abierta.
- Entrada utilizada: Perfil P01 + read-only-first + objetivo SRE + restricciones heredadas.
- Salida producida: Matriz reproducible que documenta categoría, modo, cinco criterios, snapshot de disponibilidad de modelos, evidencia de benchmarks, anti-patterns descartados y nivel de certeza; no fija proveedor/modelo exacto.

### 13. Reason
- Por qué se realiza esta acción: Evita confundir disponibilidad de modelo con adecuación del harness.
- Qué problema resuelve: Reduce improvisación, contaminación o trabajo no verificable.
- Por qué corresponde a M1: Transforma directamente una capacidad de M1 en una práctica.

### 14. Expected result
- Resultado esperado: Matriz reproducible y perfil de herramienta; la categoría B agentic puede quedar como propuesta para tareas largas, sin fijar proveedor.
- Estado esperado: PLANIFICADO y listo para ejecución futura.
- Evidencia esperada: Evidencia futura especificada en Evidence/Tests.
- Memoria incremental del paso: ZIP incremental del paso: se generará únicamente cuando el paso sea ejecutado en una sesión futura; NO se genera en Chat 2.

### 15. Evidence
- Evidencia que demuestra el resultado: M1 observada; resultado del proyecto marcado como PROPUESTA.
- Fuente de la evidencia: M1 auditado + SRE reference + continuidad de Chat 1.
- Cómo se conservará: En el repositorio de trabajo cuando se ejecute; en memoria acumulativa después de ejecución.

### 16. Validation
- Qué se debe verificar: Comprobar que los cinco criterios están contestados y que ningún benchmark aislado decide el resultado.
- Cómo se verifica: Revisión documental + prueba definida en Tests.
- Resultado esperado de la validación: PASS solo con cumplimiento concreto; FAIL requiere corrección y repetición.

### 17. Acceptance criteria
- Criterio 1: A-D aparecen diferenciadas.
- Criterio 2: Los cinco criterios tienen tratamiento explícito.
- Criterio 3: Proveedor/modelo exacto queda no determinado salvo evidencia heredada.

### 18. Tests
- ID de prueba: M1-T02-01
- Capacidad/subcapacidad cubierta: Selección condicionada
- Prueba: Aplicar la matriz a una investigación SRE multi-archivo con tests y exploración.
- Entrada: Perfil P01 + read-only-first + objetivo SRE.
- Resultado esperado: Categoría agentic apropiada para tareas largas; cada criterio queda justificado; proveedor queda abierto.
- Condición de aprobación: PASS si las cinco dimensiones están resueltas y no se usa un único score como decisión.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: “El modelo con mayor score define la herramienta”.
- Cuándo podría aparecer: Al completar la comparación.
- Síntoma: La matriz se reduce a benchmark/modelo.

### 20. Detection
- Cómo detectar el error: Revisión de columnas.
- Evidencia del error: Falta de criterios de privacidad/codebase/estilo.
- Señal observable: Justificación sin información del proyecto.

### 21. Meaning
- Qué significa el error o resultado: Selección por disponibilidad en lugar de harness.
- Qué parte del proceso afecta: Arquitectura operativa del copiloto.

### 22. Diagnosis
- Causa probable: Confusión modelo-harness.
- Evidencia que confirma o descarta la causa: Releer cinco criterios.
- Orden de diagnóstico: Aplicar filtros de riesgo y tarea antes del benchmark.

### 23. Correction
- Corrección: Completar dimensiones faltantes y repetir P02.
- Acción concreta: Mantener la salida como propuesta.
- Verificación posterior: M1-T02-01 PASS.
- Riesgos de la corrección: Fijar proveedor ahora cerraría opciones sin evidencia.

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
- M1 → archivo → sección/tema → concepto: M1 archivo 2 → categorías A-D, cinco criterios, benchmarks, framework y anti-patterns.
- Concepto → actividad: criterios → matriz.
- Actividad → paso: matriz → P02.
- Paso → artefacto: P02 → `docs/m1/tool-selection-matrix.md`.
- Paso → evidencia: Observada/futura.
- Paso → validación: M1-T02-01.
- Paso → memoria ZIP incremental: Planificado; no generado durante Chat 2.
- Paso → siguiente paso: M1-P03 consume el perfil de harness.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: 2026-09-30; M1 archivo 2; GitHub read-only.

### 26. State
- Estado inicial: Conocimiento de Chat 1 recuperado; paso no iniciado.
- Estado final esperado: Perfil de herramienta/harness documentado como propuesta condicionada.
- Estado real: PLANIFICADO; no ejecutado.
- Qué queda pendiente: Ejecución futura y captura de evidencia real.
- Relación con el siguiente paso: Perfil de herramienta/harness documentado como propuesta condicionada.

---

## Paso 03 — Diseñar la arquitectura de contexto persistente

### 1. Identification
- ID del paso: `M1-P03`
- Fase: Fase B — Context Engineering
- Subfase: Contexto persistente
- Estado: PLANIFICADO
- Tipo de paso: Unidad de trabajo profesional de M1; preparación futura, no ejecución productiva.

### 2. Objective
- Objetivo exacto del paso: Diseñar el mínimo contexto persistente de alta señal para que el agente de desarrollo pueda trabajar de forma coherente sobre el proyecto SRE.

### 3. Direct relation to M1
- Archivo(s) de M1: `3. Pilar 2 — El Contexto.md`
- Sección(es)/tema(s): Tipos de contexto; AGENTS.md; comparativa de mecanismos; buenas prácticas de contenido persistente
- Concepto(s) de M1: AGENTS.md, overview, stack, convenciones, comandos, gotchas, versionado, alta señal, vendor wrappers
- Relación directa: M1 convierte contexto persistente en una pieza de infraestructura cognitiva. Chat 2 prepara el diseño, no lo instala en el repositorio externo.

### 4. Prerequisites
- Conocimientos previos: P01-P02 y decisiones de memoria/seguridad de Chat 1.
- Condiciones previas: Separar memoria de continuidad, estado operativo y contexto persistente.
- Evidencia o artefactos necesarios: M1 archivo 3 y `MEMORY_PROTOCOL.md`/decisiones heredadas.

### 5. Dependencies
- Depende de: M1-P01 y M1-P02
- Habilita: M1-P04
- Tipo de dependencia: Dependencia arquitectónica
- Riesgo si se altera el orden: Un AGENTS.md demasiado largo o con estado volátil puede contaminar cada sesión.

### 6. Preparation
- Preparación necesaria: Definir secciones de alta señal y límites de contenido.
- Entorno: Copia de trabajo independiente; repositorios externos en modo lectura.
- Información que debe estar disponible: Estado de Chat 1, fuente M1 y SRE reference del objetivo.

### 7. Files
- Archivos que se leerán: M1 archivo 3; memoria/protocolo/decisiones de Chat 1; P01-P02.
- Archivos que se crearán en la ejecución futura: `AGENTS.md`; `docs/m1/context-architecture.md`
- Archivos que se modificarían en la ejecución futura: NO APLICA.
- Ubicación exacta de cada archivo: `AGENTS.md`; `docs/m1/context-architecture.md`

### 8. Directory structure
```text
AGENTS.md
docs/m1/context-architecture.md
```

### 9. Required concepts
- Concepto: código relevante; convenciones del proyecto; estado actual; intent/spec; restricciones; memoria persistente; documentación externa; histórico de sesión; `AGENTS.md`; `CLAUDE.md`; `.cursorrules`/`.cursor/rules/*.mdc`; `.clinerules`; `.github/copilot-instructions.md`; mínimo/alta señal; comandos clave; convenciones positivas y negativas; versionado; hooks deterministas.
- Explicación necesaria: Cada tipo de contexto se clasifica por qué aporta y qué debe quedar fuera; `AGENTS.md` se diseña como fuente portátil de alta señal, con wrappers vendor-specific solo cuando aporten compatibilidad y sin duplicar el contenido.
- Nivel requerido para ejecutar el paso: Aplicación práctica con validación humana.

### 10. Commands
```text
Python validation futura: comprobar existencia de AGENTS.md y <=200 líneas.
```
- Ubicación desde la que se ejecuta cada comando: Raíz del proyecto de trabajo futuro.
- Resultado esperado: Resultado futuro debe coincidir con el artefacto y criterios del paso.
- Verificación: Revisión contra criterios de aceptación y prueba concreta.

### 11. Code
```text
from pathlib import Path
p = Path("AGENTS.md")
assert p.exists()
assert len(p.read_text(encoding="utf-8").splitlines()) <= 200
```
- Propósito: Mecanismo de validación futura, cuando corresponda.
- Partes relevantes: Partes de la comprobación necesarias para el objetivo del paso.
- Personalización requerida: Adaptar rutas/configuración al proyecto real en ejecución futura.

### 12. Action
- Acción concreta que se realizará: Definir la política de `AGENTS.md` con `Project overview`, `Stack y versiones`, `Convenciones`, `Comandos clave` y `Gotchas`; clasificar por separado código relevante, convenciones, estado, intent/spec, restricciones, memoria persistente, documentación externa e histórico; decidir qué información se referencia mediante path/URL en vez de copiarse.
- Orden de ejecución: Clasificar tipo de contexto → seleccionar información de alta señal → eliminar estado volátil/duplicación/secretos → definir versionado → definir wrappers vendor-specific solo si son necesarios.
- Entrada utilizada: M1 archivo 3 + decisiones de memoria de Chat 1 + SRE reference.
- Salida producida: Especificación verificable de `AGENTS.md`, reglas de mantenimiento y arquitectura de contexto persistente.

### 13. Reason
- Por qué se realiza esta acción: M1 indica que el contexto persistente debe ser corto, de alta señal y tratado como código.
- Qué problema resuelve: Reduce improvisación, contaminación o trabajo no verificable.
- Por qué corresponde a M1: Transforma directamente una capacidad de M1 en una práctica.

### 14. Expected result
- Resultado esperado: Especificación verificable de AGENTS.md y arquitectura de contexto.
- Estado esperado: PLANIFICADO y listo para ejecución futura.
- Evidencia esperada: Evidencia futura especificada en Evidence/Tests.
- Memoria incremental del paso: ZIP incremental del paso: se generará únicamente cuando el paso sea ejecutado en una sesión futura; NO se genera en Chat 2.

### 15. Evidence
- Evidencia que demuestra el resultado: Observada: M1; futura: archivo AGENTS.md y validator.
- Fuente de la evidencia: M1 auditado + SRE reference + continuidad de Chat 1.
- Cómo se conservará: En el repositorio de trabajo cuando se ejecute; en memoria acumulativa después de ejecución.

### 16. Validation
- Qué se debe verificar: Revisar secciones, longitud, ausencia de secretos y separación de memoria.
- Cómo se verifica: Revisión documental + prueba definida en Tests.
- Resultado esperado de la validación: PASS solo con cumplimiento concreto; FAIL requiere corrección y repetición.

### 17. Acceptance criteria
- Criterio 1: Incluye overview/stack/conventions/commands/gotchas.
- Criterio 2: <=200 líneas.
- Criterio 3: No contiene memoria episódica volátil.

### 18. Tests
- ID de prueba: M1-T03-01
- Capacidad/subcapacidad cubierta: Contexto persistente
- Prueba: Generar un AGENTS.md futuro desde la especificación y ejecutar el validador.
- Entrada: Borrador controlado + secciones requeridas.
- Resultado esperado: Secciones presentes, <=200 líneas, sin secretos ni estado volátil.
- Condición de aprobación: PASS si todas las condiciones cumplen.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Convertir AGENTS.md en depósito de toda la documentación.
- Cuándo podría aparecer: Al redactar el archivo.
- Síntoma: Archivo excesivamente largo/duplicado.

### 20. Detection
- Cómo detectar el error: Contar líneas y revisar secciones.
- Evidencia del error: Logs/runbooks completos dentro del archivo.
- Señal observable: Mucho contenido de baja señal.

### 21. Meaning
- Qué significa el error o resultado: Confusión entre contexto persistente y conocimiento completo.
- Qué parte del proceso afecta: Ventana inicial de todas las sesiones.

### 22. Diagnosis
- Causa probable: Falta de curación.
- Evidencia que confirma o descarta la causa: Comparar con buenas prácticas de M1.
- Orden de diagnóstico: Reducir y separar información.

### 23. Correction
- Corrección: Acotar el archivo y desplazar estado/documentación a sus fuentes.
- Acción concreta: No editar repositorio externo.
- Verificación posterior: Repetir M1-T03-01.
- Riesgos de la corrección: Eliminar información necesaria por exceso de compactación.

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
- M1 → archivo → sección/tema → concepto: M1 archivo 3 → AGENTS.md, mecanismos y buenas prácticas.
- Concepto → actividad: tipos de contexto → arquitectura persistente.
- Actividad → paso: arquitectura → P03.
- Paso → artefacto: P03 → AGENTS.md + context-architecture.
- Paso → evidencia: Documental observada; artefactos futuros.
- Paso → validación: Validator futuro.
- Paso → memoria ZIP incremental: Planificado; no generado durante Chat 2.
- Paso → siguiente paso: M1-P04 consume el esquema de contexto.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: 2026-09-30; M1 archivo 3 en `Diiegoal/CursoIA`/main.

### 26. State
- Estado inicial: Conocimiento de Chat 1 recuperado; paso no iniciado.
- Estado final esperado: Arquitectura de contexto persistente definida y lista para operación.
- Estado real: PLANIFICADO; no ejecutado.
- Qué queda pendiente: Ejecución futura y captura de evidencia real.
- Relación con el siguiente paso: Arquitectura de contexto persistente definida y lista para operación.

---

## Paso 04 — Gestionar operativamente la ventana y evitar context rot

### 1. Identification
- ID del paso: `M1-P04`
- Fase: Fase B — Context Engineering
- Subfase: Operación contextual
- Estado: PLANIFICADO
- Tipo de paso: Unidad de trabajo profesional de M1; preparación futura, no ejecución productiva.

### 2. Objective
- Objetivo exacto del paso: Convertir context rot y las estrategias Write/Select/Compress/Isolate de M1 en un procedimiento operativo aplicable a sesiones agentic del proyecto.

### 3. Direct relation to M1
- Archivo(s) de M1: `3. Pilar 2 — El Contexto.md`
- Sección(es)/tema(s): Context rot; mecanismos; tipos de contexto; Write/Select/Compress/Isolate; kit operativo
- Concepto(s) de M1: lost in the middle, attention dilution, distractor interference, 50/70/90 como heurísticas, curación, sub-agents, compact/restart
- Relación directa: Separa la arquitectura persistente de la gestión dinámica de la ventana y desarrolla cada mecanismo/estrategia como acción.

### 4. Prerequisites
- Conocimientos previos: M1-P03.
- Condiciones previas: Tratar 50/70/90 como heurísticas del material, no como límites oficiales universales.
- Evidencia o artefactos necesarios: M1 archivo 3.

### 5. Dependencies
- Depende de: M1-P03
- Habilita: M1-P05
- Tipo de dependencia: Dependencia operacional
- Riesgo si se altera el orden: Acumular ruido puede provocar pérdida de coherencia y duplicación de trabajo.

### 6. Preparation
- Preparación necesaria: Definir escenarios de ocupación y decisiones de contexto.
- Entorno: Copia de trabajo independiente; repositorios externos en modo lectura.
- Información que debe estar disponible: Estado de Chat 1, fuente M1 y SRE reference del objetivo.

### 7. Files
- Archivos que se leerán: M1 archivo 3; `docs/m1/context-architecture.md` futuro.
- Archivos que se crearán en la ejecución futura: `docs/m1/context-operations.md`
- Archivos que se modificarían en la ejecución futura: NO APLICA.
- Ubicación exacta de cada archivo: `docs/m1/context-operations.md`

### 8. Directory structure
```text
docs/m1/context-operations.md
```

### 9. Required concepts
- Concepto: `Lost in the Middle`; `Attention dilution`; `Distractor interference`; degradación antes de llenar la ventana; heurísticas ~50% / ~70% / ~90%; curación activa; `Write`; `Select`; `Compress`; `Isolate`; agentic search; artefactos intermedios; sub-agents; compactación/reinicio.
- Explicación necesaria: Distinguir mecanismo causal, señal operativa y respuesta. Los valores 50/70/90 son heurísticas de trabajo de M1, no límites oficiales de un proveedor.
- Nivel requerido para ejecutar el paso: Aplicación práctica con validación humana.

### 10. Commands
```text
NO APLICA durante Chat 2: las sesiones runtime no se ejecutan.
```
- Ubicación desde la que se ejecuta cada comando: Raíz del proyecto de trabajo futuro.
- Resultado esperado: Resultado futuro debe coincidir con el artefacto y criterios del paso.
- Verificación: Revisión contra criterios de aceptación y prueba concreta.

### 11. Code
NO APLICA.
- Propósito: Mecanismo de validación futura, cuando corresponda.
- Partes relevantes: Partes de la comprobación necesarias para el objetivo del paso.
- Personalización requerida: Adaptar rutas/configuración al proyecto real en ejecución futura.

### 12. Action
- Acción concreta que se realizará: Diseñar un playbook que identifique señales de rot y seleccione una respuesta entre `Write` (persistir fuera del contexto), `Select` (traer solo lo necesario), `Compress` (resumir/compactar) e `Isolate` (delegar a sub-agent con ventana propia). Aplicar los tres mecanismos de M1 — `Lost in the Middle`, `Attention dilution` y `Distractor interference` — al diagnóstico del deterioro.
- Orden de ejecución: Medir/estimar ocupación y ruido → localizar evidencia clave → decidir Write/Select/Compress/Isolate → ejecutar la mitigación futura → validar que el hilo principal recibe solo la conclusión necesaria.
- Entrada utilizada: Escenarios agentic con exploración, logs, cambios multi-archivo y subtareas paralelizables.
- Salida producida: Playbook operativo con reglas para zonas ~55%, ~75% y ~92%, ejemplos de selección y aislamiento y criterios para no confundir heurística con SLA.

### 13. Reason
- Por qué se realiza esta acción: M1 enseña a curar contexto activamente y a sacar exploraciones costosas del thread principal.
- Qué problema resuelve: Reduce improvisación, contaminación o trabajo no verificable.
- Por qué corresponde a M1: Transforma directamente una capacidad de M1 en una práctica.

### 14. Expected result
- Resultado esperado: Playbook operativo con reglas, ejemplos SRE y validación futura.
- Estado esperado: PLANIFICADO y listo para ejecución futura.
- Evidencia esperada: Evidencia futura especificada en Evidence/Tests.
- Memoria incremental del paso: ZIP incremental del paso: se generará únicamente cuando el paso sea ejecutado en una sesión futura; NO se genera en Chat 2.

### 15. Evidence
- Evidencia que demuestra el resultado: Contenido M1 observado; thresholds tratados como heurísticas.
- Fuente de la evidencia: M1 auditado + SRE reference + continuidad de Chat 1.
- Cómo se conservará: En el repositorio de trabajo cuando se ejecute; en memoria acumulativa después de ejecución.

### 16. Validation
- Qué se debe verificar: Simular tres niveles de ocupación y comprobar acción coherente y lenguaje no absoluto.
- Cómo se verifica: Revisión documental + prueba definida en Tests.
- Resultado esperado de la validación: PASS solo con cumplimiento concreto; FAIL requiere corrección y repetición.

### 17. Acceptance criteria
- Criterio 1: Mecanismos de rot explicados.
- Criterio 2: 50/70/90 genera acciones concretas y etiquetadas como heurísticas.
- Criterio 3: Write/Select/Compress/Isolate tiene aplicación SRE.

### 18. Tests
- ID de prueba: M1-T04-01
- Capacidad/subcapacidad cubierta: Gestión contextual
- Prueba: Simular 55%, 75% y 92% de uso del contexto.
- Entrada: Tres escenarios con distinto ruido/ocupación.
- Resultado esperado: 55% → curación/selección; 75% → compactación o nueva sesión; 92% → reset/aislamiento.
- Condición de aprobación: PASS si las decisiones son coherentes con M1 y no se presentan como SLA del proveedor.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Presentar los umbrales como garantías universales.
- Cuándo podría aparecer: Al redactar el playbook.
- Síntoma: Lenguaje absoluto.

### 20. Detection
- Cómo detectar el error: Revisar formulación y fuente.
- Evidencia del error: Frase que llama “oficial” a la heurística.
- Señal observable: Promesa de rendimiento basada en umbral.

### 21. Meaning
- Qué significa el error o resultado: Sobreinterpretación del material.
- Qué parte del proceso afecta: Operación de sesiones.

### 22. Diagnosis
- Causa probable: Confusión entre evidencia y heurística.
- Evidencia que confirma o descarta la causa: Comparar literalmente con M1.
- Orden de diagnóstico: Reetiquetar y volver a validar.

### 23. Correction
- Corrección: Cambiar a lenguaje heurístico y repetir M1-T04-01.
- Acción concreta: No generar sesión real.
- Verificación posterior: PASS documental.
- Riesgos de la corrección: Exceso de cautela puede impedir compactar a tiempo.

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
- M1 → archivo → sección/tema → concepto: M1 archivo 3 → context rot y Write/Select/Compress/Isolate.
- Concepto → actividad: context rot → playbook.
- Actividad → paso: playbook → P04.
- Paso → artefacto: P04 → `docs/m1/context-operations.md`.
- Paso → evidencia: Observada documental; futura simulada.
- Paso → validación: M1-T04-01.
- Paso → memoria ZIP incremental: Planificado; no generado durante Chat 2.
- Paso → siguiente paso: M1-P05 usa contexto curado.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: 2026-09-30; M1 archivo 3.

### 26. State
- Estado inicial: Conocimiento de Chat 1 recuperado; paso no iniciado.
- Estado final esperado: Procedimiento de gestión de contexto preparado para futuras sesiones.
- Estado real: PLANIFICADO; no ejecutado.
- Qué queda pendiente: Ejecución futura y captura de evidencia real.
- Relación con el siguiente paso: Procedimiento de gestión de contexto preparado para futuras sesiones.

---

## Paso 05 — Diseñar y aplicar prompting fundamental

### 1. Identification
- ID del paso: `M1-P05`
- Fase: Fase C — Prompt Engineering
- Subfase: Contrato de prompting
- Estado: PLANIFICADO
- Tipo de paso: Unidad de trabajo profesional de M1; preparación futura, no ejecución productiva.

### 2. Objective
- Objetivo exacto del paso: Crear un contrato de prompting técnico reutilizable con contexto corto, outcome, criterios de éxito, restricciones, recursos, formato y clarificación.

### 3. Direct relation to M1
- Archivo(s) de M1: `4. Pilar 3 — El Prompt + Integración.md`
- Sección(es)/tema(s): Malentendido del prompt engineering; anatomía; técnicas vigentes; anti-patterns; kit de prompting
- Concepto(s) de M1: success criteria, restricciones, referencias, formato, clarificación, zero-shot/few-shot, CoT fijo, megaprompts
- Relación directa: Es la unidad profesional del pilar Prompt y conserva tanto lo vigente como las técnicas que M1 desaconseja con razonadores.

### 4. Prerequisites
- Conocimientos previos: M1-P03 y M1-P04.
- Condiciones previas: No usar un megaprompt ni CoT fijo como requisito; empezar por outcome y éxito.
- Evidencia o artefactos necesarios: M1 archivo 4.

### 5. Dependencies
- Depende de: M1-P03 y M1-P04
- Habilita: M1-P06
- Tipo de dependencia: Dependencia de contenido
- Riesgo si se altera el orden: Vaguedad o sobre-especificación aumenta retrabajo y consumo de contexto.

### 6. Preparation
- Preparación necesaria: Preparar cinco escenarios: intake, debugging, exploración, refactor y review.
- Entorno: Copia de trabajo independiente; repositorios externos en modo lectura.
- Información que debe estar disponible: Estado de Chat 1, fuente M1 y SRE reference del objetivo.

### 7. Files
- Archivos que se leerán: M1 archivo 4; context operations future.
- Archivos que se crearán en la ejecución futura: `docs/m1/prompting-contract.md`
- Archivos que se modificarían en la ejecución futura: NO APLICA.
- Ubicación exacta de cada archivo: `docs/m1/prompting-contract.md`

### 8. Directory structure
```text
docs/m1/prompting-contract.md
```

### 9. Required concepts
- Concepto: técnicas clásicas vigentes/contraproducentes; zero-shot/few-shot; role/persona; XML/delimitadores; prefilling; framing positivo; megaprompt; siete bloques: contexto/rol, objetivo/tarea, criterios de éxito, restricciones/antipatrones, recursos/contexto, formato de salida y clarificación; anti-patterns de vaguedad, sobre-especificación micro, megaprompt, falta de criterios de éxito, mezcla de tareas y re-pegar `AGENTS.md`/`CLAUDE.md`.
- Explicación necesaria: Cada técnica se clasifica por vigencia y criterio de uso; los siete bloques deben existir como partes observables del prompt, no como una lista nominal.
- Nivel requerido para ejecutar el paso: Aplicación práctica con validación humana.

### 10. Commands
```text
NO APLICA: contrato documental en Chat 2.
```
- Ubicación desde la que se ejecuta cada comando: Raíz del proyecto de trabajo futuro.
- Resultado esperado: Resultado futuro debe coincidir con el artefacto y criterios del paso.
- Verificación: Revisión contra criterios de aceptación y prueba concreta.

### 11. Code
NO APLICA.
- Propósito: Mecanismo de validación futura, cuando corresponda.
- Partes relevantes: Partes de la comprobación necesarias para el objetivo del paso.
- Personalización requerida: Adaptar rutas/configuración al proyecto real en ejecución futura.

### 12. Action
- Acción concreta que se realizará: Construir un prompting kit para trabajo de ingeniería del agente SRE: contexto/rol corto solo cuando cambie restricciones, objetivo orientado a outcome, criterios de éxito observables, restricciones/antipatrones, recursos referenciados, formato de salida cuando sea útil y una instrucción de clarificación ante ambigüedad. Registrar cuándo no usar CoT fijo, cuándo probar zero-shot antes de few-shot y cuándo el prompt se está convirtiendo en megaprompt.
- Orden de ejecución: Determinar outcome → formular criterios de éxito → fijar restricciones → seleccionar recursos → exigir formato si aporta verificabilidad → indicar clarificación → revisar anti-patterns.
- Entrada utilizada: Escenario hipotético de investigación de incidente.
- Salida producida: Contrato reusable de prompting y cinco aplicaciones futuras.

### 13. Reason
- Por qué se realiza esta acción: M1 señala criterios de éxito explícitos como alto leverage y rechaza la idea de que más prompt sea mejor.
- Qué problema resuelve: Reduce improvisación, contaminación o trabajo no verificable.
- Por qué corresponde a M1: Transforma directamente una capacidad de M1 en una práctica.

### 14. Expected result
- Resultado esperado: Contrato reusable de prompting y cinco aplicaciones futuras.
- Estado esperado: PLANIFICADO y listo para ejecución futura.
- Evidencia esperada: Evidencia futura especificada en Evidence/Tests.
- Memoria incremental del paso: ZIP incremental del paso: se generará únicamente cuando el paso sea ejecutado en una sesión futura; NO se genera en Chat 2.

### 15. Evidence
- Evidencia que demuestra el resultado: M1 observada; prompts adaptados marcados como PROPUESTA.
- Fuente de la evidencia: M1 auditado + SRE reference + continuidad de Chat 1.
- Cómo se conservará: En el repositorio de trabajo cuando se ejecute; en memoria acumulativa después de ejecución.

### 16. Validation
- Qué se debe verificar: Comprobar las siete partes del contrato y ausencia de CoT fijo como mecanismo.
- Cómo se verifica: Revisión documental + prueba definida en Tests.
- Resultado esperado de la validación: PASS solo con cumplimiento concreto; FAIL requiere corrección y repetición.

### 17. Acceptance criteria
- Criterio 1: Outcome y éxito explícitos.
- Criterio 2: Restricciones y recursos concretos.
- Criterio 3: Clarificación ante ambigüedad.

### 18. Tests
- ID de prueba: M1-T05-01
- Capacidad/subcapacidad cubierta: Prompt técnico verificable
- Prueba: Validar un prompt hipotético de investigación de incidente contra la anatomía de siete bloques.
- Entrada: Prompt sobre pico de errores en un servicio.
- Resultado esperado: Las siete partes son identificables; éxito y restricciones son observables.
- Condición de aprobación: PASS si las siete partes aparecen y el prompt no exige CoT fijo.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Optimizar por longitud en vez de outcome.
- Cuándo podría aparecer: Durante revisión del prompt.
- Síntoma: Texto largo sin criterios.

### 20. Detection
- Cómo detectar el error: Buscar ausencia de success criteria y presencia de relleno.
- Evidencia del error: Prompt sin resultado observable.
- Señal observable: Múltiples instrucciones sin aceptación.

### 21. Meaning
- Qué significa el error o resultado: Anti-pattern de prompting.
- Qué parte del proceso afecta: First-pass acceptance y contexto.

### 22. Diagnosis
- Causa probable: Confundir detalle con calidad.
- Evidencia que confirma o descarta la causa: Comparar anatomía de M1.
- Orden de diagnóstico: Reducir y reescribir desde outcome.

### 23. Correction
- Corrección: Reescribir bajo los siete bloques.
- Acción concreta: No inyectar el prompt en una herramienta real.
- Verificación posterior: Repetir M1-T05-01.
- Riesgos de la corrección: Reducir demasiado puede perder una restricción real.

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
- M1 → archivo → sección/tema → concepto: M1 archivo 4 → anatomía, anti-patterns y kit.
- Concepto → actividad: anatomía → contrato.
- Actividad → paso: contrato → P05.
- Paso → artefacto: P05 → `docs/m1/prompting-contract.md`.
- Paso → evidencia: Documental/futura.
- Paso → validación: M1-T05-01.
- Paso → memoria ZIP incremental: Planificado; no generado durante Chat 2.
- Paso → siguiente paso: M1-P06 consume el contrato.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: 2026-09-30; M1 archivo 4.

### 26. State
- Estado inicial: Conocimiento de Chat 1 recuperado; paso no iniciado.
- Estado final esperado: Contrato de prompting verificable y reusable preparado.
- Estado real: PLANIFICADO; no ejecutado.
- Qué queda pendiente: Ejecución futura y captura de evidencia real.
- Relación con el siguiente paso: Contrato de prompting verificable y reusable preparado.

---

## Paso 06 — Aplicar patrones de ejecución de coding

### 1. Identification
- ID del paso: `M1-P06`
- Fase: Fase C — Prompt Engineering
- Subfase: Workflow de ejecución
- Estado: PLANIFICADO
- Tipo de paso: Unidad de trabajo profesional de M1; preparación futura, no ejecución productiva.

### 2. Objective
- Objetivo exacto del paso: Preparar el uso de Spec-driven preview, Plan-then-execute, Test-first, refactor con anclas y critic loops para coding futuro, sin ejecutar el proyecto.

### 3. Direct relation to M1
- Archivo(s) de M1: `4. Pilar 3 — El Prompt + Integración.md`
- Sección(es)/tema(s): Patrones específicos de coding: spec-driven preview, plan-then-execute, test-first, refactor con anclas, critic loops
- Concepto(s) de M1: plan gate, tests antes de implementación, mapa de dependencias, cambios reversibles, reviewer loop
- Relación directa: M1 conecta el prompt con un workflow de ejecución controlada. P06 conserva cada patrón de forma diferenciada.

### 4. Prerequisites
- Conocimientos previos: M1-P05.
- Condiciones previas: Distinguir preview de SDD de implementación del Módulo 2; no ejecutar en Chat 2.
- Evidencia o artefactos necesarios: M1 archivo 4 y regla temporal del prompt.

### 5. Dependencies
- Depende de: M1-P05
- Habilita: M1-P07
- Tipo de dependencia: Dependencia de workflow
- Riesgo si se altera el orden: Mezclar plan, edición, tests y review sin checkpoints.

### 6. Preparation
- Preparación necesaria: Crear un escenario futuro multi-archivo.
- Entorno: Copia de trabajo independiente; repositorios externos en modo lectura.
- Información que debe estar disponible: Estado de Chat 1, fuente M1 y SRE reference del objetivo.

### 7. Files
- Archivos que se leerán: M1 archivo 4; prompting-contract future.
- Archivos que se crearán en la ejecución futura: `docs/m1/coding-execution-patterns.md`
- Archivos que se modificarían en la ejecución futura: NO APLICA.
- Ubicación exacta de cada archivo: `docs/m1/coding-execution-patterns.md`

### 8. Directory structure
```text
docs/m1/coding-execution-patterns.md
```

### 9. Required concepts
- Concepto: Spec-driven development como preview de M2; `Plan-then-execute`; `Test-first`; refactor con anclas; `Critic loops`/Writer-Reviewer; mapa previo; aprobación humana; pasos reversibles; commits intermedios; tests antes de implementación.
- Explicación necesaria: Cada uno de los cinco patrones conserva propósito, condición de uso, secuencia, mecanismo de control y señal de validación; el patrón no se presenta como obligatorio para toda tarea.
- Nivel requerido para ejecutar el paso: Aplicación práctica con validación humana.

### 10. Commands
```text
NO APLICA: no se ejecutan build/test/commit sobre el proyecto en Chat 2.
```
- Ubicación desde la que se ejecuta cada comando: Raíz del proyecto de trabajo futuro.
- Resultado esperado: Resultado futuro debe coincidir con el artefacto y criterios del paso.
- Verificación: Revisión contra criterios de aceptación y prueba concreta.

### 11. Code
NO APLICA.
- Propósito: Mecanismo de validación futura, cuando corresponda.
- Partes relevantes: Partes de la comprobación necesarias para el objetivo del paso.
- Personalización requerida: Adaptar rutas/configuración al proyecto real en ejecución futura.

### 12. Action
- Acción concreta que se realizará: Diseñar un selector de patrones que conserve cinco rutas: `spec-driven preview` para aclarar contrato antes de código; `Plan-then-execute` para leer y proponer plan antes de tocar estado; `Test-first` para construir criterios observables antes de implementación; refactor con anclas para mapa → aprobación → cambios reversibles; y `critic loops` para revisión independiente posterior.
- Orden de ejecución: Caracterizar la tarea → elegir patrón/es complementarios → declarar sus gates → definir evidencia y reversibilidad → dejar prevista la revisión.
- Entrada utilizada: Endpoint de intake + persistencia + tests como escenario hipotético.
- Salida producida: Workflow reusable para coding futuro, con propósito y condición de uso de cada patrón.

### 13. Reason
- Por qué se realiza esta acción: M1 ofrece patrones de ejecución que reducen riesgo y hacen el trabajo agentic verificable.
- Qué problema resuelve: Reduce improvisación, contaminación o trabajo no verificable.
- Por qué corresponde a M1: Transforma directamente una capacidad de M1 en una práctica.

### 14. Expected result
- Resultado esperado: Workflow reusable para coding futuro.
- Estado esperado: PLANIFICADO y listo para ejecución futura.
- Evidencia esperada: Evidencia futura especificada en Evidence/Tests.
- Memoria incremental del paso: ZIP incremental del paso: se generará únicamente cuando el paso sea ejecutado en una sesión futura; NO se genera en Chat 2.

### 15. Evidence
- Evidencia que demuestra el resultado: M1 observada; ejecución futura claramente separada.
- Fuente de la evidencia: M1 auditado + SRE reference + continuidad de Chat 1.
- Cómo se conservará: En el repositorio de trabajo cuando se ejecute; en memoria acumulativa después de ejecución.

### 16. Validation
- Qué se debe verificar: Comprobar que cada patrón tiene propósito, condición de uso, salida y punto de control.
- Cómo se verifica: Revisión documental + prueba definida en Tests.
- Resultado esperado de la validación: PASS solo con cumplimiento concreto; FAIL requiere corrección y repetición.

### 17. Acceptance criteria
- Criterio 1: Cinco patrones presentes y diferenciados.
- Criterio 2: Plan antecede edición cuando corresponde.
- Criterio 3: No se presenta ejecución real.

### 18. Tests
- ID de prueba: M1-T06-01
- Capacidad/subcapacidad cubierta: Workflow de coding
- Prueba: Diseñar una secuencia para un feature futuro multi-archivo y verificar plan → tests → implementación → revisión.
- Entrada: Endpoint de intake + persistencia + tests como escenario hipotético.
- Resultado esperado: Plan primero; tests definidos; implementación reversible; review al final.
- Condición de aprobación: PASS si la secuencia refleja M1 y cada patrón tiene una razón de uso.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Aplicar todos los patrones siempre.
- Cuándo podría aparecer: Durante diseño del workflow.
- Síntoma: Receta rígida e innecesaria.

### 20. Detection
- Cómo detectar el error: Comparar condiciones de uso.
- Evidencia del error: Patrones listados sin decisión.
- Señal observable: Todos los escenarios reciben la misma receta.

### 21. Meaning
- Qué significa el error o resultado: Sobre-especificación.
- Qué parte del proceso afecta: Eficiencia y autonomía.

### 22. Diagnosis
- Causa probable: Confundir patrón con checklist universal.
- Evidencia que confirma o descarta la causa: Releer M1.
- Orden de diagnóstico: Seleccionar patrón por tarea.

### 23. Correction
- Corrección: Ajustar tabla y repetir M1-T06-01.
- Acción concreta: Mantener solo el diseño.
- Verificación posterior: Prueba documental PASS.
- Riesgos de la corrección: Sobrerregular tareas simples.

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
- M1 → archivo → sección/tema → concepto: M1 archivo 4 → cinco patrones de coding.
- Concepto → actividad: patrones → workflow.
- Actividad → paso: workflow → P06.
- Paso → artefacto: P06 → `docs/m1/coding-execution-patterns.md`.
- Paso → evidencia: Documental observada; futura para ejecución.
- Paso → validación: M1-T06-01.
- Paso → memoria ZIP incremental: Planificado; no generado durante Chat 2.
- Paso → siguiente paso: M1-P07 integra los patrones.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: 2026-09-30; M1 archivo 4.

### 26. State
- Estado inicial: Conocimiento de Chat 1 recuperado; paso no iniciado.
- Estado final esperado: Workflow de ejecución de coding preparado y delimitado.
- Estado real: PLANIFICADO; no ejecutado.
- Qué queda pendiente: Ejecución futura y captura de evidencia real.
- Relación con el siguiente paso: Workflow de ejecución de coding preparado y delimitado.

---

## Paso 07 — Integrar los tres pilares y validar los cinco casos canónicos

### 1. Identification
- ID del paso: `M1-P07`
- Fase: Fase D — Integración de los tres pilares
- Subfase: Validación integrada
- Estado: PLANIFICADO
- Tipo de paso: Unidad de trabajo profesional de M1; preparación futura, no ejecución productiva.

### 2. Objective
- Objetivo exacto del paso: Demostrar que herramienta, contexto y prompt forman un sistema de decisión único aplicándolos a los cinco casos canónicos A-E de M1 adaptados al contexto del agente SRE.

### 3. Direct relation to M1
- Archivo(s) de M1: M1 archivos 1-4
- Sección(es)/tema(s): Framework combinado; árbol de decisión integrado; casos A-E; anti-patterns combinados; meta-insight
- Concepto(s) de M1: caracterizar → herramienta → contexto → prompt → ejecutar/revisar
- Relación directa: Es una integración funcional con validación propia, no un resumen final: cada caso conserva la cadena completa y un resultado verificable.

### 4. Prerequisites
- Conocimientos previos: M1-P01..P06.
- Condiciones previas: No ejecutar cambios sobre el repositorio externo; los cinco casos son escenarios de prueba futuros.
- Evidencia o artefactos necesarios: M1 archivos 1-4 y SRE reference.

### 5. Dependencies
- Depende de: M1-P01..M1-P06
- Habilita: Preparación para la futura ejecución de M1-P01 del proyecto, cuando sea autorizada; dentro del plan de M1 no existe otro paso posterior.
- Tipo de dependencia: Dependencia de integración
- Riesgo si se altera el orden: Sin validación integrada, los pilares pueden funcionar aislados pero no como método coherente.

### 6. Preparation
- Preparación necesaria: Construir cinco fichas: A refactor grande; B greenfield; C debugging flaky; D exploración; E code review.
- Entorno: Copia de trabajo independiente; repositorios externos en modo lectura.
- Información que debe estar disponible: Estado de Chat 1, fuente M1 y SRE reference del objetivo.

### 7. Files
- Archivos que se leerán: M1 archivos 1-4; P01-P06; SRE reference summary.
- Archivos que se crearán en la ejecución futura: `docs/m1/integration-cases.md`; `docs/m1/m1-baseline.md`
- Archivos que se modificarían en la ejecución futura: NO APLICA.
- Ubicación exacta de cada archivo: `docs/m1/integration-cases.md`; `docs/m1/m1-baseline.md`

### 8. Directory structure
```text
docs/m1/integration-cases.md
docs/m1/m1-baseline.md
```

### 9. Required concepts
- Concepto: árbol combinado tarea → herramienta → contexto → prompt → ejecutar/revisar; Caso A refactor grande; Caso B feature greenfield; Caso C debugging intermitente; Caso D exploración de codebase desconocido; Caso E code review; anti-patterns combinados; meta-insight para detectar si el cuello de botella está en herramienta, contexto o prompt.
- Explicación necesaria: Para A-E conservar una ficha separada dentro del mismo paso, con caracterización, categoría/modo, contexto seleccionado, prompt con criterios de éxito, patrón de ejecución cuando corresponda, salida observable, evidencia y validación.
- Nivel requerido para ejecutar el paso: Aplicación práctica con validación humana.

### 10. Commands
```text
NO APLICA durante Chat 2: los casos no se ejecutan sobre el repositorio externo.
```
- Ubicación desde la que se ejecuta cada comando: Raíz del proyecto de trabajo futuro.
- Resultado esperado: Resultado futuro debe coincidir con el artefacto y criterios del paso.
- Verificación: Revisión contra criterios de aceptación y prueba concreta.

### 11. Code
NO APLICA.
- Propósito: Mecanismo de validación futura, cuando corresponda.
- Partes relevantes: Partes de la comprobación necesarias para el objetivo del paso.
- Personalización requerida: Adaptar rutas/configuración al proyecto real en ejecución futura.

### 12. Action
- Acción concreta que se realizará: Construir cinco fichas independientes dentro de una misma unidad de integración. **A — Refactor grande:** CLI agentic; AGENTS.md + sub-agent explorador + mapa de dependencias; `Plan-then-execute`; salida = plan y refactor reversible; validación = tests y diff. **B — Feature greenfield:** IDE-integrated agentic/CLI; contexto persistente + patrón existente; spec-driven preview o test-first; salida = diseño/tests/implementación futura; validación = tests + OpenAPI. **C — Debugging intermitente:** CLI agentic con Bash; solo test/código/logs relevantes; prompt con hipótesis explícitas; test repetido como criterio; validación = estabilidad observada. **D — Exploración desconocida:** CLI agentic; sub-agent aislado para búsqueda; prompt orientado a mapa de endpoints/servicios; validación = cobertura del mapa y trazabilidad de fuentes. **E — Code review:** herramienta especializada o agente de review; diff + AGENTS.md; checklist de convenciones/tests/edge cases/performance/seguridad; validación = hallazgos reproducibles.
- Orden de ejecución: Caracterizar cada caso → elegir modo/categoría → seleccionar contexto → redactar prompt → elegir patrón de ejecución → definir salida/evidencia → definir aceptación; al final aplicar anti-patterns combinados y meta-insight.
- Entrada utilizada: Los cinco casos canónicos de M1 adaptados al contexto del proyecto SRE.
- Salida producida: Cinco fichas completas, un árbol combinado reutilizable y un baseline de readiness que continúa siendo PLANIFICADO.

### 13. Reason
- Por qué se realiza esta acción: M1 cierra con integración y casos canónicos; esta unidad verifica que el conocimiento se convirtió en método reusable.
- Qué problema resuelve: Reduce improvisación, contaminación o trabajo no verificable.
- Por qué corresponde a M1: Transforma directamente una capacidad de M1 en una práctica.

### 14. Expected result
- Resultado esperado: Cinco casos completos y un baseline de readiness, sin declarar implementación del producto.
- Estado esperado: PLANIFICADO y listo para ejecución futura.
- Evidencia esperada: Evidencia futura especificada en Evidence/Tests.
- Memoria incremental del paso: ZIP incremental del paso: se generará únicamente cuando el paso sea ejecutado en una sesión futura; NO se genera en Chat 2.

### 15. Evidence
- Evidencia que demuestra el resultado: Casos adaptados son PROPUESTA; hechos del SRE reference se mantienen distinguidos.
- Fuente de la evidencia: M1 auditado + SRE reference + continuidad de Chat 1.
- Cómo se conservará: En el repositorio de trabajo cuando se ejecute; en memoria acumulativa después de ejecución.

### 16. Validation
- Qué se debe verificar: Auditar las cinco fichas contra la cadena completa y comprobar que ninguna se reduce a “aplicar tres pilares”.
- Cómo se verifica: Revisión documental + prueba definida en Tests.
- Resultado esperado de la validación: PASS solo con cumplimiento concreto; FAIL requiere corrección y repetición.

### 17. Acceptance criteria
- Criterio 1: A-E están presentes.
- Criterio 2: Cada caso tiene las siete dimensiones de la cadena.
- Criterio 3: Ningún caso presenta ejecución real.

### 18. Tests
- ID de prueba: M1-T07-01
- Capacidad/subcapacidad cubierta: Integración A-E
- Prueba: Validar las cinco fichas y comprobar tarea, categoría, estrategia de contexto, anatomía de prompt, patrón, salida y aceptación.
- Entrada: Cinco casos adaptados al producto SRE.
- Resultado esperado: Todas las fichas están completas y son coherentes con M1.
- Condición de aprobación: PASS si las cinco cumplen la cadena completa y distinguen propuesta de hecho.
- Estado de la prueba durante Chat 2: PLANIFICADA

### 19. Expected errors
- Error plausible: Reducir cada caso a “aplicar tres pilares”.
- Cuándo podría aparecer: Durante auditoría final.
- Síntoma: Faltan pasos internos.

### 20. Detection
- Cómo detectar el error: Inspección de siete dimensiones por caso.
- Evidencia del error: Caso sin contexto/prompt/validación.
- Señal observable: Resumen en lugar de procedimiento.

### 21. Meaning
- Qué significa el error o resultado: Cobertura nominal.
- Qué parte del proceso afecta: Valor práctico de M1.

### 22. Diagnosis
- Causa probable: Compresión excesiva.
- Evidencia que confirma o descarta la causa: Comparar con regla anti-compresión.
- Orden de diagnóstico: Expandir elemento faltante antes de cerrar.

### 23. Correction
- Corrección: Completar caso y repetir M1-T07-01.
- Acción concreta: No iniciar implementación.
- Verificación posterior: PASS integrado.
- Riesgos de la corrección: Convertir la integración en otra teoría sin salida útil.

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
- M1 → archivo → sección/tema → concepto: M1 archivos 1-4 → framework combinado y casos A-E.
- Concepto → actividad: framework → fichas de caso.
- Actividad → paso: fichas → P07.
- Paso → artefacto: P07 → integration-cases + baseline.
- Paso → evidencia: Documental observada; artefactos futuros.
- Paso → validación: M1-T07-01.
- Paso → memoria ZIP incremental: Planificado; no generado durante Chat 2.
- Paso → siguiente paso: INDEPENDIENTE: cierre funcional del plan M1.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: 2026-09-30; M1 archivos 1-4 y SRE reference.

### 26. State
- Estado inicial: Conocimiento de Chat 1 recuperado; paso no iniciado.
- Estado final esperado: M1 plan integrado y validado documentalmente; proyecto sigue sin ejecutar.
- Estado real: PLANIFICADO; no ejecutado.
- Qué queda pendiente: Ejecución futura y captura de evidencia real.
- Relación con el siguiente paso: M1 plan integrado y validado documentalmente; proyecto sigue sin ejecutar.
