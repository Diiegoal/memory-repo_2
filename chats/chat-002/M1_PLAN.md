# M1_PLAN — Chat 2

**Estado global:** `NO CERRADO — BLOCKED / NO DEMOSTRADO` porque la identidad byte-a-byte del RAW de Chat 1 no pudo demostrarse contra el Blob SHA remoto; el plan sí fue producido, auditado estructuralmente y queda en estado PLANIFICADO.
**Regla temporal:** no se ejecuta el Paso 1 del proyecto y ningún repositorio externo es modificado.

## Determinación dinámica
Lectura completa de los cinco Markdown reales de M1 → inventario de capacidades/subcapacidades → resultados/evidencias → dependencias → agrupación funcional → pruebas de profundidad/independencia/integración/anti-compresión/anti-fragmentación → control de regresión. El conjunto estable es de siete unidades funcionales P01–P07; la evidencia actual no justifica cambiar las fronteras validadas en Chat 1.

## Secuencia final
1. M1-P01 — Caracterizar la tarea y determinar el modo de trabajo.
2. M1-P02 — Seleccionar y evaluar la herramienta mediante criterios verificables.
3. M1-P03 — Diseñar la arquitectura de contexto persistente del proyecto.
4. M1-P04 — Gestionar la ventana de contexto y prevenir context rot.
5. M1-P05 — Diseñar prompting técnico orientado a outcome.
6. M1-P06 — Aplicar los cinco patrones de ejecución de coding.
7. M1-P07 — Integrar los tres pilares y validar los cinco casos canónicos.

## Registro atómico de cobertura

Cada registro tiene un único propietario principal. El registro se utiliza para alimentar field 18 y no crea pasos adicionales.

### M1-P01
- SUBCAP_ID: `P01-S01`
- nombre de la subcapacidad: Caracterizar la tarea antes de decidir la herramienta, contexto o prompt.
- fuente M1 exacta: 1. El modelo mental de los 3 pilares.md — secciones «Los 3 pilares: el framework de este máster» y «El meta-mensaje de esta sesión»
- definición operativa: Caracterizar la tarea antes de decidir la herramienta, contexto o prompt.
- escenario/proyecto al que aplica: Escenario SRE futuro: incidente, refactor, feature, debugging, exploración y review.
- entrada: Ficha con seis escenarios.
- acción: Registrar tipo de tarea, superficie, necesidad de comandos y control humano.
- salida: Ficha de tarea
- criterio de éxito: Criterio: todos los atributos observables quedan registrados antes de seleccionar herramienta.
- evidencia: Ficha de caracterización.
- validación: PASS si no hay escenario sin alcance explícito; FAIL si el modo se decide sin esos atributos.
- TEST_ID: `P01-T01`
- ASSERTION_ID: `P01-A01`
- observación verificable: Se observa que la ficha identifica objetivo, superficie y necesidad de comandos.
- criterio PASS: PASS si no hay escenario sin alcance explícito; FAIL si el modo se decide sin esos atributos.
- criterio FAIL: algún atributo necesario de la tarea queda ausente o se elige modo antes de completar la ficha.

- SUBCAP_ID: `P01-S02`
- nombre de la subcapacidad: Elegir completion o agentic según tamaño, capas, comandos y control requerido.
- fuente M1 exacta: 2. Pilar 1 — La Herramienta.md — «Diferencia que NO es de categoría: completion vs agentic»
- definición operativa: Elegir completion o agentic según tamaño, capas, comandos y control requerido.
- escenario/proyecto al que aplica: Seis escenarios de trabajo del proyecto SRE.
- entrada: Seis escenarios.
- acción: Clasificar cada escenario y justificar la elección.
- salida: Matriz de modo de trabajo
- criterio de éxito: Criterio: multi-capa/comandos → agentic; tarea contenida → completion salvo excepción justificada.
- evidencia: Matriz de escenarios.
- validación: PASS si multi-capa/comandos → agentic y tarea contenida → completion salvo excepción justificada.
- TEST_ID: `P01-T01`
- ASSERTION_ID: `P01-A02`
- observación verificable: Se observa una clasificación completion/agentic coherente con la complejidad.
- criterio PASS: PASS si multi-capa/comandos → agentic y tarea contenida → completion salvo excepción justificada.
- criterio FAIL: la clasificación contradice la complejidad/comandos del escenario o carece de justificación.

- SUBCAP_ID: `P01-S03`
- nombre de la subcapacidad: Aplicar la secuencia caracterización → herramienta → contexto → prompt → ejecución/revisión.
- fuente M1 exacta: 1. El modelo mental de los 3 pilares.md — «El framework de este máster»; 4. Pilar 3 — El Prompt + Integración.md — «El framework de decisión combinado»
- definición operativa: Aplicar la secuencia caracterización → herramienta → contexto → prompt → ejecución/revisión.
- escenario/proyecto al que aplica: Tres tareas representativas del proyecto.
- entrada: Tres tareas.
- acción: Comparar la secuencia aplicada y detectar inversiones prematuras.
- salida: Registro de decisión
- criterio de éxito: Criterio: ninguna herramienta aparece como decisión primaria antes de caracterizar la tarea.
- evidencia: Registro de decisión.
- validación: PASS si ninguna herramienta se elige antes de caracterizar; FAIL si se invierte el orden.
- TEST_ID: `P01-T02`
- ASSERTION_ID: `P01-A03`
- observación verificable: Se observa la secuencia caracterización→herramienta→contexto→prompt.
- criterio PASS: PASS si ninguna herramienta se elige antes de caracterizar; FAIL si se invierte el orden.
- criterio FAIL: la herramienta se elige antes de caracterizar la tarea o se omite uno de los pilares.

- SUBCAP_ID: `P01-S04`
- nombre de la subcapacidad: Convertir el outcome y los criterios de éxito en condiciones observables.
- fuente M1 exacta: 4. Pilar 3 — El Prompt + Integración.md — «La anatomía de un prompt técnico 2026»
- definición operativa: Convertir el outcome y los criterios de éxito en condiciones observables.
- escenario/proyecto al que aplica: Ficha de una capacidad SRE aún no implementada.
- entrada: Ficha SRE.
- acción: Derivar criterios que puedan convertirse en PASS/FAIL futuro.
- salida: Especificación de éxito
- criterio de éxito: Criterio: cada criterio puede comprobarse sin depender de «funciona bien».
- evidencia: Criterios de éxito.
- validación: PASS si cada criterio puede verificarse; FAIL si solo dice 'funciona bien'.
- TEST_ID: `P01-T03`
- ASSERTION_ID: `P01-A04`
- observación verificable: Se observa outcome y criterios de éxito observables.
- criterio PASS: PASS si cada criterio puede verificarse; FAIL si solo dice 'funciona bien'.
- criterio FAIL: algún criterio no puede transformarse en una comprobación observable PASS/FAIL.

### M1-P02
- SUBCAP_ID: `P02-S01`
- nombre de la subcapacidad: Seleccionar la categoría IDE-integrated cuando el trabajo sea visual, inline o contenido.
- fuente M1 exacta: 2. Pilar 1 — La Herramienta.md — «Categoría A — IDE-integrated»
- definición operativa: Seleccionar la categoría IDE-integrated cuando el trabajo sea visual, inline o contenido.
- escenario/proyecto al que aplica: Feature pequeña o edición localizada.
- entrada: Candidato A.
- acción: Evaluar categoría A frente al escenario.
- salida: Matriz de selección
- criterio de éxito: Criterio: el flujo inline/diff justifica la categoría, no el nombre comercial.
- evidencia: Matriz.
- validación: PASS si la categoría se justifica por flujo; FAIL si solo se usa el nombre del producto.
- TEST_ID: `P02-T01`
- ASSERTION_ID: `P02-A01`
- observación verificable: La candidatura se clasifica como IDE-integrated con evidencia del modo inline.
- criterio PASS: PASS si la categoría se justifica por flujo; FAIL si solo se usa el nombre del producto.
- criterio FAIL: la categoría A se asigna solo por marca sin relacionarla con flujo inline/diff.

- SUBCAP_ID: `P02-S02`
- nombre de la subcapacidad: Seleccionar CLI agentic para tareas multiarchivo, ejecución de comandos o trabajo plan-driven.
- fuente M1 exacta: 2. Pilar 1 — La Herramienta.md — «Categoría B — Terminal/CLI agentic»
- definición operativa: Seleccionar CLI agentic para tareas multiarchivo, ejecución de comandos o trabajo plan-driven.
- escenario/proyecto al que aplica: Refactor, migración, exploración o pruebas que requieran terminal.
- entrada: Candidato B.
- acción: Evaluar categoría B frente al escenario.
- salida: Matriz de selección
- criterio de éxito: Criterio: necesidad de plan/comandos o tarea larga queda explícita.
- evidencia: Matriz.
- validación: PASS si requiere plan/comandos; FAIL si se clasifica sin ese rasgo.
- TEST_ID: `P02-T01`
- ASSERTION_ID: `P02-A02`
- observación verificable: La candidatura se clasifica como Terminal/CLI agentic.
- criterio PASS: PASS si requiere plan/comandos; FAIL si se clasifica sin ese rasgo.
- criterio FAIL: la categoría B no queda asociada a trabajo multiarchivo, plan-driven o comandos.

- SUBCAP_ID: `P02-S03`
- nombre de la subcapacidad: Seleccionar autonomía cloud solo cuando el trabajo sea ticketizado, asíncrono y supervisable.
- fuente M1 exacta: 2. Pilar 1 — La Herramienta.md — «Categoría C — Standalone autonomous agents (cloud)»
- definición operativa: Seleccionar autonomía cloud solo cuando el trabajo sea ticketizado, asíncrono y supervisable.
- escenario/proyecto al que aplica: Trabajo paralelizable fuera del horario interactivo.
- entrada: Candidato C.
- acción: Evaluar categoría C y justificar su necesidad real.
- salida: Matriz de selección
- criterio de éxito: Criterio: existe necesidad de autonomía/latencia de horas; si no, se descarta.
- evidencia: Matriz.
- validación: PASS si la unidad es ticket/async; FAIL si no existe necesidad de autonomía.
- TEST_ID: `P02-T01`
- ASSERTION_ID: `P02-A03`
- observación verificable: La candidatura se clasifica como cloud/autonomous.
- criterio PASS: PASS si la unidad es ticket/async; FAIL si no existe necesidad de autonomía.
- criterio FAIL: se añade autonomía cloud sin necesidad de async/ticket/paralelización.

- SUBCAP_ID: `P02-S04`
- nombre de la subcapacidad: Usar herramientas especializadas cuando review, search o security sea el subproblema dominante.
- fuente M1 exacta: 2. Pilar 1 — La Herramienta.md — «Categoría D — Especializados»
- definición operativa: Usar herramientas especializadas cuando review, search o security sea el subproblema dominante.
- escenario/proyecto al que aplica: Code review o análisis específico del proyecto.
- entrada: Candidato D.
- acción: Evaluar categoría D por especialización.
- salida: Matriz de selección
- criterio de éxito: Criterio: la especialización es la razón dominante del uso.
- evidencia: Matriz.
- validación: PASS si la especialización es la razón dominante.
- TEST_ID: `P02-T01`
- ASSERTION_ID: `P02-A04`
- observación verificable: La candidatura se clasifica como specialized.
- criterio PASS: PASS si la especialización es la razón dominante.
- criterio FAIL: la especialización no es el motivo dominante del uso.

- SUBCAP_ID: `P02-S06`
- nombre de la subcapacidad: Aplicar tamaño/forma del codebase, lenguaje, privacidad/compliance, presupuesto y estilo del developer.
- fuente M1 exacta: 2. Pilar 1 — La Herramienta.md — «Matriz de decisión: cinco criterios prácticos»
- definición operativa: Aplicar tamaño/forma del codebase, lenguaje, privacidad/compliance, presupuesto y estilo del developer.
- escenario/proyecto al que aplica: Dos candidaturas y atributos del proyecto.
- entrada: Dos candidatos + atributos.
- acción: Rellenar los cinco criterios y detectar candidatos incompatibles.
- salida: Decision matrix
- criterio de éxito: Criterio: los cinco criterios afectan la decisión; cualquiera puede descartar una candidatura.
- evidencia: Decision matrix.
- validación: PASS si los cinco están tratados y uno puede descartar un candidato; FAIL si alguno falta.
- TEST_ID: `P02-T02`
- ASSERTION_ID: `P02-A06`
- observación verificable: Los cinco criterios aparecen rellenos y afectan la decisión.
- criterio PASS: PASS si los cinco están tratados y uno puede descartar un candidato; FAIL si alguno falta.
- criterio FAIL: falta uno de los cinco criterios o ninguno puede cambiar la decisión.

- SUBCAP_ID: `P02-S07`
- nombre de la subcapacidad: Interpretar benchmarks junto con harness/scaffolding y evitar sesgos de vendor/score.
- fuente M1 exacta: 2. Pilar 1 — La Herramienta.md — «Benchmarks: cómo leerlos sin engañarte» y «Anti-patrones documentados en selección de herramienta»
- definición operativa: Interpretar benchmarks junto con harness/scaffolding y evitar sesgos de vendor/score.
- escenario/proyecto al que aplica: Dos resultados de benchmark y dos decisiones de herramienta.
- entrada: Dos decisiones comparadas.
- acción: Anotar contexto del benchmark y un anti-patrón con su prevención.
- salida: Benchmark note
- criterio de éxito: Criterio: el score no es la única evidencia y queda registrado el caveat.
- evidencia: Decision note.
- validación: PASS si la regla de prevención queda explícita.
- TEST_ID: `P02-T03`
- ASSERTION_ID: `P02-A11`
- observación verificable: Se identifica al menos un anti-patrón de selección y su prevención.
- criterio PASS: PASS si la regla de prevención queda explícita.
- criterio FAIL: el score se interpreta sin condiciones de benchmark/harness o el anti-patrón no tiene prevención.

### M1-P03
- SUBCAP_ID: `P03-S01`
- nombre de la subcapacidad: Clasificar contexto y decidir qué persiste, qué se selecciona y qué se deja fuera.
- fuente M1 exacta: 3. Pilar 2 — El Contexto.md — «Tipos de contexto: qué meter, qué dejar fuera»
- definición operativa: Clasificar contexto y decidir qué persiste, qué se selecciona y qué se deja fuera.
- escenario/proyecto al que aplica: Ocho tipos de contexto descritos en M1.
- entrada: Ejemplos efímeros.
- acción: Asignar política de persistencia/exclusión a cada tipo.
- salida: Context map
- criterio de éxito: Criterio: cada tipo tiene una razón explícita; no se añade contenido «por si acaso».
- evidencia: Policy.
- validación: PASS si la política distingue durable vs efímero.
- TEST_ID: `P03-T01`
- ASSERTION_ID: `P03-A02`
- observación verificable: El contexto de sesión efímero no se eleva a regla persistente sin justificación.
- criterio PASS: PASS si la política distingue durable vs efímero.
- criterio FAIL: algún tipo de contexto no tiene política de persistencia/exclusión o se incluye por si acaso.

- SUBCAP_ID: `P03-S02`
- nombre de la subcapacidad: Diseñar AGENTS.md como mapa corto de alta señal hacia documentación más profunda.
- fuente M1 exacta: 3. Pilar 2 — El Contexto.md — «El estándar de facto: AGENTS.md»
- definición operativa: Diseñar AGENTS.md como mapa corto de alta señal hacia documentación más profunda.
- escenario/proyecto al que aplica: Borrador de contexto persistente del proyecto.
- entrada: Borrador AGENTS.md.
- acción: Definir secciones, enlaces/paths y reglas de alta señal.
- salida: AGENTS.md draft
- criterio de éxito: Criterio: el archivo guía y no duplica la documentación extensa.
- evidencia: AGENTS.md draft.
- validación: PASS si no contiene la enciclopedia del proyecto.
- TEST_ID: `P03-T02`
- ASSERTION_ID: `P03-A04`
- observación verificable: AGENTS.md funciona como índice corto de alta señal.
- criterio PASS: PASS si no contiene la enciclopedia del proyecto.
- criterio FAIL: AGENTS.md contiene detalle profundo que debería vivir fuera o no ofrece rutas útiles.

- SUBCAP_ID: `P03-S03`
- nombre de la subcapacidad: Evitar duplicación de reglas y establecer una fuente de verdad compartida.
- fuente M1 exacta: 3. Pilar 2 — El Contexto.md — «Comparativa de mecanismos» y «Buenas prácticas en el contenido del archivo»
- definición operativa: Evitar duplicación de reglas y establecer una fuente de verdad compartida.
- escenario/proyecto al que aplica: AGENTS.md y políticas auxiliares.
- entrada: AGENTS.md + policy.
- acción: Asignar propietario de cada regla compartida.
- salida: Cross-reference
- criterio de éxito: Criterio: una regla no tiene dos versiones contradictorias.
- evidencia: Cross-reference.
- validación: PASS si una regla tiene un propietario; FAIL si hay versiones divergentes.
- TEST_ID: `P03-T02`
- ASSERTION_ID: `P03-A05`
- observación verificable: Existe una única fuente de verdad para reglas compartidas.
- criterio PASS: PASS si una regla tiene un propietario; FAIL si hay versiones divergentes.
- criterio FAIL: una regla compartida tiene más de un propietario o versiones contradictorias.

- SUBCAP_ID: `P03-S04`
- nombre de la subcapacidad: Mantener freshness y ownership de las reglas de contexto.
- fuente M1 exacta: 3. Pilar 2 — El Contexto.md — «Buenas prácticas en el contenido del archivo»
- definición operativa: Mantener freshness y ownership de las reglas de contexto.
- escenario/proyecto al que aplica: Listado de reglas del futuro repositorio.
- entrada: Listado de reglas.
- acción: Registrar propietario y evento que obliga a actualizar cada regla.
- salida: Policy audit
- criterio de éxito: Criterio: ninguna regla técnica queda huérfana de ownership/freshness.
- evidencia: Policy audit.
- validación: PASS si no hay regla huérfana.
- TEST_ID: `P03-T03`
- ASSERTION_ID: `P03-A07`
- observación verificable: Cada regla técnica tiene freshness/ownership.
- criterio PASS: PASS si no hay regla huérfana.
- criterio FAIL: queda una regla técnica sin propietario, freshness o evento de actualización.

