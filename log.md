---
tipo: sintesis
estado: en-desarrollo
creado: 2026-09-19
actualizado: 2026-09-19
tags: [meta]
---

# Registro

Append-only. Cada entrada abre con `## [AAAA-MM-DD] tipo | título` para que el log sea
parseable: `grep "^## \[" log.md | tail -5`.

---

## [2026-09-19] meta | Creación del wiki

- Estructura inicial: `originales/`, `wiki/` (fuentes, conceptos, entidades, preguntas, sintesis), `plantillas/`.
- Esquema definido en [[CLAUDE]]: tres capas, convenciones de nombres, frontmatter, citas y etiquetas de control; flujos de ingesta, consulta y lint.
- Decisiones de arranque: dominio = investigación de un tema; fuentes = web, documentos y notas de conversación; ingesta supervisada de a una fuente.
- Pendiente: definir la pregunta de investigación en [[panorama]] e ingerir la primera fuente. #pendiente

## [2026-09-19] meta | Definición de la pregunta de investigación

- Redactada la pregunta central en [[panorama]]: cómo rediseñar el proceso de control del despacho de última milla de la sucursal de Inter Rapidísimo en Jamundí y qué sistema de información debe soportarlo.
- Añadidas cuatro decisiones de alcance que delimitan qué cuenta como evidencia, marcadas #pendiente hasta que la ingesta las respalde con nota de fuente.
- Descompuesta la pregunta en seis frentes de evidencia (diagnóstico, rediseño, arquitectura, implementación, validación, impacto), reflejados en [[Preguntas abiertas]].
- Registrada una hipótesis de trabajo en la sección de tesis vigente, marcada #suposicion por no tener respaldo documental en el wiki todavía.
- Depositadas tres fuentes en `originales/documentos/` sin ingerir: plan de correcciones, trabajo de grado vigente y versión previa. Ninguna tiene nota de fuente: falta el paso de conversar hallazgos.
- Configurado el plugin de plantillas (`.obsidian/templates.json` → carpeta `plantillas`). Requiere reiniciar Obsidian para que tome efecto.
- Pendiente nuevo: verificar los datos bibliográficos de Quesada-Leiva (2022) y Chávez Benavides (2025), que no se encontraron en repositorio. #pendiente

## [2026-09-19] ingesta | Plan de integracion de correcciones

- Fuente: `originales/documentos/2026-09-19 Plan de integracion de correcciones.pdf`, 18 páginas. Nota creada: [[2026-09-19 Plan de integracion de correcciones]].
- Hallazgo central: el problema de la sucursal no es Excel sino un control local sin validación, sin conciliación automática y sin registro de cambios (p. 4). Eso reformula la pregunta de [[panorama]] de tecnología a control de proceso, y la tesis vigente pasa de hipótesis marcada #suposicion a afirmación con cita.
- Páginas creadas (13): conceptos [[Sistema paralelo de registro]], [[Trazabilidad por puntos de control]], [[Línea base de indicadores]], [[Segregación de funciones]]; entidades [[Sucursal Inter Rapidísimo Jamundí]], [[Libro de Excel de despacho]]; preguntas [[Uso real del prototipo en la sucursal]], [[Base de cálculo de la liquidación al mensajero]], [[Alcance del sistema corporativo para la sucursal]], [[Tiempo de archivo de las copias firmadas]], [[Costo hora del coordinador de despacho]], [[Número de iteraciones de construcción realizadas]].
- Páginas modificadas: [[panorama]] (tesis vigente con citas, sección de lo que la debilita), [[index]], [[Preguntas abiertas]] (tabla de estado de los seis frentes, trece preguntas del plan repartidas entre bloqueantes y resto).
- Contradicciones registradas #contradiccion: el borrador afirma a la vez que no hubo implementación y que el coordinador ya opera con el sistema (p. 17); el cuerpo dice dos construcciones rápidas y el apéndice muestra una tercera (p. 12). Ambas son inconsistencias internas del borrador, no choques entre fuentes.
- Debilidad de la tesis que la ingesta deja expuesta: la premisa de que el sistema corporativo no devuelve el control local se infiere de conducta observada, no de verificación técnica. Es la pregunta más probable del jurado según el propio plan (p. 8).
- Ruta crítica confirmada: la línea base (p. 16). Tres de las seis preguntas bloqueantes desembocan en ella.

