---
tipo: pregunta
estado: en-desarrollo
creado: 2026-09-19
actualizado: 2026-09-19
tags: [P-8, bloqueante, continuidad, medicion]
---

# Tiempo de archivo de las copias firmadas

Corresponde a la pregunta P-8 del plan
([[2026-09-19 Plan de integracion de correcciones]], p. 17).

**Por qué importa:** tiene dos consecuencias que no se parecen entre sí. Fija el objetivo de
punto de recuperación del sistema, y condiciona el acceso a los datos que alimentan
[[Línea base de indicadores]].

## Enunciado

Qué ocurre con las copias de guía firmadas y con los libros de Excel de meses anteriores.

## Sub-preguntas del plan

- ¿Las copias firmadas se archivan en la sucursal, y por cuánto tiempo, o se envían a Cali?
- ¿Hay acceso a los libros de Excel de meses anteriores?

## Respuesta provisional

No resuelta. El plan propone un criterio que depende por completo de esta respuesta: el
objetivo de punto de recuperación no debería superar el tiempo durante el cual existen en la
sucursal las copias físicas que permiten reconstruir los registros
([[2026-09-19 Plan de integracion de correcciones]], p. 12). El razonamiento es que mientras
esas copias estén disponibles, la información es recuperable por otro medio y la pérdida de
datos no es definitiva.

Es un criterio elegante porque deriva el parámetro técnico de un hecho del proceso en lugar de
fijarlo por convención, pero queda inservible sin el dato.

## Evidencia disponible

- El plan propone derivar el objetivo de punto de recuperación de la permanencia de las copias
  físicas ([[2026-09-19 Plan de integracion de correcciones]], p. 12).
- El indicador de errores de registro por cada mil guías se obtiene procesando los libros
  históricos, con un mínimo sugerido de un mes de datos
  ([[2026-09-19 Plan de integracion de correcciones]], p. 10).

## Qué haría falta para cerrarla

- Respuesta de los autores sobre el destino y el plazo de archivo de las copias. #pendiente
- Confirmación de acceso a los libros históricos. Sin ellos, el indicador de errores de
  registro no tiene valor «antes» y la comparación de impacto pierde su fila más
  demostrativa. #pendiente

Si las copias se envían a Cali poco después del retorno, el objetivo de punto de recuperación
se vuelve mucho más exigente de lo que el criterio sugiere, porque desaparece el respaldo
físico que justificaba tolerar pérdida de datos. #suposicion

## Estado

- [x] Abierta / [ ] Resuelta
