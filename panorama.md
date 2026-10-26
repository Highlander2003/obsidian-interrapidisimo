---
tipo: sintesis
estado: en-desarrollo
creado: 2026-09-19
actualizado: 2026-09-19
tags: [meta]
---

# Panorama

Puerta de entrada al wiki: qué se está investigando, qué se sabe hoy y con cuánta confianza.
Claude reescribe esta nota cada vez que una fuente mueve la tesis. Catálogo completo en
[[index]]; historia en [[log]].

## Pregunta de investigación

### Aprobada por la facultad

> **¿Cómo facilitar a las sucursales de mensajería en Jamundí un proceso de despacho de guías
> que sea trazable, disminuya los errores humanos y reduzca las anomalías operativas, tomando
> a Inter Rapidísimo como referente?**
>
> ([[2026-09-19 Ficha de anteproyecto aprobada]], p. 3)

Esta es la pregunta del anteproyecto aprobado y, mientras el comité no autorice otra cosa, es
la que un jurado tomará como referencia.

### Ampliada, en trámite de autorización

> ¿Cómo rediseñar el proceso de control del despacho de última milla de la sucursal de
> referencia, y qué sistema de información debe soportarlo, para reducir los errores de
> registro y el tiempo de conciliación y liquidación, garantizar la trazabilidad por guía y
> resultar económicamente viable?

Es la formulación que rige el trabajo de grado vigente. Conserva el núcleo de la aprobada
—trazabilidad, errores, anomalías operativas— y añade conciliación, liquidación y viabilidad
económica. Los autores decidieron el 2026-09-19 sostener esta versión y solicitar la
modificación formal del anteproyecto. Hasta que el comité responda, **ninguna de las dos se
da por firme**: ver [[Aprobación del comité para la ampliación del alcance]].

La comparación completa entre lo aprobado y lo vigente está en
[[Brecha entre el anteproyecto aprobado y el trabajo vigente]]. #contradiccion

### Qué delimita la pregunta

| Decisión de alcance | Consecuencia para el wiki | Respaldo |
|---|---|---|
| El objeto es el proceso de despacho, no la aplicación | Una fuente sobre frameworks web no aporta; una sobre control interno o rediseño de procesos, sí | ([[2026-09-19 Plan de integracion de correcciones]], p. 4) |
| La sucursal es caso de referencia, no muestra estadística | Los hallazgos se transfieren por mecanismo, no se generalizan por frecuencia | #suposicion |
| El mensajero es actor del proceso, no usuario del sistema | Deja fuera la geolocalización y el seguimiento continuo | ([[2026-09-19 Plan de integracion de correcciones]], p. 1-2), en tensión con la ficha p. 26 |
| Todo dato lleva condición: diseñado, implementado o validado | Ninguna cifra entra sin su origen y su estado | ([[2026-09-19 Plan de integracion de correcciones]], p. 1) |

### Descomposición operativa

Seis frentes de evidencia. Los tres primeros corresponden a los objetivos aprobados; los tres
últimos son la ampliación en trámite.

1. **Diagnóstico** — cómo opera hoy el proceso, sus puntos críticos y su línea base medida.
2. **Rediseño** — qué actividades cambian y bajo qué reglas de negocio.
3. **Arquitectura** — procesos, información, aplicaciones e infraestructura.
4. **Implementación** — qué se construyó frente a qué quedó especificado.
5. **Validación** — qué se probó, con qué método y bajo qué condición.
6. **Impacto y viabilidad** — qué cambió de forma medible y si se sostiene económicamente.

Estado de cada frente en [[Preguntas abiertas]].

## Tesis vigente

El problema de la sucursal no es el uso de una hoja de cálculo, sino un control local de
despacho que carece de validación en la captura, de conciliación automática y de registro de
cambios ([[2026-09-19 Plan de integracion de correcciones]], p. 4). El libro de Excel no es
una mala elección de herramienta: es el sustituto de un control que el sistema corporativo no
le devuelve a la sucursal, y por eso la intervención debe dirigirse al proceso y a su control
antes que a la tecnología. Ver [[Sistema paralelo de registro]].

De esa lectura se sigue el alcance de la solución: la captura se concentra en los dos puntos de
control por los que toda guía pasa físicamente por el escritorio del coordinador, con el costo
declarado de que la trazabilidad resultante es por puntos de control y no continua
([[2026-09-19 Plan de integracion de correcciones]], p. 2). Ver
[[Trazabilidad por puntos de control]].

**Nivel de confianza: medio.** Dos fuentes ingeridas, ambas internas al proyecto. Ninguna
fuente externa respalda todavía el diagnóstico.

## Qué sostiene la tesis

- La aplicación no elimina escaneos; elimina el registro sin validación, el cotejo manual y la
  liquidación manual ([[2026-09-19 Plan de integracion de correcciones]], p. 4).
- Ocho reglas de negocio, cada una contra un problema concreto del proceso actual
  ([[2026-09-19 Plan de integracion de correcciones]], p. 6).
- El argumento de control interno: quien registra no es quien anula o ajusta
  ([[2026-09-19 Plan de integracion de correcciones]], p. 12). Ver [[Segregación de funciones]].

## Qué la debilita o contradice

- **El alcance vigente excede al aprobado.** El anteproyecto renuncia por escrito a demostrar
  mejoras operativas ([[2026-09-19 Ficha de anteproyecto aprobada]], p. 5-6), y el trabajo
  vigente incluye un capítulo de impacto con retorno de la inversión. Es el riesgo formal más
  serio y está en trámite. #contradiccion
- **La premisa central no está verificada técnicamente.** Que el sistema corporativo no
  devuelva el control local se infiere de conducta observada. Ver
  [[Alcance del sistema corporativo para la sucursal]].
- **No hay línea base medida.** Sin valores «antes» la mejora no es demostrable; es la ruta
  crítica ([[2026-09-19 Plan de integracion de correcciones]], p. 16). Ver
  [[Línea base de indicadores]].
- **Tres cifras distintas de iteraciones** entre anteproyecto, cuerpo y apéndice. Ver
  [[Número de iteraciones de construcción realizadas]]. #contradiccion
- **El anteproyecto se contradice a sí mismo** sobre si la validación es interna o con
  usuarios reales ([[2026-09-19 Ficha de anteproyecto aprobada]], p. 4-5 frente a p. 25-26).

## Frentes abiertos

Siete preguntas con nota propia. La de mayor prioridad es
[[Aprobación del comité para la ampliación del alcance]], porque de ella depende la
admisibilidad del resto. Lista completa en [[Preguntas abiertas]].

## Fuentes disponibles sin ingerir

- `2026-09-19 Proyecto de Grado con correcciones integradas.docx` — versión vigente, nueve
  capítulos.
- `2026-09-09 Proyecto de Grado version previa.pdf` — versión anterior a las correcciones.
