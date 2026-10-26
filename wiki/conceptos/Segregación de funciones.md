---
tipo: concepto
estado: semilla
creado: 2026-09-19
actualizado: 2026-09-19
tags: [control-interno, seguridad, diseno]
---

# Segregación de funciones

**En una frase:** repartir una operación sensible entre personas distintas, de manera que
quien la registra no sea quien la autoriza, la anula o la ajusta.

## Qué es

Es el argumento de control interno que sostiene la matriz de permisos del sistema. El plan lo
enuncia de forma directa: quien registra no es quien anula o ajusta, y lo conecta con el
riesgo de fraude identificado en el diagnóstico del borrador
([[2026-09-19 Plan de integracion de correcciones]], p. 12).

Su relevancia aquí es concreta y no abstracta: el proceso termina en un pago a un tercero. Si
la misma persona registra las entregas, calcula la liquidación y puede ajustarla después sin
dejar rastro, no existe control alguno sobre ese pago.

## Cómo funciona / de dónde sale

El plan propone una matriz de permisos por función y rol (p. 11-12), con dos particularidades
de diseño:

- Ciertas funciones quedan **vedadas al coordinador por segregación**, no por falta de
  confianza: resolver un faltante y anular o ajustar una liquidación cerrada.
- La columna del mensajero se conserva con la anotación «no es usuario», de modo que la matriz
  responda de forma visible a la pregunta del evaluador sin sugerir que se trate de un rol con
  permisos restringidos (p. 12).

Varias celdas quedan marcadas como pendientes de definir con la sucursal, porque dependen de
quién sea el administrador en la realidad y qué haga que el coordinador no haga (p. 11, 17).

## Evidencia

| Qué dice | Fuente | Fuerza |
|---|---|---|
| Quien registra no es quien anula o ajusta | ([[2026-09-19 Plan de integracion de correcciones]], p. 12) | fuerte |
| Mantener la columna «Mensajero: no es usuario» responde de forma visible a la matriz del evaluador | ([[2026-09-19 Plan de integracion de correcciones]], p. 12) | media |
| El reparto exacto de funciones entre Administrador y Coordinador está sin definir | ([[2026-09-19 Plan de integracion de correcciones]], p. 11, 17) | fuerte |

## Tensiones y matices

La segregación supone al menos dos personas distintas operando el sistema. En una sucursal
donde el coordinador es quien ejecuta casi todo el proceso, existe el riesgo de que el
administrador sea una figura nominal y que ambos roles terminen usando la misma cuenta, con lo
que el control se vuelve decorativo. El plan lo registra como riesgo explícito, con cuentas
nominales y revisión de auditoría como mitigación (p. 14). #suposicion

## Relacionado

- [[Sistema paralelo de registro]] — la situación sin ningún control de este tipo.
- [[Trazabilidad por puntos de control]] — el otro control del diseño.
- [[Libro de Excel de despacho]] — donde la ausencia de segregación es total.

## Fuentes que lo tratan

- [[2026-09-19 Plan de integracion de correcciones]]