### M1-P04
- SUBCAP_ID: `P04-S01`
- nombre de la subcapacidad: Sacar del hilo principal el detalle que no se necesita inmediatamente y conservar una referencia recuperable.
- fuente M1 exacta: 3. Pilar 2 — El Contexto.md — «1. Write — persistir fuera del contexto»
- definición operativa: Sacar del hilo principal el detalle que no se necesita inmediatamente y conservar una referencia recuperable.
- escenario/proyecto al que aplica: Informe intermedio de investigación futura.
- entrada: Informe intermedio.
- acción: Persistir el detalle y registrar su path/resumen.
- salida: Write record
- criterio de éxito: Criterio: el detalle puede recuperarse sin reinyectarlo completo en el hilo.
- evidencia: Write record.
- validación: PASS si se conserva la capacidad de recuperar el detalle sin copiarlo.
- TEST_ID: `P04-T01`
- ASSERTION_ID: `P04-A01`
- observación verificable: Write mueve detalle fuera del contexto y deja referencia recuperable.
- criterio PASS: PASS si se conserva la capacidad de recuperar el detalle sin copiarlo.
- criterio FAIL: el detalle no puede recuperarse mediante una referencia estable o permanece copiado innecesariamente.

- SUBCAP_ID: `P04-S02`
- nombre de la subcapacidad: Traer solo los elementos relacionados con la tarea y dejar el resto descubrible.
- fuente M1 exacta: 3. Pilar 2 — El Contexto.md — «2. Select — elegir qué traer al contexto»
- definición operativa: Traer solo los elementos relacionados con la tarea y dejar el resto descubrible.
- escenario/proyecto al que aplica: Repositorio documental amplio.
- entrada: Repo documental amplio.
- acción: Seleccionar el conjunto mínimo y justificar cada inclusión.
- salida: Selection log
- criterio de éxito: Criterio: ninguna inclusión se justifica solo por «por si acaso».
- evidencia: Selection log.
- validación: PASS si cada selección se justifica por la tarea; FAIL si es 'por si acaso'.
- TEST_ID: `P04-T02`
- ASSERTION_ID: `P04-A02`
- observación verificable: Select trae solo elementos relacionados con la pregunta.
- criterio PASS: PASS si cada selección se justifica por la tarea; FAIL si es 'por si acaso'.
- criterio FAIL: la selección incorpora elementos sin relación justificable con la tarea.

- SUBCAP_ID: `P04-S03`
- nombre de la subcapacidad: Reducir volumen conservando decisiones, estado y próximos pasos necesarios.
- fuente M1 exacta: 3. Pilar 2 — El Contexto.md — «3. Compress — resumir antes de continuar»
- definición operativa: Reducir volumen conservando decisiones, estado y próximos pasos necesarios.
- escenario/proyecto al que aplica: Historial de sesión prolongado.
- entrada: Historial largo.
- acción: Generar resumen compacto y contrastarlo con el estado requerido.
- salida: Compressed state
- criterio de éxito: Criterio: no se pierde ninguna decisión/estado requerido.
- evidencia: Compressed state.
- validación: PASS si no se pierde una decisión/estado requerido.
- TEST_ID: `P04-T03`
- ASSERTION_ID: `P04-A03`
- observación verificable: Compress conserva decisiones y estado al reducir volumen.
- criterio PASS: PASS si no se pierde una decisión/estado requerido.
- criterio FAIL: el resumen pierde una decisión, estado o siguiente acción requerida.

- SUBCAP_ID: `P04-S04`
- nombre de la subcapacidad: Aislar exploraciones costosas y devolver solo hallazgos accionables.
- fuente M1 exacta: 3. Pilar 2 — El Contexto.md — «4. Isolate — aislar contexto por subagente»
- definición operativa: Aislar exploraciones costosas y devolver solo hallazgos accionables.
- escenario/proyecto al que aplica: Subtarea de exploración del proyecto SRE.
- entrada: Subtarea costosa.
- acción: Ejecutar la exploración futura en un subagente y devolver findings compactos.
- salida: Isolated findings
- criterio de éxito: Criterio: el hilo principal no recibe transcript verboso innecesario.
- evidencia: Isolated findings.
- validación: PASS si el hilo principal recibe solo hallazgos accionables.
- TEST_ID: `P04-T03`
- ASSERTION_ID: `P04-A04`
- observación verificable: Isolate devuelve findings y no transcript verboso.
- criterio PASS: PASS si el hilo principal recibe solo hallazgos accionables.
- criterio FAIL: el subagente devuelve transcript verboso/no accionable en vez de findings.

### M1-P05
- SUBCAP_ID: `P05-S01`
- nombre de la subcapacidad: Escribir prompts orientados a outcome con contexto solo cuando aporte señal.
- fuente M1 exacta: 4. Pilar 3 — El Prompt + Integración.md — «La anatomía de un prompt técnico 2026»
- definición operativa: Escribir prompts orientados a outcome con contexto solo cuando aporte señal.
- escenario/proyecto al que aplica: Prompt futuro para una tarea del proyecto.
- entrada: Prompt feature.
- acción: Redactar objetivo y contexto mínimo suficiente.
- salida: Prompt versionado
- criterio de éxito: Criterio: un lector puede identificar inequívocamente el resultado perseguido.
- evidencia: Prompt file.
- validación: PASS si el objetivo es inequívoco.
- TEST_ID: `P05-T01`
- ASSERTION_ID: `P05-A01`
- observación verificable: El prompt contiene objetivo/outcome y contexto solo cuando aporta señal.
- criterio PASS: PASS si el objetivo es inequívoco.
- criterio FAIL: el prompt no permite identificar inequívocamente el outcome.

- SUBCAP_ID: `P05-S02`
- nombre de la subcapacidad: Expresar criterios de éxito observables para cerrar el trabajo.
- fuente M1 exacta: 4. Pilar 3 — El Prompt + Integración.md — «La anatomía de un prompt técnico 2026»
- definición operativa: Expresar criterios de éxito observables para cerrar el trabajo.
- escenario/proyecto al que aplica: Tarea de debugging o feature.
- entrada: Prompt debugging.
- acción: Convertir expectativas en comprobaciones observables.
- salida: Prompt review
- criterio de éxito: Criterio: un tercero podría decidir PASS/FAIL.
- evidencia: Prompt review.
- validación: PASS si otro lector puede validar el resultado.
- TEST_ID: `P05-T01`
- ASSERTION_ID: `P05-A02`
- observación verificable: Los criterios de éxito son observables.
- criterio PASS: PASS si otro lector puede validar el resultado.
- criterio FAIL: un tercero no puede decidir PASS/FAIL con el criterio escrito.

- SUBCAP_ID: `P05-S03`
- nombre de la subcapacidad: Usar restricciones concretas sin micro-especificar la solución.
- fuente M1 exacta: 4. Pilar 3 — El Prompt + Integración.md — «Qué del prompt engineering clásico sigue vigente» y «Anti-patterns documentados»
- definición operativa: Usar restricciones concretas sin micro-especificar la solución.
- escenario/proyecto al que aplica: Prompt con restricciones de seguridad/arquitectura.
- entrada: Prompt con dos restricciones.
- acción: Evaluar que cada restricción reduzca el espacio de soluciones incorrectas.
- salida: Constraint review
- criterio de éxito: Criterio: la restricción es concreta y no duplica política persistente.
- evidencia: Prompt review.
- validación: PASS si la restricción es concreta y no repite policy persistente.
- TEST_ID: `P05-T02`
- ASSERTION_ID: `P05-A03`
- observación verificable: Las restricciones limitan soluciones incorrectas sin micro-especificar.
- criterio PASS: PASS si la restricción es concreta y no repite policy persistente.
- criterio FAIL: la restricción es vaga, contradictoria o micro-especifica una solución.

- SUBCAP_ID: `P05-S04`
- nombre de la subcapacidad: Apuntar a recursos concretos y activar clarificación cuando falte información.
- fuente M1 exacta: 4. Pilar 3 — El Prompt + Integración.md — «La anatomía de un prompt técnico 2026»
- definición operativa: Apuntar a recursos concretos y activar clarificación cuando falte información.
- escenario/proyecto al que aplica: Prompt ambiguo con referencias al repositorio.
- entrada: Prompt ambiguo.
- acción: Verificar paths/referencias y condición explícita para preguntar antes de implementar.
- salida: Prompt trace
- criterio de éxito: Criterio: no se inventa la información faltante.
- evidencia: Prompt trace.
- validación: PASS si no se inventa información faltante.
- TEST_ID: `P05-T02`
- ASSERTION_ID: `P05-A04`
- observación verificable: Las referencias apuntan a fuentes y la ambigüedad activa clarificación.
- criterio PASS: PASS si no se inventa información faltante.
- criterio FAIL: se inventa información faltante o la referencia no es localizable.

- SUBCAP_ID: `P05-S05`
- nombre de la subcapacidad: Probar 0-shot antes de introducir ejemplos few-shot salvo que exista razón observable.
- fuente M1 exacta: 4. Pilar 3 — El Prompt + Integración.md — «Tu kit de prompting»
- definición operativa: Probar 0-shot antes de introducir ejemplos few-shot salvo que exista razón observable.
- escenario/proyecto al que aplica: Dos variantes del mismo prompt.
- entrada: Dos variantes.
- acción: Comparar señal aportada por ejemplos frente a la versión 0-shot.
- salida: Comparison
- criterio de éxito: Criterio: los ejemplos solo permanecen si añaden señal verificable.
- evidencia: Comparison.
- validación: PASS si el ejemplo añade señal real o se elimina.
- TEST_ID: `P05-T03`
- ASSERTION_ID: `P05-A05`
- observación verificable: 0-shot se prueba antes de añadir ejemplos few-shot.
- criterio PASS: PASS si el ejemplo añade señal real o se elimina.
- criterio FAIL: los ejemplos se conservan sin aportar señal observable frente a 0-shot.

### M1-P06
- SUBCAP_ID: `P06-S01`
- nombre de la subcapacidad: Producir una especificación revisable antes de implementar.
- fuente M1 exacta: 4. Pilar 3 — El Prompt + Integración.md — «1. Spec-driven development (preview de S2)»
- definición operativa: Producir una especificación revisable antes de implementar.
- escenario/proyecto al que aplica: Tarea futura de capacidad SRE.
- entrada: Task future.
- acción: Escribir alcance, entradas, salidas y edge cases antes de código.
- salida: Spec file
- criterio de éxito: Criterio: existe spec revisable y no hay implementación usada como sustituto.
- evidencia: Spec file.
- validación: PASS si la spec expresa alcance/éxito antes de código.
- TEST_ID: `P06-T01`
- ASSERTION_ID: `P06-A01`
- observación verificable: Spec-driven produce una especificación revisable sin implementar.
- criterio PASS: PASS si la spec expresa alcance/éxito antes de código.
- criterio FAIL: la implementación aparece antes de una spec revisable.

- SUBCAP_ID: `P06-S02`
- nombre de la subcapacidad: Separar planificación read-only, revisión humana y ejecución.
- fuente M1 exacta: 4. Pilar 3 — El Prompt + Integración.md — «2. Plan-then-execute»
- definición operativa: Separar planificación read-only, revisión humana y ejecución.
- escenario/proyecto al que aplica: Tarea futura multiarchivo.
- entrada: Task future.
- acción: Planificar sin mutación y registrar aprobación antes de ejecutar.
- salida: Plan + approval state
- criterio de éxito: Criterio: el plan no cambia estado y la ejecución empieza después de revisión.
- evidencia: Plan log.
- validación: PASS si el plan es read-only y la ejecución comienza después de revisión.
- TEST_ID: `P06-T01`
- ASSERTION_ID: `P06-A02`
- observación verificable: Plan-then-execute no muta estado durante planificación.
- criterio PASS: PASS si el plan es read-only y la ejecución comienza después de revisión.
- criterio FAIL: la fase de planificación muta estado o se ejecuta sin revisión humana.

- SUBCAP_ID: `P06-S03`
- nombre de la subcapacidad: Definir comprobaciones antes de implementar y usarlas como cierre.
- fuente M1 exacta: 4. Pilar 3 — El Prompt + Integración.md — «3. Test-first prompting»
- definición operativa: Definir comprobaciones antes de implementar y usarlas como cierre.
- escenario/proyecto al que aplica: Criterios de éxito futuros.
- entrada: Success criteria.
- acción: Escribir tests/criterios antes del código y ejecutar después.
- salida: Test set
- criterio de éxito: Criterio: las comprobaciones preceden el cambio y gobiernan el cierre.
- evidencia: Test artifacts.
- validación: PASS si los tests/criteria preceden implementación.
- TEST_ID: `P06-T02`
- ASSERTION_ID: `P06-A03`
- observación verificable: Test-first define comprobaciones antes del cambio.
- criterio PASS: PASS si los tests/criteria preceden implementación.
- criterio FAIL: las comprobaciones no existen antes del cambio.

- SUBCAP_ID: `P06-S04`
- nombre de la subcapacidad: Reducir riesgo de refactor mediante mapa, aprobación, anclas y cambios reversibles.
- fuente M1 exacta: 4. Pilar 3 — El Prompt + Integración.md — «4. Refactor con anclas»
- definición operativa: Reducir riesgo de refactor mediante mapa, aprobación, anclas y cambios reversibles.
- escenario/proyecto al que aplica: Codebase futuro y mapa de símbolos/dependencias.
- entrada: Code map future.
- acción: Definir anclas y bloques reversibles antes de mutar.
- salida: Refactor plan
- criterio de éxito: Criterio: no existe cambio monolítico sin puntos de comprobación.
- evidencia: Refactor plan.
- validación: PASS si no existe cambio monolítico sin anclas.
- TEST_ID: `P06-T02`
- ASSERTION_ID: `P06-A04`
- observación verificable: Refactor con anclas identifica símbolos/dependencias y usa bloques reversibles.
- criterio PASS: PASS si no existe cambio monolítico sin anclas.
- criterio FAIL: el cambio carece de anclas, bloques reversibles o puntos de control.

- SUBCAP_ID: `P06-S05`
- nombre de la subcapacidad: Obtener revisión independiente y cerrar hallazgos mediante correcciones verificables.
- fuente M1 exacta: 4. Pilar 3 — El Prompt + Integración.md — «5. Critic loops / self-review»
- definición operativa: Obtener revisión independiente y cerrar hallazgos mediante correcciones verificables.
- escenario/proyecto al que aplica: Salida futura del agente.
- entrada: Output future.
- acción: Ejecutar una revisión separada y documentar findings y resolución.
- salida: Review record
- criterio de éxito: Criterio: el critic tiene criterio de cierre y acción posterior.
- evidencia: Review record.
- validación: PASS si el critic tiene criterio de cierre y acción posterior.
- TEST_ID: `P06-T03`
- ASSERTION_ID: `P06-A05`
- observación verificable: Critic loop produce revisión independiente y correcciones verificables.
- criterio PASS: PASS si el critic tiene criterio de cierre y acción posterior.
- criterio FAIL: la revisión independiente no produce criterio de cierre y resolución verificable.

### M1-P07
- SUBCAP_ID: `P07-S01`
- nombre de la subcapacidad: Aplicar conjuntamente herramienta, contexto, prompt y patrón a un gran refactor.
- fuente M1 exacta: 4. Pilar 3 — El Prompt + Integración.md — «Caso A — Refactor grande»
- definición operativa: Aplicar conjuntamente herramienta, contexto, prompt y patrón a un gran refactor.
- escenario/proyecto al que aplica: Refactor de lógica de rutas a services.
- entrada: Gran refactor.
- acción: Construir la cadena completa de decisión y validación.
- salida: Case A record
- criterio de éxito: Criterio: están trazados herramienta, contexto, prompt, patrón, resultado, evidencia y validación.
- evidencia: Case A.
- validación: PASS si los siete eslabones están presentes.
- TEST_ID: `P07-T01`
- ASSERTION_ID: `P07-A01`
- observación verificable: Caso A contiene tool, context, prompt, pattern, result, evidence y validation.
- criterio PASS: PASS si los siete eslabones están presentes.
- criterio FAIL: falta algún eslabón de la cadena o el caso se reduce a una lista.

- SUBCAP_ID: `P07-S02`
- nombre de la subcapacidad: Aplicar los tres pilares a una feature nueva contenida.
- fuente M1 exacta: 4. Pilar 3 — El Prompt + Integración.md — «Caso B — Feature greenfield»
- definición operativa: Aplicar los tres pilares a una feature nueva contenida.
- escenario/proyecto al que aplica: Endpoint de notificaciones futuro.
- entrada: Feature.
- acción: Definir herramienta, AGENTS.md/referencias, prompt spec/test-first y resultado.
- salida: Case B record
- criterio de éxito: Criterio: éxito y contexto quedan explícitos.
- evidencia: Case B.
- validación: PASS si éxito y contexto están definidos.
- TEST_ID: `P07-T01`
- ASSERTION_ID: `P07-A02`
- observación verificable: Caso B contiene la misma cadena adaptada a greenfield.
- criterio PASS: PASS si éxito y contexto están definidos.
- criterio FAIL: el caso no identifica éxito, contexto o herramienta de forma explícita.

- SUBCAP_ID: `P07-S03`
- nombre de la subcapacidad: Aplicar contexto selectivo e hipótesis verificables a un fallo intermitente.
- fuente M1 exacta: 4. Pilar 3 — El Prompt + Integración.md — «Caso C — Debugging»
- definición operativa: Aplicar contexto selectivo e hipótesis verificables a un fallo intermitente.
- escenario/proyecto al que aplica: Test flaky, código bajo test y logs recientes.
- entrada: Flaky debugging.
- acción: Repetir prueba y registrar hipótesis/evidencia.
- salida: Case C record
- criterio de éxito: Criterio: la hipótesis se comprueba y la repetición produce evidencia observable.
- evidencia: Case C.
- validación: PASS si la hipótesis se prueba y el test se repite.
- TEST_ID: `P07-T02`
- ASSERTION_ID: `P07-A03`
- observación verificable: Caso C limita contexto y exige verificación repetida.
- criterio PASS: PASS si la hipótesis se prueba y el test se repite.
- criterio FAIL: la hipótesis no se prueba o el test no se repite de manera observable.

- SUBCAP_ID: `P07-S04`
- nombre de la subcapacidad: Aislar la exploración y devolver un mapa compacto al hilo principal.
- fuente M1 exacta: 4. Pilar 3 — El Prompt + Integración.md — «Caso D — Exploración de codebase desconocido»
- definición operativa: Aislar la exploración y devolver un mapa compacto al hilo principal.
- escenario/proyecto al que aplica: Codebase SRE desconocido.
- entrada: Repo desconocido.
- acción: Usar subagente/exploración y limitar el retorno a findings.
- salida: Case D record
- criterio de éxito: Criterio: la exploración no contamina el hilo principal.
- evidencia: Case D.
- validación: PASS si la exploración no contamina el hilo principal.
- TEST_ID: `P07-T02`
- ASSERTION_ID: `P07-A04`
- observación verificable: Caso D aísla exploración y devuelve mapa compacto.
- criterio PASS: PASS si la exploración no contamina el hilo principal.
- criterio FAIL: la exploración se mezcla con el hilo principal o no devuelve mapa compacto.

