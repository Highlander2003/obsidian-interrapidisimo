---
tipo: sintesis
estado: en-desarrollo
creado: 2026-09-19
actualizado: 2026-09-19
tags: [alcance, comite, contradiccion]
---

# Brecha entre el anteproyecto aprobado y el trabajo vigente

**Pregunta que responde:** en qué se separa el trabajo de grado que hoy existe del
anteproyecto que la facultad aprobó, y qué de esa separación exige autorización.

## Respuesta corta

La separación es de alcance, no de tema. El anteproyecto aprobó una aplicación web validada en
entorno controlado y renunció de forma expresa a demostrar mejoras operativas
([[2026-09-19 Ficha de anteproyecto aprobada]], p. 5-6). El trabajo vigente, siguiendo el
[[2026-09-19 Plan de integracion de correcciones]], rediseña el proceso, amplía a seis los
objetivos y añade evaluación de impacto y viabilidad económica. Seis diferencias son
sustantivas y tres de ellas requieren autorización del comité.

Decisión tomada el 2026-09-19: se mantiene el alcance ampliado y se solicita la modificación
formal. Ver [[Aprobación del comité para la ampliación del alcance]].

## Comparación

| Dimensión | Anteproyecto aprobado | Trabajo vigente | ¿Requiere autorización? |
|---|---|---|---|
| Título | «Aplicación web para coordinadores operativos de despacho de mensajeros…» ([[2026-09-19 Ficha de anteproyecto aprobada]], p. 1) | «Sistema de información para la gestión y trazabilidad del despacho de última milla…» | Sí |
| Pregunta problema | Cómo facilitar un proceso trazable que disminuya errores humanos y reduzca anomalías operativas (p. 3) | Cómo rediseñar el proceso y qué sistema debe soportarlo, incluyendo conciliación, liquidación y viabilidad económica | Sí |
| Objetivo general | Desarrollar una aplicación web con módulos de registro, asignación, seguimiento y administración (p. 3-4) | Rediseñar el proceso, desarrollar el sistema y evaluar calidad, impacto y viabilidad | Sí |
| Objetivos específicos | Tres (p. 4) | Seis (OE1–OE6) | Sí |
| Evaluación de impacto | Excluida: «no busca demostrar mejoras operativas» (p. 5); «sin asumir impactos garantizados» (p. 6) | Capítulo 7 completo: indicadores antes y después, retorno de la inversión, sensibilidad | Sí |
| Validación | Contradictoria dentro de la ficha: pruebas internas del equipo (p. 4-5) frente a pruebas con usuarios reales (p. 25-26) | Pruebas con el coordinador bajo ISO/IEC 25010 | No: amparada en p. 25-26 |
| Rol del mensajero | Aparece como usuario de validación en el cronograma (p. 26) | Actor del proceso, no usuario del sistema | No: es delimitación de diseño, no de alcance |
| Iteraciones | Seis planificadas, 0 a 5 (p. 25-27) | Dos documentadas en el cuerpo, tres en el apéndice preliminar | No, pero exige coherencia |
| Carga de prueba | 5.000 guías (p. 26) | 750 guías | No: es menor exigencia, conviene explicarla |

## Desarrollo

Las tres primeras filas —título, pregunta y objetivo general— son la misma diferencia vista
desde tres ángulos: el anteproyecto compromete **construir una herramienta**, el trabajo
vigente compromete **intervenir un proceso y evaluar la intervención**. Es una ampliación del
objeto de estudio, no un cambio de tema, y esa distinción es la que hace defendible la
solicitud: la sucursal, el problema y el prototipo son los mismos.

La quinta fila es la más delicada y conviene no minimizarla. El anteproyecto no omitió la
evaluación de impacto: **renunció a ella de forma expresa y por escrito, dos veces** (p. 5 y
p. 6). Un capítulo de impacto con retorno de la inversión no llena un vacío del documento
aprobado, contradice una delimitación deliberada. De ahí que baste con justificarlo en el
cuerpo del trabajo solo si el comité autoriza; sin esa autorización, es material para un
reparo en la sustentación. #suposicion

La sexta fila, en cambio, no requiere trámite: la propia ficha autoriza pruebas con usuarios
reales en su metodología y en su cronograma, de modo que reportar la sesión con el coordinador
se ampara en el documento aprobado aunque tensione su tercer objetivo específico.

La octava fila no es una diferencia de alcance sino un problema de coherencia que ya estaba
abierto. Con la ficha hay ahora **tres cifras distintas** para el mismo hecho: seis
iteraciones planificadas (p. 25-27), dos documentadas en el cuerpo del borrador y tres en su
apéndice. Ver [[Número de iteraciones de construcción realizadas]]. #contradiccion

## Límites de esta respuesta

No incluye las correcciones del evaluador que originaron el plan: ese documento no está en
`originales/` y se perdió del directorio de trabajo. Sin él no es posible determinar **cuánto
de la ampliación fue exigido por el evaluador y cuánto fue iniciativa propia**, y esa
distinción es justamente el argumento más fuerte que podría llevarse al comité. #pendiente

Tampoco cubre el cumplimiento del cronograma: la ficha fecha la entrega final el 31 de enero
de 2026 ([[2026-09-19 Ficha de anteproyecto aprobada]], p. 25) y el wiki no tiene evidencia de
qué se cumplió en esas fechas.

## Fuentes usadas

- [[2026-09-19 Ficha de anteproyecto aprobada]]
- [[2026-09-19 Plan de integracion de correcciones]]