## [2026-09-19] meta | Manual de uso de la bóveda

- Creada [[Manual de uso]]: uso de Obsidian (atajos, paneles, backlinks, grafo, propiedades), diccionario de indicativos (`tipo`, `estado`, `fiabilidad`, `origen`, las cuatro etiquetas de control, formato de cita, reglas de nombres), comandos para Claude por flujo (ingesta, consulta, lint, mantenimiento), reglas duras de ambos lados, rutina sugerida, búsquedas de Obsidian y solución de problemas.
- [[index]]: añadida sección Meta con [[Manual de uso]], [[panorama]] y [[log]].
- [[CLAUDE]]: el manual queda listado en la estructura y se añade la regla 6, que obliga a sincronizarlo cuando cambie una convención del esquema.
- Detectada nota fantasma vacía en la raíz, `AAAA-MM-DD Fuente.md`, creada al abrir un enlace de ejemplo de una plantilla. Documentada como caso en el manual; queda a la espera de confirmación para borrarla. #pendiente

## [2026-09-19] ingesta | Ficha de anteproyecto aprobada

- Fuente: `originales/documentos/2026-09-19 Ficha de anteproyecto aprobada.pdf`, 29 páginas. Nota: [[2026-09-19 Ficha de anteproyecto aprobada]]. Es el documento rector del trabajo y su autoridad es superior a la del resto de fuentes del wiki.
- Hallazgo que cambia la dirección: **la pregunta de investigación que figuraba en [[panorama]] no era la aprobada**. La aprobada es «¿Cómo facilitar a las sucursales de mensajería en Jamundí un proceso de despacho de guías que sea trazable, disminuya los errores humanos y reduzca las anomalías operativas, tomando a Inter Rapidísimo como referente?» (p. 3). La formulación anterior queda registrada como versión ampliada, en trámite de autorización.
- Brecha detectada entre lo aprobado y lo vigente en seis dimensiones: título, pregunta, objetivo general, número de objetivos (3 frente a 6), evaluación de impacto y carga de prueba. Comparación completa en [[Brecha entre el anteproyecto aprobado y el trabajo vigente]].
- Conflicto más serio: el anteproyecto renuncia por escrito a demostrar mejoras operativas (p. 5) y a asumir impactos en la operación real (p. 6), mientras el trabajo vigente incluye un capítulo de impacto con retorno de la inversión. No es una omisión del anteproyecto sino una renuncia deliberada, y por eso exige autorización y no solo justificación.
- **Decisión de los autores (2026-09-19):** sostener el alcance ampliado y solicitar la modificación formal del anteproyecto. Registrada en [[Aprobación del comité para la ampliación del alcance]].
- **Decisión de los autores (2026-09-19):** reportar la validación con el coordinador, amparándose en la metodología (p. 25) y el cronograma (p. 26) del propio anteproyecto, pese a que su objetivo específico 3 habla de pruebas internas del equipo (p. 4). La contradicción interna de la ficha queda documentada, no resuelta.
- Páginas creadas (3): [[2026-09-19 Ficha de anteproyecto aprobada]], [[Brecha entre el anteproyecto aprobado y el trabajo vigente]] (primera nota de `sintesis/`), [[Aprobación del comité para la ampliación del alcance]].
- Páginas modificadas (5): [[panorama]] (dos preguntas, aprobada y ampliada, con la dependencia del comité), [[Número de iteraciones de construcción realizadas]] (tercera cifra: 6 planificadas), [[Uso real del prototipo en la sucursal]] (el anteproyecto compromete entorno controlado; confianza sube de baja a media), [[Trazabilidad por puntos de control]] (el cronograma aprobado incluye mensajeros como usuarios de validación), [[index]] y [[Preguntas abiertas]].
- Contradicciones nuevas #contradiccion: alcance aprobado frente a vigente; tres cifras de iteraciones; mensajeros como usuarios de validación; la ficha contra sí misma en validación interna frente a usuarios reales.
- Fuera del wiki: generado `Solicitud de modificacion de anteproyecto.docx` en el directorio del proyecto, y añadida a la sección 1.4 del trabajo de grado la declaración de la modificación de alcance.
- Pendientes nuevos: recuperar el documento de correcciones del evaluador (es el argumento más fuerte ante el comité y ya no está en el directorio); completar el nombre del director, en blanco en la ficha aprobada. #pendiente