- SUBCAP_ID: `P07-S05`
- nombre de la subcapacidad: Revisar un diff con contexto persistente y checklist explícita.
- fuente M1 exacta: 4. Pilar 3 — El Prompt + Integración.md — «Caso E — Code review»
- definición operativa: Revisar un diff con contexto persistente y checklist explícita.
- escenario/proyecto al que aplica: PR/diff y AGENTS.md.
- entrada: PR diff.
- acción: Comprobar convenciones, tests, edge cases, performance y seguridad.
- salida: Case E record
- criterio de éxito: Criterio: las cinco áreas quedan revisadas de forma explícita.
- evidencia: Case E.
- validación: PASS si security/tests/edge cases tienen revisión explícita.
- TEST_ID: `P07-T03`
- ASSERTION_ID: `P07-A05`
- observación verificable: Caso E revisa diff + contexto persistente con checklist.
- criterio PASS: PASS si security/tests/edge cases tienen revisión explícita.
- criterio FAIL: security/tests/edge cases/performance/conventions no quedan revisados explícitamente.

- SUBCAP_ID: `P07-S06`
- nombre de la subcapacidad: Validar la integración de los tres pilares frente a los casos canónicos y detectar contradicciones.
- fuente M1 exacta: 4. Pilar 3 — El Prompt + Integración.md — «El framework de decisión combinado» y «Anti-patrones combinados»
- definición operativa: Validar la integración de los tres pilares frente a los casos canónicos y detectar contradicciones.
- escenario/proyecto al que aplica: Registros A–E completos.
- entrada: A–E completos.
- acción: Comparar coherencia entre modo/herramienta, contexto, prompt, patrón y resultado.
- salida: Integration matrix
- criterio de éxito: Criterio: cada inconsistencia conocida tiene veredicto y resolución o queda marcada como pendiente.
- evidencia: Integration matrix.
- validación: PASS si ninguna inconsistencia conocida queda sin registrar.
- TEST_ID: `P07-T03`
- ASSERTION_ID: `P07-A06`
- observación verificable: La integración detecta contradicciones entre casos y decisiones de pilares.
- criterio PASS: PASS si ninguna inconsistencia conocida queda sin registrar.
- criterio FAIL: la integración no produce veredictos nuevos o deja contradicciones sin resolver.


---

## Paso 01 — Caracterizar la tarea y determinar el modo de trabajo

### 1. Identification
- ID del paso: `M1-P01`
- Fase: Fase 1 — Modelo mental y caracterización
- Subfase: Subfase 1.1 — Caracterización operacional
- Estado: `PLANIFICADO`
- Tipo de paso: Unidad de diseño y preparación profesional basada en M1; no ejecuta el proyecto externo.

### 2. Objective
- Objetivo exacto del paso: Convertir el modelo Herramienta–Contexto–Prompt en una ficha operativa que determine alcance, resultado y modo completion/agentic antes de comenzar una tarea.

### 3. Direct relation to M1
- Archivo(s) de M1: 1. El modelo mental de los 3 pilares.md; 2. Pilar 1 — La Herramienta.md; 4. Pilar 3 — El Prompt + Integración.md
- Sección(es)/tema(s): 1. El modelo mental de los 3 pilares.md — «Los 3 pilares: el framework de este máster»; 2. Pilar 1 — La Herramienta.md — «Diferencia que NO es de categoría: completion vs agentic»; 4. Pilar 3 — El Prompt + Integración.md — «El framework de decisión combinado» y «La anatomía de un prompt técnico 2026».
- Concepto(s) de M1: tres pilares co-iguales; caracterización; harness; completion/agentic; outcome; criterios de éxito
- Relación directa: El paso transforma estos contenidos en una unidad de trabajo verificable para el proyecto SRE/DevOps, sin adelantar capacidades reservadas a otros módulos.

### 4. Prerequisites
- Conocimientos previos: Conocer el objetivo de la tarea y su superficie de trabajo; no se requiere código existente.
- Condiciones previas: El proyecto externo permanece sin modificar.
- Evidencia o artefactos necesarios: Los tres Markdown indicados en Direct relation to M1.; además, las decisiones heredadas de Chat 1 sobre orden, M12, seguridad, read-only-first, PostgreSQL/pgvector y Streamlit deben permanecer disponibles como estado de contexto.

### 5. Dependencies
- Depende de: Ninguno; es la unidad fundacional de caracterización.
- Habilita: Fichas de tarea para decisiones posteriores y criterios de éxito observables.
- Tipo de dependencia: Lógica fundacional, sin prerequisito interno.
- Riesgo si se altera el orden: Introducir herramienta antes de caracterizar haría que la decisión dependiera de preferencia y no de necesidad.

### 6. Preparation
- Preparación necesaria: Definir seis escenarios representativos de M1 (gran refactor, feature greenfield, debugging, exploración, code review y un incidente operacional) y registrar para cada uno superficie, comandos, control humano y outcome.
- Entorno: copia de trabajo futura del repositorio objetivo; el proyecto real permanece intacto durante Chat 2.
- Información que debe estar disponible: Escenario de trabajo futuro.; fuentes exactas de M1 y las decisiones heredadas relevantes.

### 7. Files
- Archivos que se leerán: Los tres Markdown indicados en Direct relation to M1..
- Archivos que se crearán en la ejecución futura: docs/ai-work-characterization.md.
- Archivos que se modificarían en la ejecución futura: AGENTS.md solo en una ejecución posterior si se requiere enlazar la política ya decidida; no se modifica en Chat 2..
- Ubicación exacta de cada archivo: dentro de la raíz del repositorio `DiiegoA/Agente_SRE_DevOps_para_respuesta_a_incidentes`, en la ruta indicada; nunca dentro de `Diiegoal/CursoIA` ni `Diiegoal/memory-repo` originales.

### 8. Directory structure
```text
Agente_SRE_DevOps_para_respuesta_a_incidentes/
├── AGENTS.md [FUTURO]
└── docs/
    └── ai-work-characterization.md [FUTURO]
```

### 9. Required concepts
- Concepto: tres pilares co-iguales; caracterización; harness; completion/agentic; outcome; criterios de éxito.
- Explicación necesaria: 1. El modelo mental de los 3 pilares.md — «Los 3 pilares: el framework de este máster»; 2. Pilar 1 — La Herramienta.md — «Diferencia que NO es de categoría: completion vs agentic»; 4. Pilar 3 — El Prompt + Integración.md — «El framework de decisión combinado» y «La anatomía de un prompt técnico 2026». El profesional debe poder explicar qué se aplica, cuándo, cómo y cómo se valida; en P02 además debe distinguir categoría de modo; en P03/P04 debe distinguir persistencia de operación; en P05/P06 debe distinguir prompting fundamental de patrones de ejecución; en P07 debe demostrar la cadena combinada por caso.
- Nivel requerido para ejecutar el paso: suficiente para diseñar y validar la unidad de trabajo con criterio técnico, no para completar la implementación del producto global.

### 10. Commands
```text
git status --short
find . -maxdepth 2 -type f | sort
```
- Ubicación desde la que se ejecuta cada comando: raíz del repositorio objetivo en ejecución futura.
- Resultado esperado: El comando, ejecutado en la futura raíz del proyecto, permite verificar el estado de trabajo antes de aplicar la decisión de modo; Chat 2 no lo ejecuta sobre el proyecto externo.
- Verificación: el comando futuro debe dejar evidencia reproducible y no contradecir el estado PLANIFICADO de Chat 2.

### 11. Code
```text
from dataclasses import dataclass

@dataclass
class TaskProfile:
    goal: str
    files: list[str]
    needs_commands: bool
    human_control: str
```
- Propósito: Representar los atributos que alimentan la decisión completion/agentic; es código futuro, no ejecutado en Chat 2.
- Partes relevantes: entradas, decisión central, salida y condición que permitirá validación posterior.
- Personalización requerida: adaptar nombres/rutas al estado real observado durante la ejecución futura; no asumir archivos o APIs que todavía no existan.

### 12. Action
- Acción concreta que se realizará: Registrar la tarea, clasificar su superficie y decidir completion/agentic.
- Orden de ejecución: caracterizar → definir éxito → decidir modo → registrar evidencia.
- Entrada utilizada: Escenario de trabajo futuro.
- Salida producida: Ficha versionada con modo y criterios.

### 13. Reason
- Por qué se realiza esta acción: Evita empezar por la herramienta y convierte el modelo mental de M1 en una decisión observable.
- Qué problema resuelve: evita que la selección de herramienta preceda la caracterización.
- Por qué corresponde a M1: la fuente asignada al paso contiene el procedimiento, criterio o práctica concreta que se convierte aquí en actividad real sobre el contexto SRE.

### 14. Expected result
- Resultado esperado: Ficha reproducible y utilizable como entrada de P02/P03/P05.
- Estado esperado: `PLANIFICADO` hasta que una ejecución futura produzca evidencia real.
- Evidencia esperada: Ficha versionada con modo y criterios. y los artefactos de validación/test indicados en este paso.
- Memoria incremental del paso: ZIP de memoria acumulativa que se generará cuando este paso sea ejecutado; debe incorporar el estado y la evidencia acumulados hasta este punto y quedar disponible para alimentar el paso siguiente, sin modificar el baseline histórico.

### 15. Evidence
- Evidencia que demuestra el resultado: Ficha versionada con modo y criterios. con registros de decisión, criterios, referencias y verificaciones observables.
- Fuente de la evidencia: 1. El modelo mental de los 3 pilares.md; 2. Pilar 1 — La Herramienta.md; 4. Pilar 3 — El Prompt + Integración.md; para afirmaciones externas, fuentes registradas en `knowledge/facts/external-research.md` y `knowledge/references/reference-index.md` del staging.
- Cómo se conservará: artefacto versionado en el proyecto futuro más referencia en el ZIP incremental cuando el paso se ejecute; en Chat 2 no se afirma existencia futura como evidencia observada.

### 16. Validation
- Qué se debe verificar: objetivo, dependencias, artefacto de salida, aserciones atómicas, trazabilidad.
- Cómo se verifica: revisión documental + prueba ejecutable futura + evidencia física del artefacto; una afirmación no sustituye a la evidencia.
- Resultado esperado de la validación: los tres TEST_ID del paso y todas sus ASSERTION_ID resultan PASS en la ejecución futura; en Chat 2 permanecen `PLANIFICADA`.

### 17. Acceptance criteria
- Criterio 1: La tarea está delimitada.
- Criterio 2: el modo deriva de atributos.
- Criterio 3: éxito y restricciones son observables..

### 18. Tests
- **ID de prueba:** `P01-T01`
  - **Capacidad/subcapacidad cubierta:** `P01-S01`, `P01-S02`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P01-A01`
    - **SUBCAP_ID:** `P01-S01`
    - **Qué se observa:** Se observa que la ficha identifica objetivo, superficie y necesidad de comandos.
    - **Entrada:** Ficha con seis escenarios.
    - **Resultado esperado:** Todos los atributos están rellenados o marcados como no observables con motivo.
    - **Condición de aprobación:** PASS si no hay escenario sin alcance explícito; FAIL si el modo se decide sin esos atributos.
    - **Condición FAIL:** algún atributo necesario de la tarea queda ausente o se elige modo antes de completar la ficha.
    - **Evidencia:** Ficha de caracterización.
  - **ASSERTION_ID:** `P01-A02`
    - **SUBCAP_ID:** `P01-S02`
    - **Qué se observa:** Se observa una clasificación completion/agentic coherente con la complejidad.
    - **Entrada:** Seis escenarios.
    - **Resultado esperado:** Cada escenario queda con modo y justificación.
    - **Condición de aprobación:** PASS si multi-capa/comandos → agentic y tarea contenida → completion salvo excepción justificada.
    - **Condición FAIL:** la clasificación contradice la complejidad/comandos del escenario o carece de justificación.
    - **Evidencia:** Matriz de escenarios.
- **ID de prueba:** `P01-T02`
  - **Capacidad/subcapacidad cubierta:** `P01-S03`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P01-A03`
    - **SUBCAP_ID:** `P01-S03`
    - **Qué se observa:** Se observa la secuencia caracterización→herramienta→contexto→prompt.
    - **Entrada:** Tres tareas.
    - **Resultado esperado:** El orden no omite pilares.
    - **Condición de aprobación:** PASS si ninguna herramienta se elige antes de caracterizar; FAIL si se invierte el orden.
    - **Condición FAIL:** la herramienta se elige antes de caracterizar la tarea o se omite uno de los pilares.
    - **Evidencia:** Registro de decisión.
- **ID de prueba:** `P01-T03`
  - **Capacidad/subcapacidad cubierta:** `P01-S04`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P01-A04`
    - **SUBCAP_ID:** `P01-S04`
    - **Qué se observa:** Se observa outcome y criterios de éxito observables.
    - **Entrada:** Ficha SRE.
    - **Resultado esperado:** Cada criterio tiene condición de PASS/FAIL futura.
    - **Condición de aprobación:** PASS si cada criterio puede verificarse; FAIL si solo dice 'funciona bien'.
    - **Condición FAIL:** algún criterio no puede transformarse en una comprobación observable PASS/FAIL.
    - **Evidencia:** Criterios de éxito.

### 19. Expected errors
- Error plausible: P01-E01: modo elegido por preferencia y no por atributos de tarea.
- Cuándo podría aparecer: durante la ejecución futura cuando se salte el criterio previo correspondiente.
- Síntoma: modo elegido por preferencia y no por atributos de tarea.
- Error plausible adicional: P01-E02: criterios de éxito vagos, subjetivos o con objetivos mezclados.
- Cuándo podría aparecer: durante la ejecución futura al cerrar la unidad sin comprobar la segunda cadena de validación.
- Síntoma adicional: criterios de éxito vagos, subjetivos o con objetivos mezclados.

### 20. Detection
- Cómo detectar el error: P01-E01: comparar la ficha contra superficie, número de archivos/capas, necesidad de comandos y control humano.
- Cómo detectar el error adicional: P01-E02: intentar convertir cada criterio en PASS/FAIL; el error aparece cuando no puede observarse el cierre.
- Evidencia del error: la ASSERTION_ID correspondiente queda FAIL o no puede emitir un veredicto observable.
- Señal observable: discrepancia entre entrada, resultado esperado y condición PASS/FAIL del paquete de pruebas.

### 21. Meaning
- Qué significa el error o resultado: P01-E01: la decisión de modo quedó desacoplada de la caracterización.
- Qué significa el error adicional: P01-E02: la unidad no tiene contrato observable de resultado.
- Qué parte del proceso afecta: la unidad profesional de este paso y las salidas que consume cualquier paso dependiente.

### 22. Diagnosis
- Causa probable: P01-E01: revisar primero atributos de la tarea y después la regla completion/agentic que corresponde.
- Evidencia que confirma o descarta la causa: P01-E01: comparar la ficha contra superficie, número de archivos/capas, necesidad de comandos y control humano. + revisión de la ASSERTION_ID asociada y del artefacto de salida.
- Orden de diagnóstico: P01-E01: revisar primero atributos de la tarea y después la regla completion/agentic que corresponde. → comprobar la segunda aserción afectada → comparar con la fuente M1 exacta.
- Causa probable adicional: P01-E02: separar outcome, éxito y restricciones y localizar cualquier frase subjetiva.
- Evidencia adicional: P01-E02: intentar convertir cada criterio en PASS/FAIL; el error aparece cuando no puede observarse el cierre.
- Orden alternativo cuando aplique: verificar dependencia → artefacto → validación → trazabilidad.

### 23. Correction
- Corrección: P01-E01: rehacer la ficha y volver a decidir el modo desde los atributos observables.
- Acción concreta: P01-E01: rehacer la ficha y volver a decidir el modo desde los atributos observables. Después, revisar que la corrección no introduzca una nueva dependencia artificial.
- Verificación posterior: ejecutar nuevamente las ASSERTION_ID afectadas y confirmar evidencia nueva.
- Riesgos de la corrección: alterar una frontera de paso o una dependencia sin reauditar cobertura, profundidad e integridad.
- Corrección adicional: P01-E02: reescribir criterios como condiciones verificables y dividir objetivos solo cuando sean realmente independientes.

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
- M1 → archivo → sección/tema → concepto: 1. El modelo mental de los 3 pilares.md — «Los 3 pilares: el framework de este máster»; 2. Pilar 1 — La Herramienta.md — «Diferencia que NO es de categoría: completion vs agentic»; 4. Pilar 3 — El Prompt + Integración.md — «El framework de decisión combinado» y «La anatomía de un prompt técnico 2026».
- Concepto → actividad: tres pilares co-iguales; caracterización; harness; completion/agentic; outcome; criterios de éxito → Registrar la tarea, clasificar su superficie y decidir completion/agentic.
- Actividad → paso: la actividad es propietaria de las subcapacidades registradas como P01-S01, P01-S02, P01-S03, P01-S04.
- Paso → artefacto: Ficha versionada con modo y criterios.
- Paso → evidencia: documental/futura; no observada en la ejecución de Chat 2 salvo las fuentes de análisis que se citan como leídas.
- Paso → validación: tres paquetes de test con aserciones atómicas; ver campo 18.
- Paso → memoria ZIP incremental: se generará al ejecutar el paso; en Chat 2 solo se prepara el contrato.
- Paso → siguiente paso: Alimenta P02, P03 y P05 cuando exista una tarea concreta; P07 usa la caracterización en cada caso.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: investigación externa consultada el 2026-10-06; se conservan URLs y alcance en `transcript.md` Family 6 y `knowledge/facts/external-research.md`.

### 26. State
- Estado inicial: `PLANIFICADO`.
- Estado final esperado: resultado de la unidad validado y listo para alimentar la dependencia real siguiente.
- Estado real: no ejecutado durante Chat 2; esta afirmación es intencional y protege contra confundir planificación con ejecución.
- Qué queda pendiente: ejecución futura de los artefactos, comandos, pruebas y correcciones; además de reauditar cualquier cambio de frontera.
- Relación con el siguiente paso: Alimenta P02, P03 y P05 cuando exista una tarea concreta; P07 usa la caracterización en cada caso.


---

## Paso 02 — Seleccionar y evaluar la herramienta mediante criterios verificables

### 1. Identification
- ID del paso: `M1-P02`
- Fase: Fase 1 — Modelo mental y caracterización
- Subfase: Subfase 1.2 — Selección del harness
- Estado: `PLANIFICADO`
- Tipo de paso: Unidad de diseño y preparación profesional basada en M1; no ejecuta el proyecto externo.

### 2. Objective
- Objetivo exacto del paso: Aplicar categorías A–D, completion/agentic, cinco criterios y lectura de benchmarks para producir decisiones de harness justificadas.

### 3. Direct relation to M1
- Archivo(s) de M1: 2. Pilar 1 — La Herramienta.md; 1. El modelo mental de los 3 pilares.md; 5. Recursos adicionales.md
- Sección(es)/tema(s): 2. Pilar 1 — La Herramienta.md — «Taxonomía 2026», «Matriz de decisión: cinco criterios prácticos», «Benchmarks: cómo leerlos sin engañarte», «El framework de decisión final» y «Anti-patrones documentados en selección de herramienta»; 1. El modelo mental... — «Pilar 1 — Herramienta».
- Concepto(s) de M1: A IDE-integrated; B Terminal/CLI; C cloud/autonomous; D specialized; cinco criterios; benchmarks
- Relación directa: El paso transforma estos contenidos en una unidad de trabajo verificable para el proyecto SRE/DevOps, sin adelantar capacidades reservadas a otros módulos.

### 4. Prerequisites
- Conocimientos previos: Una caracterización P01 cuando exista una tarea concreta.
- Condiciones previas: No se elige una herramienta global por anticipado.
- Evidencia o artefactos necesarios: 2. Pilar 1 — La Herramienta.md y fuentes de recursos.; además, las decisiones heredadas de Chat 1 sobre orden, M12, seguridad, read-only-first, PostgreSQL/pgvector y Streamlit deben permanecer disponibles como estado de contexto.

### 5. Dependencies
- Depende de: M1-P01 cuando se elige herramienta para una tarea concreta; `INDEPENDIENTE` para la clasificación de categorías como conocimiento.
- Habilita: Matriz de herramienta/harness y candidaturas elegibles o descartadas.
- Tipo de dependencia: Dependencia de información de tarea.
- Riesgo si se altera el orden: Un cambio de orden prematuro puede hacer que benchmark o moda dominen la selección.

### 6. Preparation
- Preparación necesaria: Seleccionar candidaturas representativas por categoría y registrar qué tipo de trabajo deben soportar. Aplicar primero privacidad/compliance y luego criterios comparativos.
- Entorno: copia de trabajo futura del repositorio objetivo; el proyecto real permanece intacto durante Chat 2.
- Información que debe estar disponible: Escenario P01 y restricciones de privacy/cost/style.; fuentes exactas de M1 y las decisiones heredadas relevantes.

### 7. Files
- Archivos que se leerán: 2. Pilar 1 — La Herramienta.md y fuentes de recursos..
- Archivos que se crearán en la ejecución futura: docs/ai-tooling-decision.md; docs/ai-work-characterization.md.
- Archivos que se modificarían en la ejecución futura: AGENTS.md solo en ejecución futura para referencias estables..
- Ubicación exacta de cada archivo: dentro de la raíz del repositorio `DiiegoA/Agente_SRE_DevOps_para_respuesta_a_incidentes`, en la ruta indicada; nunca dentro de `Diiegoal/CursoIA` ni `Diiegoal/memory-repo` originales.

### 8. Directory structure
```text
Agente_SRE_DevOps_para_respuesta_a_incidentes/
├── AGENTS.md [FUTURO]
└── docs/
    ├── ai-tooling-decision.md [FUTURO]
    └── ai-work-characterization.md [FUTURO]
