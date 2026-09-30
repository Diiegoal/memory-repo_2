# Gates de calidad de la construcción de M1

## Estado de auditoría

El plan de siete pasos de M1 solo se congela después de una auditoría estructural y una auditoría semántica. Los resultados siguientes se registran a nivel de planificación y no significan que el proyecto futuro haya sido ejecutado.

## Resultados de los gates

| Gate | Estado | Evidencia / criterio |
|---|---|---|
| G01 Cobertura de fuente | PASS | Todo el contenido práctico controlado de los tres pilares queda asignado a P01–P07 con archivos y temas concretos de M1. |
| G02 Profundidad semántica | PASS | Las familias agrupadas conservan categorías, variantes, criterios y procedimientos diferenciados; no se usa una etiqueta colectiva como sustituto. |
| G03 Invariante de idioma | PASS | Todo contenido nuevo creado por Chat 2 está en español; nombres técnicos, rutas, archivos, comandos y RAW conservan su forma necesaria. |
| G04 Trazabilidad directa | PASS | Cada paso identifica archivos, temas, capacidad, resultado, evidencia y validación futura. |
| G05 Cobertura de pruebas | PASS | Hay pruebas concretas para categorías A–D, completion/agentic, criterios de herramientas, context rot, Write/Select/Compress/Isolate, cinco patrones de coding y casos A–E. |
| G06 Integridad de 26 campos | PASS | `M1-P01` a `M1-P07` contienen exactamente las 26 secciones obligatorias, en el mismo orden. |
| G07 Estado | PASS | Todos los pasos y todas las pruebas se mantienen `PLANIFICADO`; no se presenta ejecución futura como realizada. |
| G08 Fronteras de paso | PASS | Las siete unidades emergieron de cobertura, profundidad, independencia, anti-compresión, anti-fragmentación, dependencias y validación. |
| G09 Integración | PASS | P07 realiza trabajo aplicado nuevo con A–E y una aplicación SRE, no una mera recopilación. |
| G10 Evidencia externa | PASS | La corroboración externa se mantiene separada de los hechos del repositorio y de las decisiones heredadas. |
| G11 Higiene de contexto | PASS | Contexto persistente, contexto operativo y prompting se tratan como capacidades relacionadas pero distintas. |
| G12 Regresión | PASS | Chat 1 se usa como estado heredado y evidencia de continuidad; no se copia una salida previa como plantilla. |
| G13 Decisiones nuevas | PASS | Chat 2 no crea una nueva decisión sustantiva; `DEC-0001` a `DEC-0006` permanecen sin modificación. |

## Auditoría estructural

- Siete IDs: `M1-P01` a `M1-P07`.
- 26 secciones por paso.
- `Estado: PLANIFICADO` en cada paso.
- Todas las pruebas incluyen ID, capacidad, prueba, entrada, resultado esperado, condición PASS/FAIL y estado PLANIFICADA.
- No existe directorio físico `chat-002/`.
- No existe código o archivo de implementación del proyecto objetivo en la staging de Chat 2.

## Auditoría semántica

Se mantienen separadas: clasificación de tarea frente a selección de herramienta; contexto persistente frente a gestión del contexto activo; prompting fundamental frente a patrones de ejecución de coding. Context rot y Write/Select/Compress/Isolate permanecen agrupados porque comparten el resultado profesional de controlar el contexto activo.

## Anti-compresión

La planilla de cobertura se usa como control, no como sustituto del desarrollo. Las categorías A–D, criterios, variantes, mecanismos y casos canónicos aparecen dentro de los pasos correspondientes.

## Anti-fragmentación

No se crea un paso para cada subtítulo de M1. Tampoco se separan operaciones que solo serían documentación repetida. Una separación solo se conserva cuando representa una unidad profesional distinta.

## Refutación

Se revisaron las fronteras principales y no apareció evidencia posterior que obligara a cambiar las siete unidades estabilizadas.

## Estado final

`PASS — plan congelado para empaquetado.`

Este PASS indica que la documentación de planificación está lista para conservarse en la copia de memoria. No indica que el proyecto objetivo haya ejecutado M1.