## [2026-09-24] meta | Credenciales de la plataforma

- Creada la carpeta `privado/` para datos sensibles que no forman parte del wiki, con el nuevo tipo `privado`.
- Nota `privado/Acceso a la plataforma.md`: usuario administrador de la aplicación (Luis_Fdo, rol Administrador), URLs del backend y del frontend y cómo arrancar el servidor. La contraseña se verificó contra la base de datos.
- No se guardaron la contraseña del usuario MySQL `despacho` (vive en `plataforma/backend/.env`) ni la de root.
- Convención añadida a [[CLAUDE]] y a [[Manual de uso]] (regla 6); entrada sin enlace en [[index]].

## [2026-09-24] meta | Documentación del backend y del frontend

- Creadas en `privado/` las notas [[Backend de la plataforma]] (stack, base de datos con la contraseña del usuario `despacho`, configuración, estructura, rutas y comandos) y [[Frontend de la plataforma]] (stack, estructura, rutas, proxy y comandos).
- La nota de acceso enlaza ahora a ambas. Añadidas al índice sin enlace, como el resto de `privado/`.
- No se guardaron la contraseña de root de MySQL ni la `DJANGO_SECRET_KEY`.

## [2026-09-24] meta | Plataforma: módulos del coordinador y del administrador

- Implementados asignación con escaneo continuo, búsqueda, cobro diario con contra entregas, dashboard, mensajeros e historial con ajustes del administrador, según la especificación dictada por el usuario.
- Actualizadas [[Backend de la plataforma]] y [[Frontend de la plataforma]] (rutas, reglas y estado).
- Decisión de diseño que se aparta del trabajo de grado: el cobro usa precio estimado por el coordinador y registra contra entregas; coincide con el cuadre real de marzo. #pendiente reflejarlo en la regla RN-06 del documento.

## [2026-09-24] meta | Ingreso por documento y rediseño visual

- La aplicación ahora se ingresa con tipo de documento, número y contraseña; el rol sale de la cuenta. Actualizada [[Acceso a la plataforma]] y [[Backend de la plataforma]].
- Rediseño de la interfaz con la guía ui-ux-pro-max: estilo minimalista, azul #2563EB con acento naranja, fuente Inter, íconos SVG, foco visible y contraste AA.

## [2026-09-24] meta | Datos de mensajeros y usuarios

- Mensajeros con documento tipificado, nombre en cuatro partes, vehículo y placa validada por tipo; usuarios (coordinadores y administradores) con nombre en cuatro partes y pantalla de gestión propia. Actualizada [[Backend de la plataforma]].
- Supuesto sin fuente: formato del carro moto aceptado como alfanumérico de 5 a 7 caracteres. #suposicion

## [2026-09-24] meta | Reporte del dashboard y contra entregas por jornada