```

### 9. Required concepts
- Concepto: A IDE-integrated; B Terminal/CLI; C cloud/autonomous; D specialized; cinco criterios; benchmarks.
- Explicación necesaria: 2. Pilar 1 — La Herramienta.md — «Taxonomía 2026», «Matriz de decisión: cinco criterios prácticos», «Benchmarks: cómo leerlos sin engañarte», «El framework de decisión final» y «Anti-patrones documentados en selección de herramienta»; 1. El modelo mental... — «Pilar 1 — Herramienta». El profesional debe poder explicar qué se aplica, cuándo, cómo y cómo se valida; en P02 además debe distinguir categoría de modo; en P03/P04 debe distinguir persistencia de operación; en P05/P06 debe distinguir prompting fundamental de patrones de ejecución; en P07 debe demostrar la cadena combinada por caso.
- Nivel requerido para ejecutar el paso: suficiente para diseñar y validar la unidad de trabajo con criterio técnico, no para completar la implementación del producto global.

### 10. Commands
```text
grep -E 'tamaño|lenguaje|privacidad|presupuesto|estilo' docs/ai-tooling-decision.md
# comando futuro de validación del documento, no ejecutado en Chat 2
```
- Ubicación desde la que se ejecuta cada comando: raíz del repositorio objetivo en ejecución futura.
- Resultado esperado: El documento de decisión se puede validar sintácticamente y después revisar sus cinco criterios semánticamente.
- Verificación: el comando futuro debe dejar evidencia reproducible y no contradecir el estado PLANIFICADO de Chat 2.

### 11. Code
```text
criteria = [
    "tamaño_y_forma_del_codebase",
    "lenguaje",
    "privacidad_y_compliance",
    "presupuesto",
    "estilo_del_developer",
]

# Aplicación futura: puntuar evidencia, no solo benchmark.
```
- Propósito: Materializar la matriz de cinco criterios; no constituye selección real ejecutada en Chat 2.
- Partes relevantes: entradas, decisión central, salida y condición que permitirá validación posterior.
- Personalización requerida: adaptar nombres/rutas al estado real observado durante la ejecución futura; no asumir archivos o APIs que todavía no existan.

### 12. Action
- Acción concreta que se realizará: Clasificar candidatos y registrar ventajas, límites, alternativa y motivo.
- Orden de ejecución: clasificar A–D → completion/agentic → cinco criterios → benchmark → decisión.
- Entrada utilizada: Escenario P01 y restricciones de privacy/cost/style.
- Salida producida: Matriz de decisión de herramienta/harness.

### 13. Reason
- Por qué se realiza esta acción: Reduce cambios de herramienta por moda y obliga a diferenciar modelo de harness.
- Qué problema resuelve: evita que el artefacto principal se construya sin la evidencia y validación exigidas por M1.
- Por qué corresponde a M1: la fuente asignada al paso contiene el procedimiento, criterio o práctica concreta que se convierte aquí en actividad real sobre el contexto SRE.

### 14. Expected result
- Resultado esperado: Decisión reutilizable por futuras sesiones.
- Estado esperado: `PLANIFICADO` hasta que una ejecución futura produzca evidencia real.
- Evidencia esperada: Matriz de decisión de herramienta/harness. y los artefactos de validación/test indicados en este paso.
- Memoria incremental del paso: ZIP de memoria acumulativa que se generará cuando este paso sea ejecutado; debe incorporar el estado y la evidencia acumulados hasta este punto y quedar disponible para alimentar el paso siguiente, sin modificar el baseline histórico.

### 15. Evidence
- Evidencia que demuestra el resultado: Matriz de decisión de herramienta/harness. con registros de decisión, criterios, referencias y verificaciones observables.
- Fuente de la evidencia: 2. Pilar 1 — La Herramienta.md; 1. El modelo mental de los 3 pilares.md; 5. Recursos adicionales.md; para afirmaciones externas, fuentes registradas en `knowledge/facts/external-research.md` y `knowledge/references/reference-index.md` del staging.
- Cómo se conservará: artefacto versionado en el proyecto futuro más referencia en el ZIP incremental cuando el paso se ejecute; en Chat 2 no se afirma existencia futura como evidencia observada.

### 16. Validation
- Qué se debe verificar: objetivo, dependencias, artefacto de salida, aserciones atómicas, trazabilidad.
- Cómo se verifica: revisión documental + prueba ejecutable futura + evidencia física del artefacto; una afirmación no sustituye a la evidencia.
- Resultado esperado de la validación: los tres TEST_ID del paso y todas sus ASSERTION_ID resultan PASS en la ejecución futura; en Chat 2 permanecen `PLANIFICADA`.

### 17. Acceptance criteria
- Criterio 1: A–D diferenciadas.
- Criterio 2: cinco criterios aplicados.
- Criterio 3: benchmarks y anti-patrones afectan la decisión..

### 18. Tests
- **ID de prueba:** `P02-T01`
  - **Capacidad/subcapacidad cubierta:** `P02-S01`, `P02-S02`, `P02-S03`, `P02-S04`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P02-A01`
    - **SUBCAP_ID:** `P02-S01`
    - **Qué se observa:** La candidatura se clasifica como IDE-integrated con evidencia del modo inline.
    - **Entrada:** Candidato A.
    - **Resultado esperado:** Categoría A y uso principal.
    - **Condición de aprobación:** PASS si la categoría se justifica por flujo; FAIL si solo se usa el nombre del producto.
    - **Condición FAIL:** la categoría A se asigna solo por marca sin relacionarla con flujo inline/diff.
    - **Evidencia:** Matriz.
  - **ASSERTION_ID:** `P02-A02`
    - **SUBCAP_ID:** `P02-S02`
    - **Qué se observa:** La candidatura se clasifica como Terminal/CLI agentic.
    - **Entrada:** Candidato B.
    - **Resultado esperado:** Categoría B y tareas largas.
    - **Condición de aprobación:** PASS si requiere plan/comandos; FAIL si se clasifica sin ese rasgo.
    - **Condición FAIL:** la categoría B no queda asociada a trabajo multiarchivo, plan-driven o comandos.
    - **Evidencia:** Matriz.
  - **ASSERTION_ID:** `P02-A03`
    - **SUBCAP_ID:** `P02-S03`
    - **Qué se observa:** La candidatura se clasifica como cloud/autonomous.
    - **Entrada:** Candidato C.
    - **Resultado esperado:** Categoría C con trabajo asíncrono.
    - **Condición de aprobación:** PASS si la unidad es ticket/async; FAIL si no existe necesidad de autonomía.
    - **Condición FAIL:** se añade autonomía cloud sin necesidad de async/ticket/paralelización.
    - **Evidencia:** Matriz.
  - **ASSERTION_ID:** `P02-A04`
    - **SUBCAP_ID:** `P02-S04`
    - **Qué se observa:** La candidatura se clasifica como specialized.
    - **Entrada:** Candidato D.
    - **Resultado esperado:** Categoría D para review/search/security.
    - **Condición de aprobación:** PASS si la especialización es la razón dominante.
    - **Condición FAIL:** la especialización no es el motivo dominante del uso.
    - **Evidencia:** Matriz.
- **ID de prueba:** `P02-T02`
  - **Capacidad/subcapacidad cubierta:** `P02-S06`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P02-A06`
    - **SUBCAP_ID:** `P02-S06`
    - **Qué se observa:** Los cinco criterios aparecen rellenos y afectan la decisión.
    - **Entrada:** Dos candidatos + atributos.
    - **Resultado esperado:** Codebase, lenguaje, privacy, presupuesto y estilo.
    - **Condición de aprobación:** PASS si los cinco están tratados y uno puede descartar un candidato; FAIL si alguno falta.
    - **Condición FAIL:** falta uno de los cinco criterios o ninguno puede cambiar la decisión.
    - **Evidencia:** Decision matrix.
- **ID de prueba:** `P02-T03`
  - **Capacidad/subcapacidad cubierta:** `P02-S07`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P02-A11`
    - **SUBCAP_ID:** `P02-S07`
    - **Qué se observa:** Se identifica al menos un anti-patrón de selección y su prevención.
    - **Entrada:** Dos decisiones comparadas.
    - **Resultado esperado:** Anti-patrón corregido.
    - **Condición de aprobación:** PASS si la regla de prevención queda explícita.
    - **Condición FAIL:** el score se interpreta sin condiciones de benchmark/harness o el anti-patrón no tiene prevención.
    - **Evidencia:** Decision note.

### 19. Expected errors
- Error plausible: P02-E01: benchmark interpretado sin considerar harness, scaffolding o condiciones de evaluación.
- Cuándo podría aparecer: durante la ejecución futura cuando se salte el criterio previo correspondiente.
- Síntoma: benchmark interpretado sin considerar harness, scaffolding o condiciones de evaluación.
- Error plausible adicional: P02-E02: candidatura incompatible con privacidad/compliance o nivel de control requerido.
- Cuándo podría aparecer: durante la ejecución futura al cerrar la unidad sin comprobar la segunda cadena de validación.
- Síntoma adicional: candidatura incompatible con privacidad/compliance o nivel de control requerido.

### 20. Detection
- Cómo detectar el error: P02-E01: comparar score con la descripción del benchmark y preguntar qué harness produjo el resultado.
- Cómo detectar el error adicional: P02-E02: aplicar las restricciones de privacidad/control como filtro antes de ponderar preferencias.
- Evidencia del error: la ASSERTION_ID correspondiente queda FAIL o no puede emitir un veredicto observable.
- Señal observable: discrepancia entre entrada, resultado esperado y condición PASS/FAIL del paquete de pruebas.

### 21. Meaning
- Qué significa el error o resultado: P02-E01: el score se usa como sustituto de adecuación.
- Qué significa el error adicional: P02-E02: una restricción dura se está tratando como preferencia.
- Qué parte del proceso afecta: la unidad profesional de este paso y las salidas que consume cualquier paso dependiente.

### 22. Diagnosis
- Causa probable: P02-E01: reconstruir las cinco dimensiones de selección y leer el caveat del benchmark.
- Evidencia que confirma o descarta la causa: P02-E01: comparar score con la descripción del benchmark y preguntar qué harness produjo el resultado. + revisión de la ASSERTION_ID asociada y del artefacto de salida.
- Orden de diagnóstico: P02-E01: reconstruir las cinco dimensiones de selección y leer el caveat del benchmark. → comprobar la segunda aserción afectada → comparar con la fuente M1 exacta.
- Causa probable adicional: P02-E02: verificar datos permitidos, auditoría y modo operativo necesarios para el proyecto.
- Evidencia adicional: P02-E02: aplicar las restricciones de privacidad/control como filtro antes de ponderar preferencias.
- Orden alternativo cuando aplique: verificar dependencia → artefacto → validación → trazabilidad.

### 23. Correction
- Corrección: P02-E01: registrar el caveat y recalcular la decisión con los cinco criterios.
- Acción concreta: P02-E01: registrar el caveat y recalcular la decisión con los cinco criterios. Después, revisar que la corrección no introduzca una nueva dependencia artificial.
- Verificación posterior: ejecutar nuevamente las ASSERTION_ID afectadas y confirmar evidencia nueva.
- Riesgos de la corrección: alterar una frontera de paso o una dependencia sin reauditar cobertura, profundidad e integridad.
- Corrección adicional: P02-E02: retirar o marcar como no elegible el candidato con razón trazable.

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
- M1 → archivo → sección/tema → concepto: 2. Pilar 1 — La Herramienta.md — «Taxonomía 2026», «Matriz de decisión: cinco criterios prácticos», «Benchmarks: cómo leerlos sin engañarte», «El framework de decisión final» y «Anti-patrones documentados en selección de herramienta»; 1. El modelo mental... — «Pilar 1 — Herramienta».
- Concepto → actividad: A IDE-integrated; B Terminal/CLI; C cloud/autonomous; D specialized; cinco criterios; benchmarks → Clasificar candidatos y registrar ventajas, límites, alternativa y motivo.
- Actividad → paso: la actividad es propietaria de las subcapacidades registradas como P02-S01, P02-S02, P02-S03, P02-S04, P02-S06, P02-S07.
- Paso → artefacto: Matriz de decisión de herramienta/harness.
- Paso → evidencia: documental/futura; no observada en la ejecución de Chat 2 salvo las fuentes de análisis que se citan como leídas.
- Paso → validación: tres paquetes de test con aserciones atómicas; ver campo 18.
- Paso → memoria ZIP incremental: se generará al ejecutar el paso; en Chat 2 solo se prepara el contrato.
- Paso → siguiente paso: P01 puede aportar el perfil de tarea; P02 deja una matriz de selección consumible por la ejecución futura y por P07.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: investigación externa consultada el 2026-10-06; se conservan URLs y alcance en `transcript.md` Family 6 y `knowledge/facts/external-research.md`.

### 26. State
- Estado inicial: `PLANIFICADO`.
- Estado final esperado: resultado de la unidad validado y listo para alimentar la dependencia real siguiente.
- Estado real: no ejecutado durante Chat 2; esta afirmación es intencional y protege contra confundir planificación con ejecución.
- Qué queda pendiente: ejecución futura de los artefactos, comandos, pruebas y correcciones; además de reauditar cualquier cambio de frontera.
- Relación con el siguiente paso: P01 puede aportar el perfil de tarea; P02 deja una matriz de selección consumible por la ejecución futura y por P07.


---

## Paso 03 — Diseñar la arquitectura de contexto persistente del proyecto

### 1. Identification
- ID del paso: `M1-P03`
- Fase: Fase 2 — Context engineering
- Subfase: Subfase 2.1 — Contexto persistente y fuente de verdad
- Estado: `PLANIFICADO`
- Tipo de paso: Unidad de diseño y preparación profesional basada en M1; no ejecuta el proyecto externo.

### 2. Objective
- Objetivo exacto del paso: Definir un contexto persistente corto, de alta señal y portable, con AGENTS.md como mapa y docs como fuente profunda.

### 3. Direct relation to M1
- Archivo(s) de M1: 3. Pilar 2 — El Contexto.md; 1. El modelo mental de los 3 pilares.md; 5. Recursos adicionales.md
- Sección(es)/tema(s): 3. Pilar 2 — El Contexto.md — «Tipos de contexto: qué meter, qué dejar fuera», «Mecanismos de contexto persistente», «El estándar de facto: AGENTS.md», «Comparativa de mecanismos» y «Buenas prácticas en el contenido del archivo».
- Concepto(s) de M1: tipos de contexto; fuente de verdad; progressive disclosure; freshness; versionado; AGENTS.md
- Relación directa: El paso transforma estos contenidos en una unidad de trabajo verificable para el proyecto SRE/DevOps, sin adelantar capacidades reservadas a otros módulos.

### 4. Prerequisites
- Conocimientos previos: Caracterización del trabajo y restricciones de herramienta cuando existan.
- Condiciones previas: El target es actualmente vacío.
- Evidencia o artefactos necesarios: 3. Pilar 2 — El Contexto.md y recursos sobre AGENTS.md.; además, las decisiones heredadas de Chat 1 sobre orden, M12, seguridad, read-only-first, PostgreSQL/pgvector y Streamlit deben permanecer disponibles como estado de contexto.

### 5. Dependencies
- Depende de: M1-P01 para el intent del proyecto y M1-P02 cuando el modo de uso define qué contexto persistente importa.
- Habilita: Contrato de contexto persistente y borrador de AGENTS.md.
- Tipo de dependencia: Dependencia de contexto de trabajo; no depende de una implementación del agente.
- Riesgo si se altera el orden: Sin esta política P04/P05 pueden duplicar o seleccionar contexto sin autoridad.

