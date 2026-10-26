---
tipo: entidad
estado: en-desarrollo
creado: 2026-09-19
actualizado: 2026-09-19
clase: producto
tags: [as-is, artefacto]
---

# Libro de Excel de despacho

**En una frase:** archivo de hoja de cálculo con macros, con una hoja por mensajero y por día,
sobre el que hoy se sostienen el control del despacho y la liquidación del pago.

## Ficha

| Campo | Valor | Fuente |
|---|---|---|
| Estructura | Una hoja por mensajero y por día | ([[2026-09-19 Plan de integracion de correcciones]], p. 4) |
| Método de captura | Escanear con pistola lectora y pulsar Enter | ([[2026-09-19 Plan de integracion de correcciones]], p. 4) |
| Momentos de uso | Salida (actividad A6) y retorno (actividad A9) | ([[2026-09-19 Plan de integracion de correcciones]], p. 4-5) |
| Acumulación histórica | Hasta 90 hojas por semana | ([[2026-09-19 Plan de integracion de correcciones]], p. 5) |
| Control de acceso | Ninguno; libro compartido sin roles ni registro de cambios | ([[2026-09-19 Plan de integracion de correcciones]], p. 4) |

## Qué sabemos

Es el artefacto donde se materializa el [[Sistema paralelo de registro]]. Los errores que
produce están tipificados en la caracterización del proceso
([[2026-09-19 Plan de integracion de correcciones]], p. 4-5): doble escaneo, celda saltada o
sobrescrita, guía registrada en la hoja del mensajero equivocado y digitación manual cuando el
código de barras no lee. Los mismos errores se repiten en el escaneo de retorno (p. 5).

Dos consecuencias derivadas, más allá del error de captura. La primera es que el cotejo entre
lo despachado y lo entregado se hace comparando dos listas sin que nada verifique que una guía
marcada como entregada estuviera despachada a ese mismo mensajero, de modo que un faltante
real puede confundirse con un error de registro (p. 5). La segunda es que, al conservar una
fila por guía y por día sin registro de cambios de estado, el historial de una guía no es
reconstruible: es una imposibilidad de diseño y no una deficiencia de los datos capturados.
#suposicion

El plan mantiene el libro como alternativa evaluada y no descartada de entrada: la opción de
mejorarlo con validación de datos, hojas protegidas y una macro de cotejo se compara
formalmente contra el desarrollo a medida, precisamente porque responder «por qué no bastaba
con mejorar el Excel» es la objeción más previsible en la sustentación (p. 10).

## Papel en la investigación

Es el término de comparación de toda la evaluación de impacto: los indicadores «antes» de
[[Línea base de indicadores]] se miden sobre él, y el indicador de errores de registro por
cada mil guías sale de procesar sus libros históricos (p. 10). De ahí que el acceso a esos
archivos sea una condición para cerrar el capítulo de impacto: ver
[[Tiempo de archivo de las copias firmadas]].

## Relacionado

- [[Sistema paralelo de registro]] — el fenómeno del que es la manifestación concreta.
- [[Segregación de funciones]] — el control que su naturaleza de archivo compartido impide.
- [[Sucursal Inter Rapidísimo Jamundí]] — dónde se usa.

## Fuentes que la mencionan

- [[2026-09-19 Plan de integracion de correcciones]]
