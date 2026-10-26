# Esquema del wiki

Esta bóveda es un **wiki de investigación mantenido por LLM**. Claude escribe y mantiene el
wiki; el usuario aporta fuentes, dirección y preguntas. El wiki no es un buscador sobre
documentos: es un artefacto que se **compila una vez y se mantiene al día**, y que se vuelve
más rico con cada fuente ingerida y cada pregunta respondida.

**Al inicio de cada sesión:** lee este archivo, luego `index.md`, luego las últimas entradas
del log (`grep "^## \[" log.md | tail -8`). No hace falta leer todo el wiki.
Si la sesión es sobre la plataforma Trackly, lee además `privado/Punto de continuación.md` y
actualízalo al cerrar la sesión.

Idioma de todo el contenido: **español**. Los términos técnicos se conservan en su forma
original.

---

## 1. Las tres capas

| Capa | Ubicación | Quién escribe | Regla |
|---|---|---|---|
| Fuentes originales | `originales/` | El usuario (o Claude al descargar web) | **Inmutable.** Nunca edites, muevas ni borres nada de aquí. Solo lectura. Es la verdad de referencia. |
| El wiki | `wiki/` + notas de raíz | **Solo Claude** | Todo es contenido derivado: resúmenes, conceptos, entidades, síntesis. Se reescribe y refina libremente. |
| El esquema | `CLAUDE.md` | Ambos, en conversación | Cuando una convención no funcione, se cambia aquí y se aplica de ahí en adelante. |

El usuario puede escribir en el wiki, pero por defecto no lo hace. Si una nota tiene
`autor: usuario` en el frontmatter, **no la reescribas**: solo añade enlaces o una sección
`## Notas de Claude` al final.

---

## 2. Estructura de carpetas

```
CLAUDE.md               este esquema
Manual de uso.md        el mismo esquema traducido para el usuario, más el uso de Obsidian
index.md                catálogo de todo el wiki (orientado a contenido)
log.md                  registro cronológico append-only (orientado a tiempo)
panorama.md             puerta de entrada: estado de la investigación y tesis vigente

originales/             FUENTES INMUTABLES
  documentos/           PDF, docx, xlsx, imágenes que aporta el usuario
  web/                  copias en markdown de páginas web, con URL y fecha de consulta

wiki/
  fuentes/              una nota por fuente ingerida (resumen + extracción + enlaces)
  conceptos/            ideas, mecanismos, métodos, teorías
  entidades/            personas, organizaciones, productos, lugares, estudios concretos
  preguntas/            preguntas abiertas de la investigación, con su estado
  sintesis/             comparativas, análisis, respuestas archivadas, tesis en evolución

plantillas/             plantillas de cada tipo de nota

privado/                datos operativos sensibles (credenciales). Fuera del wiki: tipo `privado`,
                        no se cita, no se enlaza desde notas del wiki y no se sube a servicios externos.
```

---

## 3. Convenciones

### Nombres de archivo
- Fuentes: `AAAA-MM-DD Título corto` → `wiki/fuentes/2026-09-19 Informe anual de X.md`
- Conceptos y entidades: nombre natural en singular → `wiki/conceptos/Sesgo de supervivencia.md`
- Preguntas: enunciado sin signos de interrogación → `wiki/preguntas/Efecto de X sobre Y.md`
- **Prohibido en nombres de archivo (Windows):** `? : * " < > | \ /`

### Frontmatter obligatorio

```yaml
---
tipo: fuente | concepto | entidad | pregunta | sintesis
estado: semilla | en-desarrollo | estable | obsoleta
creado: AAAA-MM-DD
actualizado: AAAA-MM-DD
tags: []
---
```

Las notas de tipo `fuente` añaden:

```yaml
origen: documento | web | conversacion
ruta: originales/documentos/archivo.pdf   # o la URL si es web
consultado: AAAA-MM-DD
autor_fuente: ""
fiabilidad: alta | media | baja
```

### Enlaces y citas
- Enlaza con `[[Nombre de la nota]]` siempre que menciones algo que tiene (o debería tener)
  página propia. Enlaza generosamente: un `[[enlace]]` a una nota inexistente es una señal
  válida de "esto merece página", no un error.
- **Toda afirmación no trivial lleva cita** a la nota de fuente de donde salió:
  `El margen cayó 4 puntos en 2025 ([[2026-09-19 Informe anual de X]], p. 12).`
- Cita textual: bloque `>` seguido de la referencia con página o timestamp.
- Si una afirmación no viene de ninguna fuente sino de razonamiento propio, márcala con
  `#suposicion`. Nunca la presentes como dato de fuente.

### Etiquetas de control (búsquedas rápidas en Obsidian)
- `#contradiccion` — dos fuentes afirman cosas incompatibles. Describe ambas versiones.
- `#pendiente` — hueco de información conocido, algo por verificar o buscar.
- `#suposicion` — inferencia de Claude, no respaldada por fuente.
- `#obsoleto` — dato superado por una fuente más reciente; se conserva indicando qué lo superó.