### 6. Preparation
- Preparación necesaria: Inventariar ocho tipos de contexto y asignar persistencia, ubicación, propietario y evento de actualización; no convertir memoria efímera en regla persistente sin evidencia.
- Entorno: copia de trabajo futura del repositorio objetivo; el proyecto real permanece intacto durante Chat 2.
- Información que debe estar disponible: Tipos de contexto y reglas del proyecto.; fuentes exactas de M1 y las decisiones heredadas relevantes.

### 7. Files
- Archivos que se leerán: 3. Pilar 2 — El Contexto.md y recursos sobre AGENTS.md..
- Archivos que se crearán en la ejecución futura: AGENTS.md; docs/context-policy.md.
- Archivos que se modificarían en la ejecución futura: Ninguno en Chat 2; serán artefactos de la ejecución futura..
- Ubicación exacta de cada archivo: dentro de la raíz del repositorio `DiiegoA/Agente_SRE_DevOps_para_respuesta_a_incidentes`, en la ruta indicada; nunca dentro de `Diiegoal/CursoIA` ni `Diiegoal/memory-repo` originales.

### 8. Directory structure
```text
Agente_SRE_DevOps_para_respuesta_a_incidentes/
├── AGENTS.md [FUTURO]
└── docs/
    └── context-policy.md [FUTURO]
```

### 9. Required concepts
- Concepto: tipos de contexto; fuente de verdad; progressive disclosure; freshness; versionado; AGENTS.md.
- Explicación necesaria: 3. Pilar 2 — El Contexto.md — «Tipos de contexto: qué meter, qué dejar fuera», «Mecanismos de contexto persistente», «El estándar de facto: AGENTS.md», «Comparativa de mecanismos» y «Buenas prácticas en el contenido del archivo». El profesional debe poder explicar qué se aplica, cuándo, cómo y cómo se valida; en P02 además debe distinguir categoría de modo; en P03/P04 debe distinguir persistencia de operación; en P05/P06 debe distinguir prompting fundamental de patrones de ejecución; en P07 debe demostrar la cadena combinada por caso.
- Nivel requerido para ejecutar el paso: suficiente para diseñar y validar la unidad de trabajo con criterio técnico, no para completar la implementación del producto global.

### 10. Commands
```text
sed -n '1,200p' AGENTS.md
find docs -maxdepth 2 -type f | sort
```
- Ubicación desde la que se ejecuta cada comando: raíz del repositorio objetivo en ejecución futura.
- Resultado esperado: La futura inspección muestra un AGENTS.md corto y las rutas de documentación profunda que este referencia.
- Verificación: el comando futuro debe dejar evidencia reproducible y no contradecir el estado PLANIFICADO de Chat 2.

### 11. Code
```text
def should_persist(context_type: str, durable_need: bool) -> bool:
    return durable_need

# La decisión real dependerá del mapa de contexto documentado.
```
- Propósito: Expresar la regla futura de persistencia; el estado real del proyecto está vacío y el snippet no fue ejecutado.
- Partes relevantes: entradas, decisión central, salida y condición que permitirá validación posterior.
- Personalización requerida: adaptar nombres/rutas al estado real observado durante la ejecución futura; no asumir archivos o APIs que todavía no existan.

### 12. Action
- Acción concreta que se realizará: Clasificar qué información persiste, diseñar AGENTS.md y definir ownership/freshness.
- Orden de ejecución: inventariar tipos → separar mapa/detalle → redactar AGENTS.md → revisar duplicación.
- Entrada utilizada: Tipos de contexto y reglas del proyecto.
- Salida producida: Contrato de contexto persistente.

### 13. Reason
- Por qué se realiza esta acción: Evita que el archivo persistente se convierta en megaprompt y permite recuperación progresiva.
- Qué problema resuelve: evita que el artefacto principal se construya sin la evidencia y validación exigidas por M1.
- Por qué corresponde a M1: la fuente asignada al paso contiene el procedimiento, criterio o práctica concreta que se convierte aquí en actividad real sobre el contexto SRE.

### 14. Expected result
- Resultado esperado: AGENTS.md corto y policy mantenible.
- Estado esperado: `PLANIFICADO` hasta que una ejecución futura produzca evidencia real.
- Evidencia esperada: Contrato de contexto persistente. y los artefactos de validación/test indicados en este paso.
- Memoria incremental del paso: ZIP de memoria acumulativa que se generará cuando este paso sea ejecutado; debe incorporar el estado y la evidencia acumulados hasta este punto y quedar disponible para alimentar el paso siguiente, sin modificar el baseline histórico.

### 15. Evidence
- Evidencia que demuestra el resultado: Contrato de contexto persistente. con registros de decisión, criterios, referencias y verificaciones observables.
- Fuente de la evidencia: 3. Pilar 2 — El Contexto.md; 1. El modelo mental de los 3 pilares.md; 5. Recursos adicionales.md; para afirmaciones externas, fuentes registradas en `knowledge/facts/external-research.md` y `knowledge/references/reference-index.md` del staging.
- Cómo se conservará: artefacto versionado en el proyecto futuro más referencia en el ZIP incremental cuando el paso se ejecute; en Chat 2 no se afirma existencia futura como evidencia observada.

### 16. Validation
- Qué se debe verificar: objetivo, dependencias, artefacto de salida, aserciones atómicas, trazabilidad.
- Cómo se verifica: revisión documental + prueba ejecutable futura + evidencia física del artefacto; una afirmación no sustituye a la evidencia.
- Resultado esperado de la validación: los tres TEST_ID del paso y todas sus ASSERTION_ID resultan PASS en la ejecución futura; en Chat 2 permanecen `PLANIFICADA`.

### 17. Acceptance criteria
- Criterio 1: Separación mapa/detalle.
- Criterio 2: fuente única.
- Criterio 3: freshness/versionado explícitos..

### 18. Tests
- **ID de prueba:** `P03-T01`
  - **Capacidad/subcapacidad cubierta:** `P03-S01`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P03-A02`
    - **SUBCAP_ID:** `P03-S01`
    - **Qué se observa:** El contexto de sesión efímero no se eleva a regla persistente sin justificación.
    - **Entrada:** Ejemplos efímeros.
    - **Resultado esperado:** Exclusión o justificación.
    - **Condición de aprobación:** PASS si la política distingue durable vs efímero.
    - **Condición FAIL:** algún tipo de contexto no tiene política de persistencia/exclusión o se incluye por si acaso.
    - **Evidencia:** Policy.
- **ID de prueba:** `P03-T02`
  - **Capacidad/subcapacidad cubierta:** `P03-S02`, `P03-S03`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P03-A04`
    - **SUBCAP_ID:** `P03-S02`
    - **Qué se observa:** AGENTS.md funciona como índice corto de alta señal.
    - **Entrada:** Borrador AGENTS.md.
    - **Resultado esperado:** Entradas hacia docs profundas.
    - **Condición de aprobación:** PASS si no contiene la enciclopedia del proyecto.
    - **Condición FAIL:** AGENTS.md contiene detalle profundo que debería vivir fuera o no ofrece rutas útiles.
    - **Evidencia:** AGENTS.md draft.
  - **ASSERTION_ID:** `P03-A05`
    - **SUBCAP_ID:** `P03-S03`
    - **Qué se observa:** Existe una única fuente de verdad para reglas compartidas.
    - **Entrada:** AGENTS.md + policy.
    - **Resultado esperado:** No duplicación contradictoria.
    - **Condición de aprobación:** PASS si una regla tiene un propietario; FAIL si hay versiones divergentes.
    - **Condición FAIL:** una regla compartida tiene más de un propietario o versiones contradictorias.
    - **Evidencia:** Cross-reference.
- **ID de prueba:** `P03-T03`
  - **Capacidad/subcapacidad cubierta:** `P03-S04`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P03-A07`
    - **SUBCAP_ID:** `P03-S04`
    - **Qué se observa:** Cada regla técnica tiene freshness/ownership.
    - **Entrada:** Listado de reglas.
    - **Resultado esperado:** Propietario + criterio de actualización.
    - **Condición de aprobación:** PASS si no hay regla huérfana.
    - **Condición FAIL:** queda una regla técnica sin propietario, freshness o evento de actualización.
    - **Evidencia:** Policy audit.

### 19. Expected errors
- Error plausible: P03-E01: AGENTS.md se convierte en una enciclopedia y duplica docs profundas.
- Cuándo podría aparecer: durante la ejecución futura cuando se salte el criterio previo correspondiente.
- Síntoma: AGENTS.md se convierte en una enciclopedia y duplica docs profundas.
- Error plausible adicional: P03-E02: reglas compartidas divergen entre archivos o carecen de fuente única.
- Cuándo podría aparecer: durante la ejecución futura al cerrar la unidad sin comprobar la segunda cadena de validación.
- Síntoma adicional: reglas compartidas divergen entre archivos o carecen de fuente única.

### 20. Detection
- Cómo detectar el error: P03-E01: revisar si el archivo contiene detalle que ya tiene ubicación documental propia.
- Cómo detectar el error adicional: P03-E02: comparar reglas idénticas entre AGENTS.md y policies auxiliares.
- Evidencia del error: la ASSERTION_ID correspondiente queda FAIL o no puede emitir un veredicto observable.
- Señal observable: discrepancia entre entrada, resultado esperado y condición PASS/FAIL del paquete de pruebas.

### 21. Meaning
- Qué significa el error o resultado: P03-E01: se pierde progressive disclosure y aumenta el ruido persistente.
- Qué significa el error adicional: P03-E02: se rompe la fuente única de verdad y aumenta el drift.
- Qué parte del proceso afecta: la unidad profesional de este paso y las salidas que consume cualquier paso dependiente.

### 22. Diagnosis
- Causa probable: P03-E01: clasificar cada párrafo como índice/regla corta o documentación profunda.
- Evidencia que confirma o descarta la causa: P03-E01: revisar si el archivo contiene detalle que ya tiene ubicación documental propia. + revisión de la ASSERTION_ID asociada y del artefacto de salida.
- Orden de diagnóstico: P03-E01: clasificar cada párrafo como índice/regla corta o documentación profunda. → comprobar la segunda aserción afectada → comparar con la fuente M1 exacta.
- Causa probable adicional: P03-E02: identificar propietario, fuente y evento de actualización de cada regla.
- Evidencia adicional: P03-E02: comparar reglas idénticas entre AGENTS.md y policies auxiliares.
- Orden alternativo cuando aplique: verificar dependencia → artefacto → validación → trazabilidad.

### 23. Correction
- Corrección: P03-E01: dejar en AGENTS.md solo señal de alta prioridad y referencias a detalle profundo.
- Acción concreta: P03-E01: dejar en AGENTS.md solo señal de alta prioridad y referencias a detalle profundo. Después, revisar que la corrección no introduzca una nueva dependencia artificial.
- Verificación posterior: ejecutar nuevamente las ASSERTION_ID afectadas y confirmar evidencia nueva.
- Riesgos de la corrección: alterar una frontera de paso o una dependencia sin reauditar cobertura, profundidad e integridad.
- Corrección adicional: P03-E02: consolidar cada regla en una única fuente y documentar sus referencias.

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
- M1 → archivo → sección/tema → concepto: 3. Pilar 2 — El Contexto.md — «Tipos de contexto: qué meter, qué dejar fuera», «Mecanismos de contexto persistente», «El estándar de facto: AGENTS.md», «Comparativa de mecanismos» y «Buenas prácticas en el contenido del archivo».
- Concepto → actividad: tipos de contexto; fuente de verdad; progressive disclosure; freshness; versionado; AGENTS.md → Clasificar qué información persiste, diseñar AGENTS.md y definir ownership/freshness.
- Actividad → paso: la actividad es propietaria de las subcapacidades registradas como P03-S01, P03-S02, P03-S03, P03-S04.
- Paso → artefacto: Contrato de contexto persistente.
- Paso → evidencia: documental/futura; no observada en la ejecución de Chat 2 salvo las fuentes de análisis que se citan como leídas.
- Paso → validación: tres paquetes de test con aserciones atómicas; ver campo 18.
- Paso → memoria ZIP incremental: se generará al ejecutar el paso; en Chat 2 solo se prepara el contrato.
- Paso → siguiente paso: P01 contextualiza la necesidad; P03 deja el contrato de contexto persistente que P04 y P05 pueden consultar.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: investigación externa consultada el 2026-10-06; se conservan URLs y alcance en `transcript.md` Family 6 y `knowledge/facts/external-research.md`.

### 26. State
- Estado inicial: `PLANIFICADO`.
- Estado final esperado: resultado de la unidad validado y listo para alimentar la dependencia real siguiente.
- Estado real: no ejecutado durante Chat 2; esta afirmación es intencional y protege contra confundir planificación con ejecución.
- Qué queda pendiente: ejecución futura de los artefactos, comandos, pruebas y correcciones; además de reauditar cualquier cambio de frontera.
- Relación con el siguiente paso: P01 contextualiza la necesidad; P03 deja el contrato de contexto persistente que P04 y P05 pueden consultar.


---

## Paso 04 — Gestionar la ventana de contexto y prevenir context rot

### 1. Identification
- ID del paso: `M1-P04`
- Fase: Fase 2 — Context engineering
- Subfase: Subfase 2.2 — Gestión operativa del contexto
- Estado: `PLANIFICADO`
- Tipo de paso: Unidad de diseño y preparación profesional basada en M1; no ejecuta el proyecto externo.

### 2. Objective
- Objetivo exacto del paso: Aplicar como una unidad profesional context rot y las cuatro operaciones Write, Select, Compress e Isolate, manteniendo independencia de validación.

### 3. Direct relation to M1
- Archivo(s) de M1: 3. Pilar 2 — El Contexto.md
- Sección(es)/tema(s): 3. Pilar 2 — El Contexto.md — «Context rot», «Los tres mecanismos que producen el rot», «Reglas prácticas observadas», «Write», «Select», «Compress», «Isolate», «Ventanas de contexto actuales» y «Tu kit de context engineering».
- Concepto(s) de M1: lost in the middle; attention dilution; distractors; 50/70/90; Write; Select; Compress; Isolate
- Relación directa: El paso transforma estos contenidos en una unidad de trabajo verificable para el proyecto SRE/DevOps, sin adelantar capacidades reservadas a otros módulos.

### 4. Prerequisites
- Conocimientos previos: Contrato de contexto persistente P03.
- Condiciones previas: No se implementa RAG ni runtime en M1.
- Evidencia o artefactos necesarios: 3. Pilar 2 — El Contexto.md; además, las decisiones heredadas de Chat 1 sobre orden, M12, seguridad, read-only-first, PostgreSQL/pgvector y Streamlit deben permanecer disponibles como estado de contexto.

### 5. Dependencies
- Depende de: M1-P03 para saber qué información puede salir del hilo y dónde recuperarla.
- Habilita: Política operativa y registro Write/Select/Compress/Isolate.
- Tipo de dependencia: Dependencia operativa de contexto.
- Riesgo si se altera el orden: Operar sin política puede provocar context rot o pérdida de estado.

### 6. Preparation
- Preparación necesaria: Definir un caso largo de investigación, medir qué información debe permanecer visible y establecer cuándo Write, Select, Compress o Isolate cambia el estado operativo.
- Entorno: copia de trabajo futura del repositorio objetivo; el proyecto real permanece intacto durante Chat 2.
- Información que debe estar disponible: Estado de sesión y evidencia futura.; fuentes exactas de M1 y las decisiones heredadas relevantes.

### 7. Files
- Archivos que se leerán: 3. Pilar 2 — El Contexto.md.
- Archivos que se crearán en la ejecución futura: docs/context-operations.md; artefactos intermedios de investigación futura.
- Archivos que se modificarían en la ejecución futura: AGENTS.md únicamente si una regla corta de operación necesita referencia persistente..
- Ubicación exacta de cada archivo: dentro de la raíz del repositorio `DiiegoA/Agente_SRE_DevOps_para_respuesta_a_incidentes`, en la ruta indicada; nunca dentro de `Diiegoal/CursoIA` ni `Diiegoal/memory-repo` originales.

### 8. Directory structure
```text
Agente_SRE_DevOps_para_respuesta_a_incidentes/
├── AGENTS.md [FUTURO]
└── docs/
    └── context-operations.md [FUTURO]
```

### 9. Required concepts
- Concepto: lost in the middle; attention dilution; distractors; 50/70/90; Write; Select; Compress; Isolate.
- Explicación necesaria: 3. Pilar 2 — El Contexto.md — «Context rot», «Los tres mecanismos que producen el rot», «Reglas prácticas observadas», «Write», «Select», «Compress», «Isolate», «Ventanas de contexto actuales» y «Tu kit de context engineering». El profesional debe poder explicar qué se aplica, cuándo, cómo y cómo se valida; en P02 además debe distinguir categoría de modo; en P03/P04 debe distinguir persistencia de operación; en P05/P06 debe distinguir prompting fundamental de patrones de ejecución; en P07 debe demostrar la cadena combinada por caso.
- Nivel requerido para ejecutar el paso: suficiente para diseñar y validar la unidad de trabajo con criterio técnico, no para completar la implementación del producto global.

### 10. Commands
```text
find . -maxdepth 3 -type f | sort
# en ejecución futura: usar las herramientas de la categoría de agente elegida en P02
```
- Ubicación desde la que se ejecuta cada comando: raíz del repositorio objetivo en ejecución futura.
- Resultado esperado: El inventario futuro permite seleccionar solo archivos/artefactos necesarios; la operación aplicada se registra junto con evidencia.
- Verificación: el comando futuro debe dejar evidencia reproducible y no contradecir el estado PLANIFICADO de Chat 2.

### 11. Code
```text
operations = ("Write", "Select", "Compress", "Isolate")

def choose_operation(context_load: float, exploration_costly: bool, durable_detail: bool) -> str:
    if durable_detail:
        return "Write"
    if exploration_costly:
        return "Isolate"
    if context_load >= 0.70:
        return "Compress"
    return "Select"