- Dashboard con periodos rápidos (hoy, ayer, 7 días, mes) y botón «Generar reporte»: página imprimible/PDF y descarga CSV con resumen, por mensajero, por día, detalle de contra entregas y cobros. Cada reporte generado queda en auditoría.
- Las contra entregas se cuentan por jornada de reparto; solo un rango de fechas las acumula. Cubierto con prueba automática.

## [2026-09-24] meta | Identidad Trackly

- Eliminadas de la plataforma las menciones a Inter Rapidísimo (recibos, reporte e inicio de sesión). El trabajo de grado y este wiki no se tocaron: ahí la empresa es el caso de estudio.
- Nombre elegido por el usuario: Trackly. Logo propio (ruta de origen a destino), paleta tinta-piedra-dorado y tipografía Plus Jakarta Sans. Actualizada [[Frontend de la plataforma]].

## [2026-09-24] meta | Paleta grafito + azul petróleo

- El usuario cambió la paleta de Trackly: grafito `#1F2328` y azul petróleo `#1F6F78` sobre gris frío. Actualizada [[Frontend de la plataforma]].

## [2026-09-24] meta | Control de seguridad: guías ajenas en el cuadre

- Si en el cobro el mensajero presenta una guía que no llevaba, la plataforma la clasifica (en ruta con otro mensajero, ya entregada, debía estar en bodega, no registrada, otra jornada), muestra su información y emite un tono de alerta.
- Cada alerta queda registrada (tabla AlertaGuia y auditoría), aparece en el recibo de cobro con las tres firmas, en el reporte y como aviso en el Dashboard.
- Refuerza el argumento de control interno del trabajo de grado (segregación y evidencia ante faltantes). #pendiente reflejarlo en el capítulo 4.

## [2026-09-24] meta | Punto de continuación

- Creada [[Punto de continuación]]: estado completo de Trackly, cómo arrancarla, datos reales en la base, decisiones del usuario y pendientes de plataforma, trabajo de grado y wiki.
- [[CLAUDE]] y [[Manual de uso]]: al trabajar en la plataforma se lee esa nota al inicio y se actualiza al cierre. Añadida al [[index]].

## [2026-10-24] meta | Plataforma: guías por mensajero (vista de conciliación)

- Implementada la vista de conciliación de la Tabla 11 (T7) según `proyecto-grado-latex_1.pdf`: por jornada, lo despachado a cada mensajero frente a lo entregado, con las guías sin estado final de jornadas anteriores. Actualizada [[Punto de continuación]].
- Estados con el vocabulario del documento: Pendiente, En reparto, Entregada, Devuelta.
- Sin zonas ni reglas RN inventadas: el PDF las nombra pero no las define. #pendiente

## [2026-10-24] meta | Plataforma: recibos en ventana emergente

- A pedido del usuario, todos los recibos y el reporte del Dashboard se abren en una ventana emergente del navegador. Detalle en [[Punto de continuación]]. #pendiente probarlo en el navegador.

## [2026-10-24] meta | Plataforma: funciones del administrador

- CRUD de mensajeros completo: eliminar solo sin historial; con historial se desactiva, para conservar la trazabilidad.
- Nuevas pantallas del administrador: pista de auditoría y copias de seguridad (crear, verificar, descargar, eliminar, retención). Comandos `respaldar` y `restaurar`; restauración ensayada sobre `test_despacho` con conteos iguales a la base real.
- Actualizadas [[Punto de continuación]], [[Backend de la plataforma]] y [[Frontend de la plataforma]]. #pendiente programar la copia diaria.

## [2026-10-24] meta | Plataforma: recorrido de bienvenida y configuración de la cuenta

- Usuario nuevo: recorrido guiado de la jornada normal (salida, conciliación, retorno y liquidación, consulta e indicadores) más las funciones de su rol; se muestra una sola vez.
- Nueva pantalla Configuración de la cuenta: datos propios, cambio de contraseña y botón para repetir el tutorial. Actualizadas [[Punto de continuación]], [[Backend de la plataforma]] y [[Frontend de la plataforma]].
