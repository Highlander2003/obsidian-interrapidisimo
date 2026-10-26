---
tipo: concepto
estado: en-desarrollo
creado: 2026-09-19
actualizado: 2026-09-19
tags: [diagnostico, proceso]
---

# Sistema paralelo de registro

**En una frase:** registro local que una unidad operativa sostiene por fuera del sistema
corporativo porque ese sistema no le devuelve el control que necesita para operar.

## Qué es

En la sucursal, cada guía se escanea tres veces al día: una en el sistema corporativo del
operador, que notifica al destinatario, y dos en un libro de Excel, a la salida y al retorno
([[2026-09-19 Plan de integracion de correcciones]], p. 4). El libro no duplica al sistema
corporativo por descuido: existe porque el sistema corporativo no le da a la sucursal el
control de la relación mensajero–guía–pago (p. 4).

Esa lectura es la que reformula el problema. Si el Excel fuera una mala elección de
herramienta, la solución sería cambiar de herramienta. Si es el sustituto de un control que
no existe, la solución es construir ese control, y la herramienta es consecuencia y no causa.
El plan lo enuncia así: el problema no es «Excel», sino un control local de despacho sin
validación, sin conciliación automática y sin registro de cambios (p. 4).

## Cómo funciona / de dónde sale

El mecanismo tiene tres carencias que se encadenan:

1. **Captura sin validación.** El dato entra sin que nada verifique formato ni unicidad en el
   momento del escaneo, de modo que el error se detecta después o no se detecta.
2. **Conciliación manual.** La comparación entre lo despachado y lo retornado se hace a mano,
   así que un error de la salida se propaga hasta la liquidación.
3. **Sin registro de cambios.** El libro es compartido y no identifica quién modificó qué,
   por lo que una alteración no deja rastro (p. 4).

La consecuencia práctica es que el pago a quince mensajeros se sostiene sobre un archivo que
no puede auditarse.

## Evidencia

| Qué dice | Fuente | Fuerza |
|---|---|---|
| El Excel existe porque el sistema corporativo no entrega el control local mensajero–guía–pago | ([[2026-09-19 Plan de integracion de correcciones]], p. 4) | fuerte |
| Tres escaneos diarios por guía, dos de ellos en la misma ventana de salida | ([[2026-09-19 Plan de integracion de correcciones]], p. 4) | fuerte |
| La intervención no elimina escaneos; elimina el registro sin validación, el cotejo manual y la liquidación manual | ([[2026-09-19 Plan de integracion de correcciones]], p. 4) | fuerte |
| El libro histórico acumula hasta 90 hojas por semana | ([[2026-09-19 Plan de integracion de correcciones]], p. 5) | media |

## Tensiones y matices

La afirmación central —que el sistema corporativo no devuelve el control local— está tomada
del plan, que a su vez la infiere de la conducta observada en la sucursal. El propio plan
reconoce que no sabe qué permite exactamente el sistema corporativo y lo convierte en
pregunta abierta (p. 17). Mientras esa pregunta siga sin respuesta, el argumento se sostiene
sobre evidencia conductual y no sobre evidencia técnica. Ver
[[Alcance del sistema corporativo para la sucursal]]. #pendiente

## Relacionado

- [[Libro de Excel de despacho]] — el artefacto concreto en que se materializa.
- [[Trazabilidad por puntos de control]] — la capacidad que el registro paralelo no puede dar.
- [[Segregación de funciones]] — el control que su naturaleza de archivo compartido impide.
- [[Sucursal Inter Rapidísimo Jamundí]] — el caso donde se observa.

## Fuentes que lo tratan

- [[2026-09-19 Plan de integracion de correcciones]]