```
- Propósito: Regla orientativa para decidir la operación de contexto; 50/70/90 son heurísticas de M1, no garantías.
- Partes relevantes: entradas, decisión central, salida y condición que permitirá validación posterior.
- Personalización requerida: adaptar nombres/rutas al estado real observado durante la ejecución futura; no asumir archivos o APIs que todavía no existan.

### 12. Action
- Acción concreta que se realizará: Medir ruido/contexto y escoger la operación necesaria.
- Orden de ejecución: diagnosticar rot → Write/Select/Compress/Isolate → conservar findings → validar.
- Entrada utilizada: Estado de sesión y evidencia futura.
- Salida producida: Contexto optimizado y registro de operación.

### 13. Reason
- Por qué se realiza esta acción: Curar contexto es parte del trabajo de ingeniería y evita degradación silenciosa.
- Qué problema resuelve: evita que el artefacto principal se construya sin la evidencia y validación exigidas por M1.
- Por qué corresponde a M1: la fuente asignada al paso contiene el procedimiento, criterio o práctica concreta que se convierte aquí en actividad real sobre el contexto SRE.

### 14. Expected result
- Resultado esperado: Kit operativo con cuatro subcapacidades diferenciadas.
- Estado esperado: `PLANIFICADO` hasta que una ejecución futura produzca evidencia real.
- Evidencia esperada: Contexto optimizado y registro de operación. y los artefactos de validación/test indicados en este paso.
- Memoria incremental del paso: ZIP de memoria acumulativa que se generará cuando este paso sea ejecutado; debe incorporar el estado y la evidencia acumulados hasta este punto y quedar disponible para alimentar el paso siguiente, sin modificar el baseline histórico.

### 15. Evidence
- Evidencia que demuestra el resultado: Contexto optimizado y registro de operación. con registros de decisión, criterios, referencias y verificaciones observables.
- Fuente de la evidencia: 3. Pilar 2 — El Contexto.md; para afirmaciones externas, fuentes registradas en `knowledge/facts/external-research.md` y `knowledge/references/reference-index.md` del staging.
- Cómo se conservará: artefacto versionado en el proyecto futuro más referencia en el ZIP incremental cuando el paso se ejecute; en Chat 2 no se afirma existencia futura como evidencia observada.

### 16. Validation
- Qué se debe verificar: objetivo, dependencias, artefacto de salida, aserciones atómicas, trazabilidad.
- Cómo se verifica: revisión documental + prueba ejecutable futura + evidencia física del artefacto; una afirmación no sustituye a la evidencia.
- Resultado esperado de la validación: los tres TEST_ID del paso y todas sus ASSERTION_ID resultan PASS en la ejecución futura; en Chat 2 permanecen `PLANIFICADA`.

### 17. Acceptance criteria
- Criterio 1: Write/Select son curación.
- Criterio 2: Compress conserva estado.
- Criterio 3: Isolate devuelve findings compactos..

### 18. Tests
- **ID de prueba:** `P04-T01`
  - **Capacidad/subcapacidad cubierta:** `P04-S01`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P04-A01`
    - **SUBCAP_ID:** `P04-S01`
    - **Qué se observa:** Write mueve detalle fuera del contexto y deja referencia recuperable.
    - **Entrada:** Informe intermedio.
    - **Resultado esperado:** Path/resumen.
    - **Condición de aprobación:** PASS si se conserva la capacidad de recuperar el detalle sin copiarlo.
    - **Condición FAIL:** el detalle no puede recuperarse mediante una referencia estable o permanece copiado innecesariamente.
    - **Evidencia:** Write record.
- **ID de prueba:** `P04-T02`
  - **Capacidad/subcapacidad cubierta:** `P04-S02`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P04-A02`
    - **SUBCAP_ID:** `P04-S02`
    - **Qué se observa:** Select trae solo elementos relacionados con la pregunta.
    - **Entrada:** Repo documental amplio.
    - **Resultado esperado:** Conjunto mínimo.
    - **Condición de aprobación:** PASS si cada selección se justifica por la tarea; FAIL si es 'por si acaso'.
    - **Condición FAIL:** la selección incorpora elementos sin relación justificable con la tarea.
    - **Evidencia:** Selection log.
- **ID de prueba:** `P04-T03`
  - **Capacidad/subcapacidad cubierta:** `P04-S03`, `P04-S04`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P04-A03`
    - **SUBCAP_ID:** `P04-S03`
    - **Qué se observa:** Compress conserva decisiones y estado al reducir volumen.
    - **Entrada:** Historial largo.
    - **Resultado esperado:** Resumen compacto.
    - **Condición de aprobación:** PASS si no se pierde una decisión/estado requerido.
    - **Condición FAIL:** el resumen pierde una decisión, estado o siguiente acción requerida.
    - **Evidencia:** Compressed state.
  - **ASSERTION_ID:** `P04-A04`
    - **SUBCAP_ID:** `P04-S04`
    - **Qué se observa:** Isolate devuelve findings y no transcript verboso.
    - **Entrada:** Subtarea costosa.
    - **Resultado esperado:** Findings compactos.
    - **Condición de aprobación:** PASS si el hilo principal recibe solo hallazgos accionables.
    - **Condición FAIL:** el subagente devuelve transcript verboso/no accionable en vez de findings.
    - **Evidencia:** Isolated findings.

### 19. Expected errors
- Error plausible: P04-E01: el contexto se acumula tras el umbral heurístico y produce repetición, pérdida de coherencia o ruido.
- Cuándo podría aparecer: durante la ejecución futura cuando se salte el criterio previo correspondiente.
- Síntoma: el contexto se acumula tras el umbral heurístico y produce repetición, pérdida de coherencia o ruido.
- Error plausible adicional: P04-E02: Select/Isolate devuelve material no relacionado o transcript verboso.
- Cuándo podría aparecer: durante la ejecución futura al cerrar la unidad sin comprobar la segunda cadena de validación.
- Síntoma adicional: Select/Isolate devuelve material no relacionado o transcript verboso.

### 20. Detection
- Cómo detectar el error: P04-E01: observar crecimiento de contexto, repeticiones, pérdida de instrucciones y necesidad de reexplicar.
- Cómo detectar el error adicional: P04-E02: comparar cada elemento devuelto con la subtarea y contar contenido no accionable.
- Evidencia del error: la ASSERTION_ID correspondiente queda FAIL o no puede emitir un veredicto observable.
- Señal observable: discrepancia entre entrada, resultado esperado y condición PASS/FAIL del paquete de pruebas.

### 21. Meaning
- Qué significa el error o resultado: P04-E01: existe señal de context rot y hace falta una operación explícita de gestión.
- Qué significa el error adicional: P04-E02: la política de selección/aislamiento no está manteniendo la densidad de señal.
- Qué parte del proceso afecta: la unidad profesional de este paso y las salidas que consume cualquier paso dependiente.

### 22. Diagnosis
- Causa probable: P04-E01: decidir entre Write, Compress, nueva sesión o Select según qué información siga siendo necesaria.
- Evidencia que confirma o descarta la causa: P04-E01: observar crecimiento de contexto, repeticiones, pérdida de instrucciones y necesidad de reexplicar. + revisión de la ASSERTION_ID asociada y del artefacto de salida.
- Orden de diagnóstico: P04-E01: decidir entre Write, Compress, nueva sesión o Select según qué información siga siendo necesaria. → comprobar la segunda aserción afectada → comparar con la fuente M1 exacta.
- Causa probable adicional: P04-E02: identificar por qué entró cada pieza y si la exploración debió aislarse.
- Evidencia adicional: P04-E02: comparar cada elemento devuelto con la subtarea y contar contenido no accionable.
- Orden alternativo cuando aplique: verificar dependencia → artefacto → validación → trazabilidad.

### 23. Correction
- Corrección: P04-E01: comprimir o reiniciar manteniendo decisiones/estado requeridos.
- Acción concreta: P04-E01: comprimir o reiniciar manteniendo decisiones/estado requeridos. Después, revisar que la corrección no introduzca una nueva dependencia artificial.
- Verificación posterior: ejecutar nuevamente las ASSERTION_ID afectadas y confirmar evidencia nueva.
- Riesgos de la corrección: alterar una frontera de paso o una dependencia sin reauditar cobertura, profundidad e integridad.
- Corrección adicional: P04-E02: reseleccionar el conjunto mínimo o devolver findings compactos desde el subagente.

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
- M1 → archivo → sección/tema → concepto: 3. Pilar 2 — El Contexto.md — «Context rot», «Los tres mecanismos que producen el rot», «Reglas prácticas observadas», «Write», «Select», «Compress», «Isolate», «Ventanas de contexto actuales» y «Tu kit de context engineering».
- Concepto → actividad: lost in the middle; attention dilution; distractors; 50/70/90; Write; Select; Compress; Isolate → Medir ruido/contexto y escoger la operación necesaria.
- Actividad → paso: la actividad es propietaria de las subcapacidades registradas como P04-S01, P04-S02, P04-S03, P04-S04.
- Paso → artefacto: Contexto optimizado y registro de operación.
- Paso → evidencia: documental/futura; no observada en la ejecución de Chat 2 salvo las fuentes de análisis que se citan como leídas.
- Paso → validación: tres paquetes de test con aserciones atómicas; ver campo 18.
- Paso → memoria ZIP incremental: se generará al ejecutar el paso; en Chat 2 solo se prepara el contrato.
- Paso → siguiente paso: Depende de P03 para saber qué debe persistir; P04 alimenta P05/P06 con contexto curado cuando existe una tarea larga.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: investigación externa consultada el 2026-10-06; se conservan URLs y alcance en `transcript.md` Family 6 y `knowledge/facts/external-research.md`.

### 26. State
- Estado inicial: `PLANIFICADO`.
- Estado final esperado: resultado de la unidad validado y listo para alimentar la dependencia real siguiente.
- Estado real: no ejecutado durante Chat 2; esta afirmación es intencional y protege contra confundir planificación con ejecución.
- Qué queda pendiente: ejecución futura de los artefactos, comandos, pruebas y correcciones; además de reauditar cualquier cambio de frontera.
- Relación con el siguiente paso: Depende de P03 para saber qué debe persistir; P04 alimenta P05/P06 con contexto curado cuando existe una tarea larga.


---

## Paso 05 — Diseñar prompting técnico orientado a outcome

### 1. Identification
- ID del paso: `M1-P05`
- Fase: Fase 3 — Prompt engineering
- Subfase: Subfase 3.1 — Prompt técnico y criterios de éxito
- Estado: `PLANIFICADO`
- Tipo de paso: Unidad de diseño y preparación profesional basada en M1; no ejecuta el proyecto externo.

### 2. Objective
- Objetivo exacto del paso: Definir prompts técnicos cortos, outcome-oriented y verificables, con restricciones y referencias, evitando vaguedad y duplicación de contexto.

### 3. Direct relation to M1
- Archivo(s) de M1: 4. Pilar 3 — El Prompt + Integración.md; 5. Recursos adicionales.md
- Sección(es)/tema(s): 4. Pilar 3 — El Prompt + Integración.md — «Qué del prompt engineering clásico sigue vigente», «La anatomía de un prompt técnico 2026», «Anti-patterns documentados», «Investigación reciente sobre prompting con razonadores» y «Tu kit de prompting».
- Concepto(s) de M1: outcome; success criteria; constraints; references; output format; clarification; 0-shot/few-shot
- Relación directa: El paso transforma estos contenidos en una unidad de trabajo verificable para el proyecto SRE/DevOps, sin adelantar capacidades reservadas a otros módulos.

### 4. Prerequisites
- Conocimientos previos: Tarea caracterizada y contexto disponible.
- Condiciones previas: No se ejecutarán prompts sobre el target en Chat2.
- Evidencia o artefactos necesarios: 4. Pilar 3 — El Prompt + Integración.md; además, las decisiones heredadas de Chat 1 sobre orden, M12, seguridad, read-only-first, PostgreSQL/pgvector y Streamlit deben permanecer disponibles como estado de contexto.

### 5. Dependencies
- Depende de: M1-P01, M1-P03 y M1-P04 cuando la tarea y contexto ya estén definidos.
- Habilita: Guía y prompts versionados orientados a outcome.
- Tipo de dependencia: Dependencia de outcome y contexto disponible.
- Riesgo si se altera el orden: Promptear antes de saber qué información debe estar disponible produce instrucciones redundantes.

### 6. Preparation
- Preparación necesaria: Elegir dos tareas del proyecto y redactar primero prompts cortos orientados a outcome; comprobar qué parte ya está en AGENTS.md antes de copiarla.
- Entorno: copia de trabajo futura del repositorio objetivo; el proyecto real permanece intacto durante Chat 2.
- Información que debe estar disponible: Tarea + contexto + restricciones.; fuentes exactas de M1 y las decisiones heredadas relevantes.

### 7. Files
- Archivos que se leerán: 4. Pilar 3 — El Prompt + Integración.md.
- Archivos que se crearán en la ejecución futura: docs/prompting-guidelines.md; docs/prompts/.
- Archivos que se modificarían en la ejecución futura: AGENTS.md solo para enlaces estables; no se modifica en Chat 2..
- Ubicación exacta de cada archivo: dentro de la raíz del repositorio `DiiegoA/Agente_SRE_DevOps_para_respuesta_a_incidentes`, en la ruta indicada; nunca dentro de `Diiegoal/CursoIA` ni `Diiegoal/memory-repo` originales.

### 8. Directory structure
```text
Agente_SRE_DevOps_para_respuesta_a_incidentes/
├── AGENTS.md [FUTURO]
├── docs/
│   ├── prompting-guidelines.md [FUTURO]
│   └── prompts/ [FUTURO]

```

### 9. Required concepts
- Concepto: outcome; success criteria; constraints; references; output format; clarification; 0-shot/few-shot.
- Explicación necesaria: 4. Pilar 3 — El Prompt + Integración.md — «Qué del prompt engineering clásico sigue vigente», «La anatomía de un prompt técnico 2026», «Anti-patterns documentados», «Investigación reciente sobre prompting con razonadores» y «Tu kit de prompting». El profesional debe poder explicar qué se aplica, cuándo, cómo y cómo se valida; en P02 además debe distinguir categoría de modo; en P03/P04 debe distinguir persistencia de operación; en P05/P06 debe distinguir prompting fundamental de patrones de ejecución; en P07 debe demostrar la cadena combinada por caso.
- Nivel requerido para ejecutar el paso: suficiente para diseñar y validar la unidad de trabajo con criterio técnico, no para completar la implementación del producto global.

### 10. Commands
```text
find docs/prompts -maxdepth 2 -type f | sort
# validación futura de referencias y delimitadores del prompt
```
- Ubicación desde la que se ejecuta cada comando: raíz del repositorio objetivo en ejecución futura.
- Resultado esperado: Las versiones de prompt quedan localizables y cada referencia apunta a una fuente persistente concreta.
- Verificación: el comando futuro debe dejar evidencia reproducible y no contradecir el estado PLANIFICADO de Chat 2.

### 11. Code
```text
prompt = {
    "objective": "outcome concreto",
    "success_criteria": ["criterio observable 1", "criterio observable 2"],
    "constraints": ["restricción necesaria"],
    "references": ["AGENTS.md", "docs/..."],
    "clarification": "pregunta antes de implementar si falta información",
}
```
- Propósito: Ejemplo futuro de estructura de prompt técnico; no es un prompt ejecutado ni un artefacto real del proyecto.
- Partes relevantes: entradas, decisión central, salida y condición que permitirá validación posterior.
- Personalización requerida: adaptar nombres/rutas al estado real observado durante la ejecución futura; no asumir archivos o APIs que todavía no existan.

### 12. Action
- Acción concreta que se realizará: Redactar/validar prompts y elegir 0-shot vs few-shot.
- Orden de ejecución: outcome → éxito → restricciones → referencias → formato/clarificación → revisión.
- Entrada utilizada: Tarea + contexto + restricciones.
- Salida producida: Prompt versionado y guía.

### 13. Reason
- Por qué se realiza esta acción: El prompt es interfaz operacional entre intención y ejecución agentic.
- Qué problema resuelve: evita que el artefacto principal se construya sin la evidencia y validación exigidas por M1.
- Por qué corresponde a M1: la fuente asignada al paso contiene el procedimiento, criterio o práctica concreta que se convierte aquí en actividad real sobre el contexto SRE.

### 14. Expected result
- Resultado esperado: Prompts que permiten PASS/FAIL observable.
- Estado esperado: `PLANIFICADO` hasta que una ejecución futura produzca evidencia real.
- Evidencia esperada: Prompt versionado y guía. y los artefactos de validación/test indicados en este paso.
- Memoria incremental del paso: ZIP de memoria acumulativa que se generará cuando este paso sea ejecutado; debe incorporar el estado y la evidencia acumulados hasta este punto y quedar disponible para alimentar el paso siguiente, sin modificar el baseline histórico.

### 15. Evidence
- Evidencia que demuestra el resultado: Prompt versionado y guía. con registros de decisión, criterios, referencias y verificaciones observables.
- Fuente de la evidencia: 4. Pilar 3 — El Prompt + Integración.md; 5. Recursos adicionales.md; para afirmaciones externas, fuentes registradas en `knowledge/facts/external-research.md` y `knowledge/references/reference-index.md` del staging.
- Cómo se conservará: artefacto versionado en el proyecto futuro más referencia en el ZIP incremental cuando el paso se ejecute; en Chat 2 no se afirma existencia futura como evidencia observada.

### 16. Validation
- Qué se debe verificar: objetivo, dependencias, artefacto de salida, aserciones atómicas, trazabilidad.
- Cómo se verifica: revisión documental + prueba ejecutable futura + evidencia física del artefacto; una afirmación no sustituye a la evidencia.
- Resultado esperado de la validación: los tres TEST_ID del paso y todas sus ASSERTION_ID resultan PASS en la ejecución futura; en Chat 2 permanecen `PLANIFICADA`.

### 17. Acceptance criteria
- Criterio 1: Outcome/éxito.
- Criterio 2: restricciones y referencias.
- Criterio 3: ausencia de redundancia..

### 18. Tests
- **ID de prueba:** `P05-T01`
  - **Capacidad/subcapacidad cubierta:** `P05-S01`, `P05-S02`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P05-A01`
    - **SUBCAP_ID:** `P05-S01`
    - **Qué se observa:** El prompt contiene objetivo/outcome y contexto solo cuando aporta señal.
    - **Entrada:** Prompt feature.
    - **Resultado esperado:** Prompt versionado.
    - **Condición de aprobación:** PASS si el objetivo es inequívoco.
    - **Condición FAIL:** el prompt no permite identificar inequívocamente el outcome.
    - **Evidencia:** Prompt file.
  - **ASSERTION_ID:** `P05-A02`
    - **SUBCAP_ID:** `P05-S02`
    - **Qué se observa:** Los criterios de éxito son observables.
    - **Entrada:** Prompt debugging.
    - **Resultado esperado:** PASS/FAIL futuro.
    - **Condición de aprobación:** PASS si otro lector puede validar el resultado.
    - **Condición FAIL:** un tercero no puede decidir PASS/FAIL con el criterio escrito.
    - **Evidencia:** Prompt review.
- **ID de prueba:** `P05-T02`
  - **Capacidad/subcapacidad cubierta:** `P05-S03`, `P05-S04`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P05-A03`
    - **SUBCAP_ID:** `P05-S03`
    - **Qué se observa:** Las restricciones limitan soluciones incorrectas sin micro-especificar.
    - **Entrada:** Prompt con dos restricciones.
    - **Resultado esperado:** Constraints claras.
    - **Condición de aprobación:** PASS si la restricción es concreta y no repite policy persistente.
    - **Condición FAIL:** la restricción es vaga, contradictoria o micro-especifica una solución.
    - **Evidencia:** Prompt review.
  - **ASSERTION_ID:** `P05-A04`
    - **SUBCAP_ID:** `P05-S04`
    - **Qué se observa:** Las referencias apuntan a fuentes y la ambigüedad activa clarificación.
    - **Entrada:** Prompt ambiguo.
    - **Resultado esperado:** Pregunta de aclaración y paths concretos.
    - **Condición de aprobación:** PASS si no se inventa información faltante.
    - **Condición FAIL:** se inventa información faltante o la referencia no es localizable.
    - **Evidencia:** Prompt trace.