### Reglas duras
1. **Nunca inventes datos, cifras, citas ni referencias.** Si no está en una fuente: o lo
   marcas `#suposicion`, o no lo escribes.
2. Nunca borres información contradictoria: se documentan las dos versiones y se marca
   `#contradiccion`.
3. Nunca edites `originales/`.
4. `log.md` es append-only: se añade al final, no se reescribe.
5. Al modificar una nota, actualiza su campo `actualizado`.
6. Si cambias una convención de este esquema (tipos, estados, etiquetas, nombres, flujos),
   actualiza `Manual de uso.md` en la misma sesión: es la versión que lee el usuario y las dos
   no pueden divergir.

---

## 4. Flujo: INGESTA (una fuente a la vez, supervisada)

Disparadores: "ingiere esto", "procesa este documento", "mete esto al wiki".

1. **Leer la fuente completa.** Documento en `originales/`, o URL (descárgala a
   `originales/web/AAAA-MM-DD-slug.md` con URL y fecha de consulta en el encabezado), o lo
   que el usuario dicte en la conversación.
2. **Conversar los hallazgos antes de escribir.** Presenta 5-10 puntos clave, qué conecta con
   lo que ya hay en el wiki, qué contradice y qué preguntas abre. Espera dirección del usuario
   sobre qué enfatizar. *Este paso no se salta.*
3. **Escribir la nota de fuente** en `wiki/fuentes/` con `plantillas/fuente.md`.
4. **Propagar al resto del wiki:** actualiza las páginas de concepto y entidad afectadas, crea
   las que falten, marca contradicciones con lo ya escrito, marca como `#obsoleto` lo superado.
   Una sola fuente suele tocar entre 5 y 15 páginas: esto es lo que hace que el wiki compile
   conocimiento en vez de acumular resúmenes sueltos.
5. **Actualizar `panorama.md`** si la fuente mueve la tesis vigente.
6. **Actualizar `index.md`** con las páginas nuevas.
7. **Añadir entrada al `log.md`** y reportar al usuario: páginas creadas, páginas modificadas,
   contradicciones nuevas, preguntas abiertas nuevas.

---

## 5. Flujo: CONSULTA

Disparador: cualquier pregunta sobre el material.

1. Lee `index.md` para ubicar las páginas relevantes; luego abre esas páginas. Si el índice no
   alcanza, `grep -ri "término" wiki/`.
2. Responde **con citas a las notas de fuente**, no de memoria. Si el wiki no tiene la
   respuesta, dilo explícitamente y propón qué fuente conseguir.
3. Si la respuesta tiene valor duradero (una comparativa, un análisis, una conexión nueva),
   **ofrece archivarla** en `wiki/sintesis/`. Una buena respuesta no debe morir en el chat:
   las exploraciones también componen el wiki.
4. Si se archiva: añádela a `index.md` y registra la consulta en `log.md`.

Formatos de respuesta según convenga: nota markdown, tabla comparativa, gráfica, artifact.
El formato no cambia la regla de citar.

---

## 6. Flujo: LINT (revisión de salud)

Disparador: "lint", "revisa el wiki".

Revisa y reporta; propón en vez de arreglar en silencio lo que sea opinable:

1. **Contradicciones** sin resolver: `grep -rn "#contradiccion" wiki/`
2. **Pendientes** acumulados: `grep -rn "#pendiente" wiki/`
3. **Datos obsoletos**: notas `estado: obsoleta` o con `#obsoleto` aún citadas como vigentes.
4. **Notas huérfanas** (sin enlaces entrantes) y **enlaces rotos** (apuntan a notas que no
   existen). Los enlaces rotos recurrentes indican conceptos que merecen página propia.
5. **Conceptos mencionados repetidamente sin página propia.**
6. **Notas estancadas**: `estado: semilla` sin tocar hace mucho.
7. **Vacíos de datos**: qué le falta a la investigación y qué fuente o búsqueda web lo llenaría.
8. Propón **preguntas nuevas que valdría la pena investigar**.

Cierra el lint con una entrada en `log.md`.

---

## 7. Formato de `index.md` y `log.md`

`index.md` está organizado por tipo. Cada línea:
`- [[Nombre de la nota]] — resumen en una línea` (las fuentes llevan además la fecha).

`log.md` es cronológico y **parseable**. Cada entrada empieza exactamente así:

```
## [AAAA-MM-DD] ingesta | Título de la fuente
## [AAAA-MM-DD] consulta | Pregunta resumida
## [AAAA-MM-DD] lint | Alcance
```

Bajo el encabezado, viñetas cortas: qué se hizo, páginas tocadas, hallazgos, preguntas nuevas.
Últimas entradas: `grep "^## \[" log.md | tail -5`.
