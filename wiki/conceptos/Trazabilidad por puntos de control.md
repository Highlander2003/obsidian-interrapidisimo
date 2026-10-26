---
tipo: concepto
estado: en-desarrollo
creado: 2026-09-19
actualizado: 2026-09-19
tags: [diseno, trazabilidad, alcance]
---

# Trazabilidad por puntos de control

**En una frase:** registrar el estado de un envío en los momentos definidos en que pasa
físicamente por una estación de trabajo, en lugar de observarlo de forma continua durante el
trayecto.

## Qué es

Es la decisión de diseño que delimita todo el alcance del trabajo. La captura se concentra en
los dos momentos en que toda guía pasa por el escritorio del coordinador —la salida y el
retorno— en vez de distribuirse en dispositivos que portarían los mensajeros
([[2026-09-19 Plan de integracion de correcciones]], p. 2).

El plan la presenta explícitamente como decisión y no como carencia, con tres argumentos: no
obliga a dar dispositivos ni datos móviles a quince mensajeros, reduce la superficie de
ataque y no cambia el trabajo en campo (p. 2).

## Cómo funciona / de dónde sale

El corolario es el que hay que sostener en la sustentación: entre la salida y el retorno la
guía solo puede figurar «En reparto», porque durante ese intervalo ningún componente del
sistema observa nada (p. 2). De ahí que el plan exija eliminar del documento toda afirmación
de «tiempo real» (p. 2).

Conviene separar dos capacidades que suelen confundirse:

| Capacidad | Pregunta que responde | ¿La da este diseño? |
|---|---|---|
| Consulta de estado | Dónde está la guía ahora | Sí, con la precisión del último punto de control |
| Historial de eventos | Qué le pasó, cuándo y por decisión de quién | Sí, si se registran eventos y no solo el último estado |
| Observación continua | Por dónde va el mensajero en este momento | No, y está excluido a propósito |

## Evidencia

| Qué dice | Fuente | Fuerza |
|---|---|---|
| Concentrar la captura en salida y retorno es decisión de diseño, no carencia | ([[2026-09-19 Plan de integracion de correcciones]], p. 2) | fuerte |
| Costo declarado: trazabilidad por puntos de control, no en tiempo real | ([[2026-09-19 Plan de integracion de correcciones]], p. 2) | fuerte |
| La geolocalización se excluye porque el mensajero no usa ningún dispositivo del sistema | ([[2026-09-19 Plan de integracion de correcciones]], p. 2) | fuerte |
| La unidad espacial del proceso es la zona o estantería, modelable sin GPS | ([[2026-09-19 Plan de integracion de correcciones]], p. 2) | media |

## Tensiones y matices

El plan advierte que el borrador afirmaba trazabilidad en tiempo real en varios lugares
—introducción, marco teórico, resultados y conclusiones— y que esas afirmaciones son
incompatibles con el diseño real (p. 3). No es una contradicción entre fuentes sino una
inconsistencia interna del borrador, que el plan manda corregir. Si al ingerir el trabajo de
grado vigente quedara algún rastro de «tiempo real», eso sí sería material para
`#contradiccion`.

Segundo matiz: la validación en la captura impide registrar dos veces la misma guía, pero no
impide por sí sola escanear una guía al mensajero equivocado; el plan señala que eso se
mitiga con el mensajero activo en pantalla y el contador de lote, no se elimina (p. 13).

## Tensión con el anteproyecto aprobado

El cronograma del anteproyecto incluye a los mensajeros entre los usuarios de validación:
«Validación del prototipo con usuarios (coordinador/mensajeros)»
([[2026-09-19 Ficha de anteproyecto aprobada]], p. 26). La decisión de diseño vigente sostiene
que el mensajero es actor del proceso y no usuario del sistema, de modo que no habría nada que
validar con él. #contradiccion

Las dos versiones se conservan. La lectura más probable es que el anteproyecto se redactó
antes de tomar la decisión de concentrar la captura en dos puntos de control, y que la
mención a los mensajeros quedó de una idea previa del sistema; pero eso es inferencia y no
consta en ninguna fuente. #suposicion

No es un problema de alcance frente al comité, porque restringir quién valida no amplía el
compromiso adquirido. Sí es un problema de coherencia si un jurado compara los dos documentos.
Ver [[Brecha entre el anteproyecto aprobado y el trabajo vigente]].

## Relacionado

- [[Sistema paralelo de registro]] — la carencia que este diseño ataca.
- [[Segregación de funciones]] — el otro control que el diseño incorpora.
- [[Uso real del prototipo en la sucursal]] — decide si la trazabilidad se probó en operación
  o solo con datos simulados.

## Fuentes que lo tratan

- [[2026-09-19 Plan de integracion de correcciones]]
