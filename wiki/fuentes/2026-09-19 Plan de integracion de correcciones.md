---
tipo: fuente
estado: en-desarrollo
creado: 2026-09-19
actualizado: 2026-09-19
origen: documento
ruta: originales/documentos/2026-09-19 Plan de integracion de correcciones.pdf
consultado: 2026-09-19
autor_fuente: ""
fiabilidad: alta
tags: [plan, correcciones, metodologia]
---

# 2026-09-19 Plan de integracion de correcciones

**Qué es:** documento de trabajo de 18 páginas que recorre el borrador del trabajo de grado
bloque por bloque y, para cada uno, contrasta lo que el documento dice hoy con lo que debería
decir. Es el plan de acción sobre el que se hizo la reescritura del trabajo, no una fuente
externa sobre el dominio.

La portada nombra a Luis Fernando Caicedo Sánchez y Sebastián Salazar Caicedo con «Versión 1 ·
19 de septiembre de 2026», pero no declara quién redacta el plan frente a quién lo recibe.
Queda sin resolver si el autor es el equipo, el director o el evaluador. #pendiente

## Resumen

El plan parte de una tesis fuerte sobre el caso: el problema de la sucursal no es el uso de
Excel sino un control local de despacho sin validación, sin conciliación automática y sin
registro de cambios ([[2026-09-19 Plan de integracion de correcciones]], p. 4). De ahí se
derivan dos capas de trabajo. La primera es de coherencia: el borrador describe un rol
Mensajero con acceso al sistema y afirma trazabilidad en tiempo real, y ambas cosas son
incompatibles con la solución real, por lo que hay pasajes que deben corregirse antes de
agregar contenido nuevo (p. 2-3). La segunda es de contenido: faltan capítulos completos de
diagnóstico, diseño, evaluación de impacto y gestión de la implementación.

El documento fija una **regla transversal**: todo lo que se escriba debe marcarse como
diseñado, implementado o validado, y ningún tiempo, costo o conteo de errores se escribe sin
fuente (p. 1). Lo que no se tenga se mide o se declara como supuesto con su razonamiento. Esa
regla es la que convierte el plan en algo más que una lista de correcciones de estilo.

El plan describe además el proceso real de la sucursal, que según el propio documento es el
insumo más valioso del trabajo y no estaba en el borrador (p. 4): caracteriza trece
actividades del proceso actual (p. 4-5) y diez del proceso propuesto (p. 5-6), con ocho
reglas de negocio asociadas (p. 6).

Cierra con trece preguntas numeradas a los autores (p. 17) que condicionan el resto: sin
respuesta a varias de ellas, capítulos enteros no pueden escribirse con datos.

## Datos y afirmaciones clave

| Afirmación | Dato | Ubicación |
|---|---|---|
| El sistema tiene dos tipos de usuario; el mensajero es actor del proceso pero no del sistema | Administrador y Coordinador | p. 1 |
| Concentrar la captura en salida y retorno es decisión de diseño, no carencia | Evita dotar de dispositivos a 15 mensajeros y no cambia el trabajo en campo | p. 2 |
| Costo declarado de esa decisión | La trazabilidad es por puntos de control, no en tiempo real | p. 2 |
| La aplicación no elimina escaneos | Elimina el registro sin validación, el cotejo manual y la liquidación manual; agrega historial y auditoría | p. 4 |
| Cada guía se escanea tres veces al día | Una en el sistema corporativo y dos en Excel (salida y retorno) | p. 4 |
| Tiempo de liquidación reportado en entrevista | Cerca de 45 min, sin resolver si es por mensajero o por los 15 | p. 5, p. 17 |
| Volumen del libro histórico | Hasta 90 hojas por semana | p. 5 |
| Reglas de negocio propuestas | RN-01 a RN-08 | p. 6 |
| Criterio de segregación de funciones | Quien registra no es quien anula o ajusta | p. 12 |
| Cuello de botella del cronograma | La ruta crítica es la línea base | p. 16 |
| Preguntas que condicionan el plan | P-1 a P-13 | p. 17 |

## Citas textuales

> La aplicación no elimina escaneos. Lo que elimina es el registro sin validación, el cotejo
> manual y la liquidación manual, y además agrega historial y auditoría.
> — p. 4

> Regla transversal: todo lo que se escriba debe marcarse como diseñado, implementado o
> validado. Ningún tiempo, costo o conteo de errores se escribe sin fuente.
> — p. 1

> La fase 1 no necesita datos nuevos y puede avanzar desde hoy, mientras se hace la medición.
> La ruta crítica es la línea base.
> — p. 16

## Conexiones con el wiki

- Sostiene la hipótesis de trabajo de [[panorama]]: el Excel como sustituto de un control
  local ausente, no como mala elección de herramienta.
- Funda: [[Sistema paralelo de registro]], [[Trazabilidad por puntos de control]],
  [[Línea base de indicadores]], [[Segregación de funciones]].
- Caracteriza: [[Sucursal Inter Rapidísimo Jamundí]], [[Libro de Excel de despacho]].
- Abre: las seis preguntas bloqueantes listadas abajo.

Sin contradicciones con el wiki, porque es la primera fuente ingerida. El contraste real
aparecerá al ingerir el trabajo de grado y su versión previa.

## Qué abre

Seis preguntas con nota propia, por bloquear capítulos completos:

- [[Uso real del prototipo en la sucursal]] (P-1)
- [[Base de cálculo de la liquidación al mensajero]] (P-4)
- [[Alcance del sistema corporativo para la sucursal]] (P-7)
- [[Tiempo de archivo de las copias firmadas]] (P-8)
- [[Costo hora del coordinador de despacho]] (P-9)
- [[Número de iteraciones de construcción realizadas]] (P-10)

Las siete restantes (P-2, P-3, P-5, P-6, P-11, P-12, P-13) quedan listadas en
[[Preguntas abiertas]] sin nota propia por ahora. #pendiente

## Lectura crítica

El plan es un documento de trabajo interno, no una fuente sobre el dominio: su fiabilidad es
alta respecto de **qué dice el borrador y qué le falta**, porque eso lo verifica contra el
propio documento, y no aplica respecto de hechos del sector logístico, sobre los que no
aporta evidencia propia.

Conviene señalar dos cosas. La primera es que el plan propone reglas de negocio y capítulos
que en parte no existían en el borrador, de modo que describe un estado deseado y no un
estado alcanzado; confundir ambos al citarlo produciría exactamente el error que el plan
busca corregir. La segunda es que el propio plan advierte que varias de sus tablas —KPI,
análisis económico, riesgos— quedan en «X» mientras no se ejecute la campaña de medición
(p. 10), así que sus cifras no son datos sino plantillas de datos. #suposicion