- **ID de prueba:** `P05-T03`
  - **Capacidad/subcapacidad cubierta:** `P05-S05`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P05-A05`
    - **SUBCAP_ID:** `P05-S05`
    - **Qué se observa:** 0-shot se prueba antes de añadir ejemplos few-shot.
    - **Entrada:** Dos variantes.
    - **Resultado esperado:** Selección justificada.
    - **Condición de aprobación:** PASS si el ejemplo añade señal real o se elimina.
    - **Condición FAIL:** los ejemplos se conservan sin aportar señal observable frente a 0-shot.
    - **Evidencia:** Comparison.

### 19. Expected errors
- Error plausible: P05-E01: no hay criterios de éxito observables.
- Cuándo podría aparecer: durante la ejecución futura cuando se salte el criterio previo correspondiente.
- Síntoma: no hay criterios de éxito observables.
- Error plausible adicional: P05-E02: megaprompt con duplicación de contexto o micro-especificación.
- Cuándo podría aparecer: durante la ejecución futura al cerrar la unidad sin comprobar la segunda cadena de validación.
- Síntoma adicional: megaprompt con duplicación de contexto o micro-especificación.

### 20. Detection
- Cómo detectar el error: P05-E01: intentar cerrar la tarea con la información del prompt y comprobar si un tercero puede decidir PASS/FAIL.
- Cómo detectar el error adicional: P05-E02: contrastar el prompt con AGENTS.md y docs referenciados para localizar duplicación y pasos innecesarios.
- Evidencia del error: la ASSERTION_ID correspondiente queda FAIL o no puede emitir un veredicto observable.
- Señal observable: discrepancia entre entrada, resultado esperado y condición PASS/FAIL del paquete de pruebas.

### 21. Meaning
- Qué significa el error o resultado: P05-E01: el prompt no funciona como contrato de resultado.
- Qué significa el error adicional: P05-E02: se desperdicia contexto y se reduce la flexibilidad del razonador.
- Qué parte del proceso afecta: la unidad profesional de este paso y las salidas que consume cualquier paso dependiente.

### 22. Diagnosis
- Causa probable: P05-E01: separar outcome, criterios y restricciones y localizar el punto de vaguedad.
- Evidencia que confirma o descarta la causa: P05-E01: intentar cerrar la tarea con la información del prompt y comprobar si un tercero puede decidir PASS/FAIL. + revisión de la ASSERTION_ID asociada y del artefacto de salida.
- Orden de diagnóstico: P05-E01: separar outcome, criterios y restricciones y localizar el punto de vaguedad. → comprobar la segunda aserción afectada → comparar con la fuente M1 exacta.
- Causa probable adicional: P05-E02: distinguir contexto persistente de prompt de tarea y eliminar instrucciones micro-operativas no necesarias.
- Evidencia adicional: P05-E02: contrastar el prompt con AGENTS.md y docs referenciados para localizar duplicación y pasos innecesarios.
- Orden alternativo cuando aplique: verificar dependencia → artefacto → validación → trazabilidad.

### 23. Correction
- Corrección: P05-E01: reescribir los criterios como observables y trazarlos a evidencia futura.
- Acción concreta: P05-E01: reescribir los criterios como observables y trazarlos a evidencia futura. Después, revisar que la corrección no introduzca una nueva dependencia artificial.
- Verificación posterior: ejecutar nuevamente las ASSERTION_ID afectadas y confirmar evidencia nueva.
- Riesgos de la corrección: alterar una frontera de paso o una dependencia sin reauditar cobertura, profundidad e integridad.
- Corrección adicional: P05-E02: sustituir contenido repetido por referencias y conservar solo restricciones que aportan control.

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
- M1 → archivo → sección/tema → concepto: 4. Pilar 3 — El Prompt + Integración.md — «Qué del prompt engineering clásico sigue vigente», «La anatomía de un prompt técnico 2026», «Anti-patterns documentados», «Investigación reciente sobre prompting con razonadores» y «Tu kit de prompting».
- Concepto → actividad: outcome; success criteria; constraints; references; output format; clarification; 0-shot/few-shot → Redactar/validar prompts y elegir 0-shot vs few-shot.
- Actividad → paso: la actividad es propietaria de las subcapacidades registradas como P05-S01, P05-S02, P05-S03, P05-S04, P05-S05.
- Paso → artefacto: Prompt versionado y guía.
- Paso → evidencia: documental/futura; no observada en la ejecución de Chat 2 salvo las fuentes de análisis que se citan como leídas.
- Paso → validación: tres paquetes de test con aserciones atómicas; ver campo 18.
- Paso → memoria ZIP incremental: se generará al ejecutar el paso; en Chat 2 solo se prepara el contrato.
- Paso → siguiente paso: Consume caracterización y política de contexto; su salida habilita P06 y se aplica en P07.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: investigación externa consultada el 2026-10-06; se conservan URLs y alcance en `transcript.md` Family 6 y `knowledge/facts/external-research.md`.

### 26. State
- Estado inicial: `PLANIFICADO`.
- Estado final esperado: resultado de la unidad validado y listo para alimentar la dependencia real siguiente.
- Estado real: no ejecutado durante Chat 2; esta afirmación es intencional y protege contra confundir planificación con ejecución.
- Qué queda pendiente: ejecución futura de los artefactos, comandos, pruebas y correcciones; además de reauditar cualquier cambio de frontera.
- Relación con el siguiente paso: Consume caracterización y política de contexto; su salida habilita P06 y se aplica en P07.


---

## Paso 06 — Aplicar los cinco patrones de ejecución de coding

### 1. Identification
- ID del paso: `M1-P06`
- Fase: Fase 3 — Prompt engineering
- Subfase: Subfase 3.2 — Patrones de ejecución
- Estado: `PLANIFICADO`
- Tipo de paso: Unidad de diseño y preparación profesional basada en M1; no ejecuta el proyecto externo.

### 2. Objective
- Objetivo exacto del paso: Convertir Spec-driven, Plan-then-execute, Test-first, Refactor con anclas y Critic loops en un playbook ejecutable y validable.

### 3. Direct relation to M1
- Archivo(s) de M1: 4. Pilar 3 — El Prompt + Integración.md
- Sección(es)/tema(s): 4. Pilar 3 — El Prompt + Integración.md — «Patrones específicos de coding» (Spec-driven, Plan-then-execute, Test-first, Refactor con anclas, Critic loops).
- Concepto(s) de M1: Spec-driven preview; Plan-then-execute; Test-first; Refactor con anclas; Critic loops
- Relación directa: El paso transforma estos contenidos en una unidad de trabajo verificable para el proyecto SRE/DevOps, sin adelantar capacidades reservadas a otros módulos.

### 4. Prerequisites
- Conocimientos previos: Prompting y contexto preparados.
- Condiciones previas: No se ejecutan patrones sobre el target en Chat2.
- Evidencia o artefactos necesarios: 4. Pilar 3 — El Prompt + Integración.md; además, las decisiones heredadas de Chat 1 sobre orden, M12, seguridad, read-only-first, PostgreSQL/pgvector y Streamlit deben permanecer disponibles como estado de contexto.

### 5. Dependencies
- Depende de: M1-P05; P03/P04 se consumen cuando el patrón necesita contexto controlado.
- Habilita: Playbook de cinco patrones y criterios de selección.
- Tipo de dependencia: Dependencia metodológica de prompting.
- Riesgo si se altera el orden: Sin criterios de éxito, los patrones no pueden cerrar con evidencia.

### 6. Preparation
- Preparación necesaria: Preparar una matriz patrón↔tarea que conserve para cada patrón cuándo usarlo, cuándo no, secuencia, entrada, salida, aceptación y error plausible.
- Entorno: copia de trabajo futura del repositorio objetivo; el proyecto real permanece intacto durante Chat 2.
- Información que debe estar disponible: Tarea + prompt + contexto.; fuentes exactas de M1 y las decisiones heredadas relevantes.

### 7. Files
- Archivos que se leerán: 4. Pilar 3 — El Prompt + Integración.md.
- Archivos que se crearán en la ejecución futura: docs/agent-execution-patterns.md.
- Archivos que se modificarían en la ejecución futura: AGENTS.md solo para enlazar el playbook futuro..
- Ubicación exacta de cada archivo: dentro de la raíz del repositorio `DiiegoA/Agente_SRE_DevOps_para_respuesta_a_incidentes`, en la ruta indicada; nunca dentro de `Diiegoal/CursoIA` ni `Diiegoal/memory-repo` originales.

### 8. Directory structure
```text
Agente_SRE_DevOps_para_respuesta_a_incidentes/
├── AGENTS.md [FUTURO]
└── docs/
    └── agent-execution-patterns.md [FUTURO]
```

### 9. Required concepts
- Concepto: Spec-driven preview; Plan-then-execute; Test-first; Refactor con anclas; Critic loops.
- Explicación necesaria: 4. Pilar 3 — El Prompt + Integración.md — «Patrones específicos de coding» (Spec-driven, Plan-then-execute, Test-first, Refactor con anclas, Critic loops). El profesional debe poder explicar qué se aplica, cuándo, cómo y cómo se valida; en P02 además debe distinguir categoría de modo; en P03/P04 debe distinguir persistencia de operación; en P05/P06 debe distinguir prompting fundamental de patrones de ejecución; en P07 debe demostrar la cadena combinada por caso.
- Nivel requerido para ejecutar el paso: suficiente para diseñar y validar la unidad de trabajo con criterio técnico, no para completar la implementación del producto global.

### 10. Commands
```text
python - <<'PY'
from pathlib import Path
text = Path("docs/agent-execution-patterns.md").read_text(encoding="utf-8")
required = ["Spec-driven", "Plan-then-execute", "Test-first", "Refactor con anclas", "Critic loops"]
assert all(item in text for item in required)
PY
# validación futura del playbook, no ejecutada en Chat 2.
```
- Ubicación desde la que se ejecuta cada comando: raíz del repositorio objetivo en ejecución futura.
- Resultado esperado: La ejecución futura no debe mutar estado durante Spec/Plan y debe dejar artefactos que puedan ser revisados antes de ejecutar.
- Verificación: el comando futuro debe dejar evidencia reproducible y no contradecir el estado PLANIFICADO de Chat 2.

### 11. Code
```text
PATTERNS = {
    "spec_driven": "definir alcance/inputs/outputs antes de implementar",
    "plan_then_execute": "planificar sin mutar y revisar antes de ejecutar",
    "test_first": "definir pruebas antes del cambio",
    "refactor_with_anchors": "mapa + anclas + bloques reversibles",
    "critic_loops": "revisión independiente + corrección verificable",
}
```
- Propósito: Representar el inventario de patrones que se desarrollará en el playbook; no ejecutado en Chat 2.
- Partes relevantes: entradas, decisión central, salida y condición que permitirá validación posterior.
- Personalización requerida: adaptar nombres/rutas al estado real observado durante la ejecución futura; no asumir archivos o APIs que todavía no existan.

### 12. Action
- Acción concreta que se realizará: Seleccionar y documentar el patrón adecuado por tarea.
- Orden de ejecución: seleccionar patrón → ejecutar estructura → revisar → validar → corregir/repetir.
- Entrada utilizada: Tarea + prompt + contexto.
- Salida producida: Playbook y evidencia futura.

### 13. Reason
- Por qué se realiza esta acción: Los patrones convierten el coding asistido en un workflow controlado, no en un turno único.
- Qué problema resuelve: evita que el artefacto principal se construya sin la evidencia y validación exigidas por M1.
- Por qué corresponde a M1: la fuente asignada al paso contiene el procedimiento, criterio o práctica concreta que se convierte aquí en actividad real sobre el contexto SRE.

### 14. Expected result
- Resultado esperado: Cinco subcapacidades con tests independientes.
- Estado esperado: `PLANIFICADO` hasta que una ejecución futura produzca evidencia real.
- Evidencia esperada: Playbook y evidencia futura. y los artefactos de validación/test indicados en este paso.
- Memoria incremental del paso: ZIP de memoria acumulativa que se generará cuando este paso sea ejecutado; debe incorporar el estado y la evidencia acumulados hasta este punto y quedar disponible para alimentar el paso siguiente, sin modificar el baseline histórico.

### 15. Evidence
- Evidencia que demuestra el resultado: Playbook y evidencia futura. con registros de decisión, criterios, referencias y verificaciones observables.
- Fuente de la evidencia: 4. Pilar 3 — El Prompt + Integración.md; para afirmaciones externas, fuentes registradas en `knowledge/facts/external-research.md` y `knowledge/references/reference-index.md` del staging.
- Cómo se conservará: artefacto versionado en el proyecto futuro más referencia en el ZIP incremental cuando el paso se ejecute; en Chat 2 no se afirma existencia futura como evidencia observada.

### 16. Validation
- Qué se debe verificar: objetivo, dependencias, artefacto de salida, aserciones atómicas, trazabilidad.
- Cómo se verifica: revisión documental + prueba ejecutable futura + evidencia física del artefacto; una afirmación no sustituye a la evidencia.
- Resultado esperado de la validación: los tres TEST_ID del paso y todas sus ASSERTION_ID resultan PASS en la ejecución futura; en Chat 2 permanecen `PLANIFICADA`.

### 17. Acceptance criteria
- Criterio 1: cinco patrones identificados.
- Criterio 2: diferencias preservadas.
- Criterio 3: cada patrón validable..

### 18. Tests
- **ID de prueba:** `P06-T01`
  - **Capacidad/subcapacidad cubierta:** `P06-S01`, `P06-S02`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P06-A01`
    - **SUBCAP_ID:** `P06-S01`
    - **Qué se observa:** Spec-driven produce una especificación revisable sin implementar.
    - **Entrada:** Task future.
    - **Resultado esperado:** Spec.
    - **Condición de aprobación:** PASS si la spec expresa alcance/éxito antes de código.
    - **Condición FAIL:** la implementación aparece antes de una spec revisable.
    - **Evidencia:** Spec file.
  - **ASSERTION_ID:** `P06-A02`
    - **SUBCAP_ID:** `P06-S02`
    - **Qué se observa:** Plan-then-execute no muta estado durante planificación.
    - **Entrada:** Task future.
    - **Resultado esperado:** Plan + approval state.
    - **Condición de aprobación:** PASS si el plan es read-only y la ejecución comienza después de revisión.
    - **Condición FAIL:** la fase de planificación muta estado o se ejecuta sin revisión humana.
    - **Evidencia:** Plan log.
- **ID de prueba:** `P06-T02`
  - **Capacidad/subcapacidad cubierta:** `P06-S03`, `P06-S04`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P06-A03`
    - **SUBCAP_ID:** `P06-S03`
    - **Qué se observa:** Test-first define comprobaciones antes del cambio.
    - **Entrada:** Success criteria.
    - **Resultado esperado:** Test set.
    - **Condición de aprobación:** PASS si los tests/criteria preceden implementación.
    - **Condición FAIL:** las comprobaciones no existen antes del cambio.
    - **Evidencia:** Test artifacts.
  - **ASSERTION_ID:** `P06-A04`
    - **SUBCAP_ID:** `P06-S04`
    - **Qué se observa:** Refactor con anclas identifica símbolos/dependencias y usa bloques reversibles.
    - **Entrada:** Code map future.
    - **Resultado esperado:** Anchors/checkpoints.
    - **Condición de aprobación:** PASS si no existe cambio monolítico sin anclas.
    - **Condición FAIL:** el cambio carece de anclas, bloques reversibles o puntos de control.
    - **Evidencia:** Refactor plan.
- **ID de prueba:** `P06-T03`
  - **Capacidad/subcapacidad cubierta:** `P06-S05`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P06-A05`
    - **SUBCAP_ID:** `P06-S05`
    - **Qué se observa:** Critic loop produce revisión independiente y correcciones verificables.
    - **Entrada:** Output future.
    - **Resultado esperado:** Findings + resolution.
    - **Condición de aprobación:** PASS si el critic tiene criterio de cierre y acción posterior.
    - **Condición FAIL:** la revisión independiente no produce criterio de cierre y resolución verificable.
    - **Evidencia:** Review record.

### 19. Expected errors
- Error plausible: P06-E01: la planificación cambia estado antes de revisión/aprobación.
- Cuándo podría aparecer: durante la ejecución futura cuando se salte el criterio previo correspondiente.
- Síntoma: la planificación cambia estado antes de revisión/aprobación.
- Error plausible adicional: P06-E02: refactor/ejecución monolítica sin anclas o critic sin criterio de cierre.
- Cuándo podría aparecer: durante la ejecución futura al cerrar la unidad sin comprobar la segunda cadena de validación.
- Síntoma adicional: refactor/ejecución monolítica sin anclas o critic sin criterio de cierre.

### 20. Detection
- Cómo detectar el error: P06-E01: revisar diff/estado durante y después de planificar; cualquier mutación es señal inmediata.
- Cómo detectar el error adicional: P06-E02: buscar ausencia de mapa, anclas, checkpoints, commits intermedios o resolución de findings.
- Evidencia del error: la ASSERTION_ID correspondiente queda FAIL o no puede emitir un veredicto observable.
- Señal observable: discrepancia entre entrada, resultado esperado y condición PASS/FAIL del paquete de pruebas.

### 21. Meaning
- Qué significa el error o resultado: P06-E01: se rompió plan → revisión → ejecución.
- Qué significa el error adicional: P06-E02: aumentó el riesgo de regresión y la revisión perdió capacidad preventiva.
- Qué parte del proceso afecta: la unidad profesional de este paso y las salidas que consume cualquier paso dependiente.

### 22. Diagnosis
- Causa probable: P06-E01: inspeccionar orden y evidencia de plan, aprobación y cambio.
- Evidencia que confirma o descarta la causa: P06-E01: revisar diff/estado durante y después de planificar; cualquier mutación es señal inmediata. + revisión de la ASSERTION_ID asociada y del artefacto de salida.
- Orden de diagnóstico: P06-E01: inspeccionar orden y evidencia de plan, aprobación y cambio. → comprobar la segunda aserción afectada → comparar con la fuente M1 exacta.
- Causa probable adicional: P06-E02: identificar el bloque que carece de anchor/checkpoint y el finding no cerrado.
- Evidencia adicional: P06-E02: buscar ausencia de mapa, anclas, checkpoints, commits intermedios o resolución de findings.
- Orden alternativo cuando aplique: verificar dependencia → artefacto → validación → trazabilidad.

