---
tipo: pregunta
estado: en-desarrollo
creado: 2026-09-19
actualizado: 2026-09-19
tags: [P-10, bloqueante, coherencia]
---

# Número de iteraciones de construcción realizadas

Corresponde a la pregunta P-10 del plan
([[2026-09-19 Plan de integracion de correcciones]], p. 17).

**Por qué importa:** es la única de las seis preguntas bloqueantes que no requiere medición ni
gestión con terceros. Se resuelve recordando y revisando el repositorio, y hasta que se
resuelva hay una incoherencia visible entre el cuerpo del documento y su apéndice.

## Enunciado

Cuántas construcciones rápidas hubo realmente, y en qué fechas.

## Respuesta provisional

No resuelta, con contradicción documentada. El texto del borrador describe dos construcciones
rápidas, mientras que el apéndice del plan de desarrollo muestra una «Construcción rápida 3»
en la semana 10 ([[2026-09-19 Plan de integracion de correcciones]], p. 12).
#contradiccion

El plan agrega un señalamiento más severo sobre el mismo apéndice: el cronograma describía
actividades de otro proyecto —CRUD de «documentos», subida de archivos a un servicio de
almacenamiento, consentimiento y anonimización, revisión legal por abogado— y herramientas de
prueba distintas de las declaradas en el cuerpo del documento
([[2026-09-19 Plan de integracion de correcciones]], p. 12). El plan lo califica como uno de
los errores más visibles, y advierte que un jurado que lo detecte puede poner en duda el resto
del trabajo.

## Evidencia a favor de dos iteraciones

- El cuerpo del borrador documenta dos construcciones rápidas con sus funcionalidades
  ([[2026-09-19 Plan de integracion de correcciones]], p. 12).

## Evidencia a favor de tres

- El apéndice de plan de desarrollo sitúa una tercera en la semana 10
  ([[2026-09-19 Plan de integracion de correcciones]], p. 12).

La contradicción puede ser aparente: si el apéndice provenía de otro proyecto, su
«Construcción rápida 3» no es evidencia de nada sobre este. #suposicion

## Qué haría falta para cerrarla

- Historial del repositorio de código, que daría fechas verificables en lugar de recuerdo.
  #pendiente
- Una vez fijado el número, texto, cronograma y conclusiones deben decir lo mismo
  ([[2026-09-19 Plan de integracion de correcciones]], p. 12).

## Tercera versión: el anteproyecto aprobado

La ingesta de [[2026-09-19 Ficha de anteproyecto aprobada]] agrega una cifra más, y no
coincide con ninguna de las dos anteriores: el cronograma aprobado planifica **seis
iteraciones**, numeradas de la 0 a la 5, con fechas entre el 4 de noviembre de 2025 y el 30 de
enero de 2026 (p. 25-27). #contradiccion

El cuadro queda así:

| Fuente | Iteraciones | Ubicación |
|---|---|---|
| Anteproyecto aprobado | 6 (0 a 5) | ([[2026-09-19 Ficha de anteproyecto aprobada]], p. 25-27) |
| Cuerpo del borrador | 2 | ([[2026-09-19 Plan de integracion de correcciones]], p. 12) |
| Apéndice del borrador | 3 | ([[2026-09-19 Plan de integracion de correcciones]], p. 12) |

Las tres cifras no son necesariamente incompatibles: el anteproyecto declara lo **planificado**
y el borrador lo **ejecutado**, y que se ejecuten menos iteraciones de las planificadas es
normal. Lo que no es normal es que el propio borrador se contradiga consigo mismo, ni que el
informe final no explique la diferencia frente al cronograma aprobado. #suposicion

Al resolver esta pregunta hay que dejar coherentes **cuatro** documentos, no dos: cuerpo,
apéndice, conclusiones y cronograma del anteproyecto.

## Estado

- [x] Abierta / [ ] Resuelta