### 23. Correction
- Corrección: P06-E01: restaurar desde el último punto válido y rehacer el plan sin mutación.
- Acción concreta: P06-E01: restaurar desde el último punto válido y rehacer el plan sin mutación. Después, revisar que la corrección no introduzca una nueva dependencia artificial.
- Verificación posterior: ejecutar nuevamente las ASSERTION_ID afectadas y confirmar evidencia nueva.
- Riesgos de la corrección: alterar una frontera de paso o una dependencia sin reauditar cobertura, profundidad e integridad.
- Corrección adicional: P06-E02: dividir la ejecución futura en bloques reversibles y añadir critic con cierre explícito.

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
- M1 → archivo → sección/tema → concepto: 4. Pilar 3 — El Prompt + Integración.md — «Patrones específicos de coding» (Spec-driven, Plan-then-execute, Test-first, Refactor con anclas, Critic loops).
- Concepto → actividad: Spec-driven preview; Plan-then-execute; Test-first; Refactor con anclas; Critic loops → Seleccionar y documentar el patrón adecuado por tarea.
- Actividad → paso: la actividad es propietaria de las subcapacidades registradas como P06-S01, P06-S02, P06-S03, P06-S04, P06-S05.
- Paso → artefacto: Playbook y evidencia futura.
- Paso → evidencia: documental/futura; no observada en la ejecución de Chat 2 salvo las fuentes de análisis que se citan como leídas.
- Paso → validación: tres paquetes de test con aserciones atómicas; ver campo 18.
- Paso → memoria ZIP incremental: se generará al ejecutar el paso; en Chat 2 solo se prepara el contrato.
- Paso → siguiente paso: Consume prompts y contexto; sus patrones se aplican en P07 cuando el caso lo requiere.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: investigación externa consultada el 2026-10-06; se conservan URLs y alcance en `transcript.md` Family 6 y `knowledge/facts/external-research.md`.

### 26. State
- Estado inicial: `PLANIFICADO`.
- Estado final esperado: resultado de la unidad validado y listo para alimentar la dependencia real siguiente.
- Estado real: no ejecutado durante Chat 2; esta afirmación es intencional y protege contra confundir planificación con ejecución.
- Qué queda pendiente: ejecución futura de los artefactos, comandos, pruebas y correcciones; además de reauditar cualquier cambio de frontera.
- Relación con el siguiente paso: Consume prompts y contexto; sus patrones se aplican en P07 cuando el caso lo requiere.


---

## Paso 07 — Integrar los tres pilares y validar los cinco casos canónicos

### 1. Identification
- ID del paso: `M1-P07`
- Fase: Fase 4 — Integración y preparación
- Subfase: Subfase 4.1 — Aplicación combinada y readiness
- Estado: `PLANIFICADO`
- Tipo de paso: Unidad de diseño y preparación profesional basada en M1; no ejecuta el proyecto externo.

### 2. Objective
- Objetivo exacto del paso: Aplicar herramienta, contexto, prompt y patrón a A–E y producir un readiness assessment que cierre M1 sin implementar el producto.

### 3. Direct relation to M1
- Archivo(s) de M1: 4. Pilar 3 — El Prompt + Integración.md; 1. El modelo mental de los 3 pilares.md; 5. Recursos adicionales.md
- Sección(es)/tema(s): 4. Pilar 3 — El Prompt + Integración.md — «El framework de decisión combinado», «Casos canónicos A–E», «Anti-patrones combinados» y «El meta-insight de los 3 pilares»; 1. El modelo mental... — «Por qué los tres son co-iguales».
- Concepto(s) de M1: A refactor; B greenfield; C debugging; D exploración; E review; integración completa
- Relación directa: El paso transforma estos contenidos en una unidad de trabajo verificable para el proyecto SRE/DevOps, sin adelantar capacidades reservadas a otros módulos.

### 4. Prerequisites
- Conocimientos previos: Resultados documentales de P01–P06 según cada caso.
- Condiciones previas: P07 es integración futura; no ejecuta el Paso 1 del producto.
- Evidencia o artefactos necesarios: 4. Pilar 3 — El Prompt + Integración.md y outputs de P01–P06.; además, las decisiones heredadas de Chat 1 sobre orden, M12, seguridad, read-only-first, PostgreSQL/pgvector y Streamlit deben permanecer disponibles como estado de contexto.

### 5. Dependencies
- Depende de: M1-P01–P06 según la cadena de cada caso; no se crea dependencia artificial entre casos independientes.
- Habilita: Matriz integrada A–E y readiness de M1.
- Tipo de dependencia: Dependencia transversal por caso.
- Riesgo si se altera el orden: Confundir recopilación con integración eliminaría la validación conjunta.

### 6. Preparation
- Preparación necesaria: Construir registros independientes para A–E y una matriz de integración que compare los siete eslabones sin convertir la integración en simple recopilación.
- Entorno: copia de trabajo futura del repositorio objetivo; el proyecto real permanece intacto durante Chat 2.
- Información que debe estar disponible: Casos A–E y artefactos de P01–P06.; fuentes exactas de M1 y las decisiones heredadas relevantes.

### 7. Files
- Archivos que se leerán: 4. Pilar 3 — El Prompt + Integración.md y outputs de P01–P06..
- Archivos que se crearán en la ejecución futura: docs/m1-operating-model.md; docs/m1-integration.json.
- Archivos que se modificarían en la ejecución futura: AGENTS.md y docs solo en ejecución futura para enlazar readiness..
- Ubicación exacta de cada archivo: dentro de la raíz del repositorio `DiiegoA/Agente_SRE_DevOps_para_respuesta_a_incidentes`, en la ruta indicada; nunca dentro de `Diiegoal/CursoIA` ni `Diiegoal/memory-repo` originales.

### 8. Directory structure
```text
Agente_SRE_DevOps_para_respuesta_a_incidentes/
├── AGENTS.md [FUTURO]
└── docs/
    ├── m1-integration.json [FUTURO]
    └── m1-operating-model.md [FUTURO]
```

### 9. Required concepts
- Concepto: A refactor; B greenfield; C debugging; D exploración; E review; integración completa.
- Explicación necesaria: 4. Pilar 3 — El Prompt + Integración.md — «El framework de decisión combinado», «Casos canónicos A–E», «Anti-patrones combinados» y «El meta-insight de los 3 pilares»; 1. El modelo mental... — «Por qué los tres son co-iguales». El profesional debe poder explicar qué se aplica, cuándo, cómo y cómo se valida; en P02 además debe distinguir categoría de modo; en P03/P04 debe distinguir persistencia de operación; en P05/P06 debe distinguir prompting fundamental de patrones de ejecución; en P07 debe demostrar la cadena combinada por caso.
- Nivel requerido para ejecutar el paso: suficiente para diseñar y validar la unidad de trabajo con criterio técnico, no para completar la implementación del producto global.

### 10. Commands
```text
python -m json.tool docs/m1-integration.json
# validación futura del artefacto integrado, no ejecutada en Chat 2
```
- Ubicación desde la que se ejecuta cada comando: raíz del repositorio objetivo en ejecución futura.
- Resultado esperado: El artefacto integrado permite comprobar cada caso y cualquier contradicción entre decisiones de los pilares.
- Verificación: el comando futuro debe dejar evidencia reproducible y no contradecir el estado PLANIFICADO de Chat 2.

### 11. Code
```text
def integration_record(case, tool, context, prompt, pattern, result, evidence, validation):
    return {
        "case": case, "tool": tool, "context": context,
        "prompt": prompt, "pattern": pattern,
        "result": result, "evidence": evidence,
        "validation": validation,
    }
```
- Propósito: Modelo futuro de registro para la integración A–E; no ejecutado.
- Partes relevantes: entradas, decisión central, salida y condición que permitirá validación posterior.
- Personalización requerida: adaptar nombres/rutas al estado real observado durante la ejecución futura; no asumir archivos o APIs que todavía no existan.

### 12. Action
- Acción concreta que se realizará: Simular A–E, registrar decisiones combinadas y ejecutar readiness.
- Orden de ejecución: caracterizar → tool → context → prompt → patrón → revisar → evidencia → readiness.
- Entrada utilizada: Casos A–E y artefactos de P01–P06.
- Salida producida: Matriz integrada y estado de M1.

### 13. Reason
- Por qué se realiza esta acción: Comprueba que los tres pilares funcionan como sistema, no como listas independientes.
- Qué problema resuelve: evita que el artefacto principal se construya sin la evidencia y validación exigidas por M1.
- Por qué corresponde a M1: la fuente asignada al paso contiene el procedimiento, criterio o práctica concreta que se convierte aquí en actividad real sobre el contexto SRE.

### 14. Expected result
- Resultado esperado: Readiness PASS solo con evidencia suficiente; en Chat2 queda planificado.
- Estado esperado: `PLANIFICADO` hasta que una ejecución futura produzca evidencia real.
- Evidencia esperada: Matriz integrada y estado de M1. y los artefactos de validación/test indicados en este paso.
- Memoria incremental del paso: ZIP de memoria acumulativa que se generará cuando este paso sea ejecutado; debe incorporar el estado y la evidencia acumulados hasta este punto y quedar disponible para alimentar el paso siguiente, sin modificar el baseline histórico.

### 15. Evidence
- Evidencia que demuestra el resultado: Matriz integrada y estado de M1. con registros de decisión, criterios, referencias y verificaciones observables.
- Fuente de la evidencia: 4. Pilar 3 — El Prompt + Integración.md; 1. El modelo mental de los 3 pilares.md; 5. Recursos adicionales.md; para afirmaciones externas, fuentes registradas en `knowledge/facts/external-research.md` y `knowledge/references/reference-index.md` del staging.
- Cómo se conservará: artefacto versionado en el proyecto futuro más referencia en el ZIP incremental cuando el paso se ejecute; en Chat 2 no se afirma existencia futura como evidencia observada.

### 16. Validation
- Qué se debe verificar: objetivo, dependencias, artefacto de salida, aserciones atómicas, trazabilidad.
- Cómo se verifica: revisión documental + prueba ejecutable futura + evidencia física del artefacto; una afirmación no sustituye a la evidencia.
- Resultado esperado de la validación: los tres TEST_ID del paso y todas sus ASSERTION_ID resultan PASS en la ejecución futura; en Chat 2 permanecen `PLANIFICADA`.

### 17. Acceptance criteria
- Criterio 1: A–E completos.
- Criterio 2: integración nueva.
- Criterio 3: readiness trazable..

### 18. Tests
- **ID de prueba:** `P07-T01`
  - **Capacidad/subcapacidad cubierta:** `P07-S01`, `P07-S02`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P07-A01`
    - **SUBCAP_ID:** `P07-S01`
    - **Qué se observa:** Caso A contiene tool, context, prompt, pattern, result, evidence y validation.
    - **Entrada:** Gran refactor.
    - **Resultado esperado:** Case record.
    - **Condición de aprobación:** PASS si los siete eslabones están presentes.
    - **Condición FAIL:** falta algún eslabón de la cadena o el caso se reduce a una lista.
    - **Evidencia:** Case A.
  - **ASSERTION_ID:** `P07-A02`
    - **SUBCAP_ID:** `P07-S02`
    - **Qué se observa:** Caso B contiene la misma cadena adaptada a greenfield.
    - **Entrada:** Feature.
    - **Resultado esperado:** Case record.
    - **Condición de aprobación:** PASS si éxito y contexto están definidos.
    - **Condición FAIL:** el caso no identifica éxito, contexto o herramienta de forma explícita.
    - **Evidencia:** Case B.
- **ID de prueba:** `P07-T02`
  - **Capacidad/subcapacidad cubierta:** `P07-S03`, `P07-S04`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P07-A03`
    - **SUBCAP_ID:** `P07-S03`
    - **Qué se observa:** Caso C limita contexto y exige verificación repetida.
    - **Entrada:** Flaky debugging.
    - **Resultado esperado:** Diagnosis + repeated check.
    - **Condición de aprobación:** PASS si la hipótesis se prueba y el test se repite.
    - **Condición FAIL:** la hipótesis no se prueba o el test no se repite de manera observable.
    - **Evidencia:** Case C.
  - **ASSERTION_ID:** `P07-A04`
    - **SUBCAP_ID:** `P07-S04`
    - **Qué se observa:** Caso D aísla exploración y devuelve mapa compacto.
    - **Entrada:** Repo desconocido.
    - **Resultado esperado:** Repo map + findings.
    - **Condición de aprobación:** PASS si la exploración no contamina el hilo principal.
    - **Condición FAIL:** la exploración se mezcla con el hilo principal o no devuelve mapa compacto.
    - **Evidencia:** Case D.
- **ID de prueba:** `P07-T03`
  - **Capacidad/subcapacidad cubierta:** `P07-S05`, `P07-S06`
  - **Estado de la prueba durante Chat 2:** `PLANIFICADA`
  - **ASSERTION_ID:** `P07-A05`
    - **SUBCAP_ID:** `P07-S05`
    - **Qué se observa:** Caso E revisa diff + contexto persistente con checklist.
    - **Entrada:** PR diff.
    - **Resultado esperado:** Review findings.
    - **Condición de aprobación:** PASS si security/tests/edge cases tienen revisión explícita.
    - **Condición FAIL:** security/tests/edge cases/performance/conventions no quedan revisados explícitamente.
    - **Evidencia:** Case E.
  - **ASSERTION_ID:** `P07-A06`
    - **SUBCAP_ID:** `P07-S06`
    - **Qué se observa:** La integración detecta contradicciones entre casos y decisiones de pilares.
    - **Entrada:** A–E completos.
    - **Resultado esperado:** Readiness matrix.
    - **Condición de aprobación:** PASS si ninguna inconsistencia conocida queda sin registrar.
    - **Condición FAIL:** la integración no produce veredictos nuevos o deja contradicciones sin resolver.
    - **Evidencia:** Integration matrix.

### 19. Expected errors
- Error plausible: P07-E01: la integración solo recopila lo ya producido.
- Cuándo podría aparecer: durante la ejecución futura cuando se salte el criterio previo correspondiente.
- Síntoma: la integración solo recopila lo ya producido.
- Error plausible adicional: P07-E02: un caso A–E carece de una parte de herramienta→contexto→prompt→patrón→resultado→evidencia→validación.
- Cuándo podría aparecer: durante la ejecución futura al cerrar la unidad sin comprobar la segunda cadena de validación.
- Síntoma adicional: un caso A–E carece de una parte de herramienta→contexto→prompt→patrón→resultado→evidencia→validación.

### 20. Detection
- Cómo detectar el error: P07-E01: preguntar qué veredicto nuevo produce la integración que no exista en los pasos propietarios.
- Cómo detectar el error adicional: P07-E02: recorrer cada eslabón por caso y marcar el primer enlace ausente.
- Evidencia del error: la ASSERTION_ID correspondiente queda FAIL o no puede emitir un veredicto observable.
- Señal observable: discrepancia entre entrada, resultado esperado y condición PASS/FAIL del paquete de pruebas.

### 21. Meaning
- Qué significa el error o resultado: P07-E01: sería un paso de consolidación, contrario al contrato.
- Qué significa el error adicional: P07-E02: la cobertura conceptual no está completa aunque el caso tenga un registro nominal.
- Qué parte del proceso afecta: la unidad profesional de este paso y las salidas que consume cualquier paso dependiente.

### 22. Diagnosis
- Causa probable: P07-E01: comparar el artefacto de integración con las salidas de P01–P06.
- Evidencia que confirma o descarta la causa: P07-E01: preguntar qué veredicto nuevo produce la integración que no exista en los pasos propietarios. + revisión de la ASSERTION_ID asociada y del artefacto de salida.
- Orden de diagnóstico: P07-E01: comparar el artefacto de integración con las salidas de P01–P06. → comprobar la segunda aserción afectada → comparar con la fuente M1 exacta.
- Causa probable adicional: P07-E02: localizar si el hueco pertenece al paso propietario o a la aplicación conjunta.
- Evidencia adicional: P07-E02: recorrer cada eslabón por caso y marcar el primer enlace ausente.
- Orden alternativo cuando aplique: verificar dependencia → artefacto → validación → trazabilidad.

### 23. Correction
- Corrección: P07-E01: añadir verificación nueva de coherencia A–E o devolver el contenido a su propietario.
- Acción concreta: P07-E01: añadir verificación nueva de coherencia A–E o devolver el contenido a su propietario. Después, revisar que la corrección no introduzca una nueva dependencia artificial.
- Verificación posterior: ejecutar nuevamente las ASSERTION_ID afectadas y confirmar evidencia nueva.
- Riesgos de la corrección: alterar una frontera de paso o una dependencia sin reauditar cobertura, profundidad e integridad.
- Corrección adicional: P07-E02: completar el eslabón en su paso propietario y luego volver a integrar.

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
- M1 → archivo → sección/tema → concepto: 4. Pilar 3 — El Prompt + Integración.md — «El framework de decisión combinado», «Casos canónicos A–E», «Anti-patrones combinados» y «El meta-insight de los 3 pilares»; 1. El modelo mental... — «Por qué los tres son co-iguales».
- Concepto → actividad: A refactor; B greenfield; C debugging; D exploración; E review; integración completa → Simular A–E, registrar decisiones combinadas y ejecutar readiness.
- Actividad → paso: la actividad es propietaria de las subcapacidades registradas como P07-S01, P07-S02, P07-S03, P07-S04, P07-S05, P07-S06.
- Paso → artefacto: Matriz integrada y estado de M1.
- Paso → evidencia: documental/futura; no observada en la ejecución de Chat 2 salvo las fuentes de análisis que se citan como leídas.
- Paso → validación: tres paquetes de test con aserciones atómicas; ver campo 18.
- Paso → memoria ZIP incremental: se generará al ejecutar el paso; en Chat 2 solo se prepara el contrato.
- Paso → siguiente paso: Usa salidas de los pasos anteriores solo cuando existe dependencia real por caso; la integración añade una validación transversal nueva.
- Fuente externa → fecha de consulta → URL/recurso → afirmación soportada, cuando corresponda: investigación externa consultada el 2026-10-06; se conservan URLs y alcance en `transcript.md` Family 6 y `knowledge/facts/external-research.md`.

### 26. State
- Estado inicial: `PLANIFICADO`.
- Estado final esperado: resultado de la unidad validado y listo para alimentar la dependencia real siguiente.
- Estado real: no ejecutado durante Chat 2; esta afirmación es intencional y protege contra confundir planificación con ejecución.
- Qué queda pendiente: ejecución futura de los artefactos, comandos, pruebas y correcciones; además de reauditar cualquier cambio de frontera.
- Relación con el siguiente paso: Usa salidas de los pasos anteriores solo cuando existe dependencia real por caso; la integración añade una validación transversal nueva.
