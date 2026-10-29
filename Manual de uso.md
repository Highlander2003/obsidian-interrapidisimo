---
tipo: sintesis
estado: estable
creado: 2026-09-19
actualizado: 2026-10-29
tags: [meta]
---

# Manual de uso

Cómo se usa esta bóveda: Obsidian del lado tuyo, Claude del lado del teclado, y las
convenciones que hacen que las dos cosas encajen. Si solo vas a leer una sección, lee
[[#3. Diccionario de indicativos]] y [[#4. Comandos para Claude]].

El esquema formal —las instrucciones que yo obedezco— está en `CLAUDE.md`. Este manual es su
traducción para humanos, más lo que `CLAUDE.md` no cubre: cómo moverte por Obsidian.

---

## 1. Qué es esta bóveda en treinta segundos

No es una carpeta de documentos ni un buscador sobre PDF. Es un **wiki que se compila**: cada
fuente que entra se lee una vez, se integra al conocimiento existente y actualiza todo lo que
la contradice o la refuerza. La próxima pregunta no vuelve a partir de cero.

Tres capas, con dueños distintos:

| Capa | Carpeta | Quién escribe | Qué pasa si se rompe |
|---|---|---|---|
| Originales | `originales/` | Tú (o yo al bajar una web) | Se pierde la verdad de referencia. **Inmutable**: nunca los edito. |
| Wiki | `wiki/` + notas de raíz | **Yo** | Se puede reconstruir desde los originales. Por eso puedo reescribirlo sin miedo. |
| Esquema | `CLAUDE.md` | Los dos, hablando | Yo dejo de ser mantenedor y vuelvo a ser un chatbot genérico. |

Tu trabajo: conseguir fuentes, dirigir el foco, hacer preguntas. El mío: resumir, conectar,
archivar, detectar contradicciones y mantener el índice y el log.

---

## 2. Obsidian: lo que de verdad necesitas

### El patrón de trabajo

Obsidian a un lado de la pantalla, la terminal con Claude al otro. Yo edito, tú ves los
cambios aparecer en vivo: Obsidian recarga el archivo solo. Obsidian es el IDE, yo soy el
programador, el wiki es el código.

### Atajos que se usan a diario

| Atajo | Para qué |
|---|---|
| `Ctrl+O` | Abrir cualquier nota escribiendo su nombre. **El atajo más útil de todos.** |
| `Ctrl+Shift+F` | Buscar en toda la bóveda (la sintaxis está en la sección 7) |
| `Ctrl+F` | Buscar dentro de la nota abierta |
| `Ctrl+P` | Paleta de comandos: todo lo que Obsidian sabe hacer |
| `Ctrl+E` | Alternar entre editar y leer |
| `Ctrl+G` | Vista de grafo |
| `Ctrl+clic` en un enlace | Abrirlo en un panel nuevo, al lado |
| `Alt+←` / `Alt+→` | Atrás y adelante, como en el navegador |
| `Ctrl+N` | Nota nueva (normalmente no la necesitas: las creo yo) |

### Los cuatro paneles que importan

- **Explorador de archivos** — el árbol de carpetas. Útil para ver el volumen, poco para navegar.
- **Vínculos entrantes (backlinks)** — al final de cada nota: *quién la cita*. Aquí se ve el
  valor del wiki: abres un concepto y descubres las cuatro fuentes que lo tocan.
- **Etiquetas** — el tablero de control real. Un clic en `#pendiente` o `#contradiccion` te
  muestra todo lo que está sin cerrar.
- **Esquema (outline)** — los encabezados de la nota abierta; sirve en las notas largas
  como `panorama` o `Preguntas abiertas`.

### Vista de grafo: cómo leerla

Cada punto es una nota, cada línea un enlace. Sirve para dos diagnósticos rápidos:

- **Puntos sueltos, sin líneas** → notas huérfanas: nadie las cita, probablemente están
  muertas o mal integradas.
- **Puntos grises o tenues** → enlaces a notas que todavía no existen. En este wiki eso **no
  es un error**: es una lista de deseos, marca conceptos que se mencionan tanto que merecen
  página propia. Cuando veas uno repetido, pídeme que lo cree.

**Colores** (grupos ya configurados): azul = fuentes · verde = conceptos · naranja =
entidades · rojo = preguntas · morado = síntesis · gris oscuro = notas raíz (`panorama`,
`index`, este manual).

**Qué no aparece** (filtro guardado): `privado/`, `originales/`, `Clippings/`, `plantillas/`,
`log.md` y el canvas. El log enlaza casi todo y convertía el grafo en una madeja; lo privado
no debe mezclarse con el wiki. Las flechas muestran la dirección: quién cita a quién.

### Enlaces `[[así]]`

Todo lo que va entre dobles corchetes es un enlace a otra nota. Obsidian los resuelve por
nombre de archivo sin importar la carpeta, por eso las carpetas importan poco y los nombres
importan mucho. Si pasas el mouse por encima con `Ctrl`, ves la nota sin abrirla.

### Propiedades (el bloque de arriba)

El recuadro `---` del principio de cada nota son sus propiedades: `tipo`, `estado`, `creado`,
`actualizado`, `tags`. Obsidian las muestra como una tabla editable. **No las borres**: son
lo que me permite filtrar, y lo que el lint usa para encontrar notas estancadas.

### Plantillas

Ya está configurado: `Ctrl+P` → *Insertar plantilla* usa la carpeta `plantillas`. En la
práctica las uso yo al crear notas; tú solo las necesitas si escribes una a mano.

---

## 3. Diccionario de indicativos

Todo lo que verás marcado en una nota y qué significa exactamente.

### `tipo` — qué clase de nota es

| Tipo | Vive en | Contiene | Ejemplo vivo |
|---|---|---|---|
| `fuente` | `wiki/fuentes/` | Resumen y extracción de **una** fuente. Nunca opinión mía sin marcar. | [[2026-09-19 Plan de integracion de correcciones]] |
| `concepto` | `wiki/conceptos/` | Una idea, mecanismo o método, con la evidencia de varias fuentes. | [[Trazabilidad por puntos de control]] |
| `entidad` | `wiki/entidades/` | Algo concreto: persona, organización, lugar, artefacto. | [[Libro de Excel de despacho]] |
| `pregunta` | `wiki/preguntas/` | Un hueco de conocimiento con su respuesta provisional y qué la cerraría. | [[Uso real del prototipo en la sucursal]] |
| `sintesis` | `wiki/sintesis/` y raíz | Comparativas, análisis y respuestas archivadas. | [[panorama]] |

### `estado` — madurez de la nota

| Estado | Significa |
|---|---|
| `semilla` | Existe el título y poco más. Creada porque algo la citó. |
| `en-desarrollo` | Tiene contenido con citas, pero se espera que crezca con las próximas fuentes. |
| `estable` | Cubierta por suficientes fuentes; cambia solo si algo la contradice. |
| `obsoleta` | Superada. **No se borra**: se conserva indicando qué la reemplazó. |

### `fiabilidad` (solo en fuentes) — cuánto peso tiene lo que dice

`alta` documento oficial o primario · `media` secundario o interno sin verificar ·
`baja` indicio, borrador o material sin respaldo. Cuando dos fuentes chocan, esta propiedad
decide cuál pesa más.

### `origen` (solo en fuentes)

`documento` (archivo en `originales/documentos/`) · `web` (copia en `originales/web/` con URL
y fecha) · `conversacion` (algo que me dictaste; no tiene archivo original).

### Etiquetas de control — las cuatro que leerás a diario

| Etiqueta | Qué significa | Qué hacer cuando la veas |
|---|---|---|
| `#contradiccion` | Dos afirmaciones incompatibles, ambas documentadas. Nunca borro una para que cuadre. | Decidir cuál vale, o conseguir la fuente que lo resuelva |
| `#pendiente` | Hueco conocido: falta un dato, una verificación o una fuente. | Es tu lista de tareas de investigación |
| `#suposicion` | **Inferencia mía, sin respaldo de fuente.** | Tratarla como opinión, no como dato. Si el jurado pregunta, esto es lo que no puedes citar |
| `#obsoleto` | Dato superado por material más reciente, conservado por trazabilidad. | Verificar que nada lo siga citando como vigente |

Ver todas las de un tipo: clic en la etiqueta, o `Ctrl+Shift+F` → `tag:#pendiente`.

### Citas — cómo se lee la evidencia

```
El margen cayó 4 puntos ([[2026-09-19 Informe anual]], p. 12).
```

La regla que sostiene todo el wiki: **toda afirmación no trivial lleva su fuente y su
página.** Si encuentras una afirmación sin cita y sin `#suposicion`, es un defecto: dímelo y
la corrijo o la retiro.

### Nombres de archivo

- Fuentes: `AAAA-MM-DD Título corto` — ordenan solas por fecha.
- Conceptos y entidades: nombre natural en singular.
- Preguntas: enunciado afirmativo, **sin signos de interrogación**.
- Windows prohíbe en nombres: `? : * " < > | \ /` — por eso las preguntas no llevan `¿?`.

---

## 4. Comandos para Claude

No hay sintaxis especial: son frases. Lo que importa es el verbo, porque cada uno dispara un
flujo distinto descrito en `CLAUDE.md`.

### Ingesta — meter material al wiki

| Le dices | Yo hago |
|---|---|
| «ingiere `originales/documentos/X.pdf`» | Lo leo entero, **te comento los hallazgos y espero tu visto bueno**, luego escribo la nota de fuente y propago a conceptos, entidades y preguntas |
| «ingiere esta URL: …» | La descargo a `originales/web/` con fecha de consulta y sigo el mismo flujo |
| «anota esto: …» / «esto me lo dijo el tutor: …» | Creo una nota de fuente con `origen: conversacion` |
| «ingiere estos tres, sin pararte» | Proceso en lote y reporto al final (modo no supervisado, bajo tu orden explícita) |

El paso de conversar antes de escribir no se salta salvo que me lo pidas: es donde tú
decides qué se enfatiza.

### Consulta — preguntar al wiki

| Le dices | Yo hago |
|---|---|
| «¿qué dice el wiki sobre X?» | Busco, leo las páginas y respondo **con citas**. Si no está, lo digo en vez de inventarlo |
| «compara A y B» | Tabla comparativa con la fuente de cada celda |
| «archiva esa respuesta» | La guardo en `wiki/sintesis/`, la indexo y la registro en el log |
| «¿en qué me estoy apoyando sin evidencia?» | Barrido de `#suposicion` y de afirmaciones sin cita |

Las buenas respuestas no deberían morir en el chat: cuando una valga la pena, te ofrezco
archivarla, pero puedes pedirlo tú.

### Lint — revisar la salud del wiki

| Le dices | Yo reviso |
|---|---|
| «lint» | Todo: contradicciones, pendientes, obsoletos, huérfanas, enlaces rotos, notas estancadas, vacíos de datos, y te propongo preguntas nuevas |
| «lint de contradicciones» | Solo ese frente |
| «¿qué le falta al wiki?» | Vacíos de evidencia y qué fuente los llenaría |

Ritmo razonable: cada 5–10 fuentes, o antes de una entrega.

### Mantenimiento y esquema

| Le dices | Yo hago |
|---|---|
| «actualiza el índice» | Reconcilio `index.md` con lo que hay en disco |
| «registra en el log lo que hicimos» | Entrada nueva con el formato parseable |
| «marca X como obsoleto porque Y» | Cambio estado, añado `#obsoleto` y anoto qué lo reemplazó |
| «saca esto a nota propia» | Promuevo una sección a nota y arreglo los enlaces |
| «cambia la convención de … en CLAUDE.md» | Edito el esquema; rige de ahí en adelante |

---

## 5. Reglas

### Lo que yo nunca hago

1. **Inventar** datos, cifras, citas o referencias. Sin fuente: o va marcado `#suposicion`, o
   no se escribe.
2. **Tocar `originales/`.** Solo lectura.
3. **Borrar una contradicción** para que el relato quede limpio.
4. **Reescribir el log.** Es append-only.
5. **Afirmar sin citar.**

### Lo que conviene que tú hagas

- **Renombrar y mover notas desde Obsidian**, nunca desde el Explorador de Windows: Obsidian
  actualiza todos los enlaces; Windows los rompe en silencio.
- **Dejar los originales quietos** en `originales/`. Si una versión cambia, entra como archivo
  nuevo con su fecha; no se sobrescribe la anterior.
- **Escribir tú una nota es válido**, pero ponle `autor: usuario` en las propiedades: así no la
  reescribo, solo le añado enlaces o una sección `## Notas de Claude` al final.
- **Cuestionarme.** Si una afirmación te suena rara, pídeme la cita: si no la tengo, es un
  defecto que hay que corregir.

---

## 6. Rutina sugerida

**Al abrir una sesión conmigo:** no hace falta ponerme al día, leo `CLAUDE.md`, `index.md` y
las últimas entradas del log. Si vamos a trabajar en la plataforma, también leo
`privado/Punto de continuación.md`, que resume su estado y los pendientes. Basta con que me digas qué quieres hacer hoy.

**Durante:** una fuente a la vez. Ingerir dos seguidas sin revisar la primera es la forma más
rápida de llenar el wiki de resúmenes sueltos en vez de conocimiento integrado.

**Al cerrar:** «registra en el log lo que hicimos». Toma diez segundos y es lo que permite
retomar dentro de tres semanas sin releer nada.

**Cada 5–10 fuentes:** un lint.

---

## 7. Búsquedas útiles

En Obsidian (`Ctrl+Shift+F`):

| Búsqueda | Encuentra |
|---|---|
| `tag:#pendiente` | Todo lo que falta por resolver |
| `tag:#contradiccion` | Los choques sin decidir |
| `tag:#suposicion` | Lo que no puedes citar como evidencia |
| `[tipo:concepto]` | Todas las notas de un tipo (búsqueda por propiedad) |
| `[estado:semilla]` | Notas que se quedaron a medias |
| `path:wiki/fuentes` | Solo las notas de fuente |
| `"línea base"` | Frase exacta |
| `despacho -tag:#obsoleto` | Un término, excluyendo lo superado |

Las mismas preguntas, hechas a mí, devuelven además el porqué y las conexiones. La búsqueda
de Obsidian te dice *dónde aparece*; yo te digo *qué significa*.

---

## 8. Cuando algo sale raro

**Aparece una nota vacía con nombre de plantilla** (ejemplo real: `AAAA-MM-DD Fuente.md` en la
raíz). Pasa al hacer clic en un enlace de ejemplo dentro de una plantilla: Obsidian crea la
nota al vuelo. Se borra sin consecuencias; los enlaces de las plantillas son ilustrativos.

**Un enlace se ve gris o tenue.** Apunta a una nota que no existe. No es error: es una
candidata a página nueva. Si se repite, pídemela.

**Borraste una nota que otras citaban.** Quedan enlaces rotos. Un lint los encuentra todos.

**No puedes crear una nota con cierto nombre.** Lleva alguno de los caracteres que Windows
prohíbe: `? : * " < > | \ /`.

**Cambiaste algo a mano y quieres que lo respete.** Ponle `autor: usuario` en las propiedades.

**Quieres deshacer algo que escribí.** Obsidian guarda versiones: `Ctrl+P` → *Recuperación de
archivos*. Y si me lo pides, reconstruyo la nota desde la fuente original: el wiki es
derivable, ese es justamente el punto de mantener `originales/` intacto.

---

## 9. Mapa de la bóveda

```
CLAUDE.md          el esquema que yo obedezco (léelo si quieres cambiar cómo trabajo)
Manual de uso.md   esta nota
index.md           catálogo de todo el wiki, por tipo
log.md             qué pasó y cuándo, append-only
panorama.md        EMPIEZA AQUÍ: pregunta de investigación, tesis vigente y qué la debilita

originales/        fuentes intactas: documentos/ y web/
wiki/
  fuentes/         una nota por fuente ingerida
  conceptos/       ideas y mecanismos
  entidades/       personas, organizaciones, artefactos, lugares
  preguntas/       huecos de conocimiento, con Preguntas abiertas como lista viva
  sintesis/        comparativas y respuestas archivadas
plantillas/        estructura de cada tipo de nota
privado/           credenciales y datos sensibles (tipo `privado`); no forma parte del wiki
```

Las cuatro notas meta, en una línea cada una:

- [[panorama]] — dónde está la investigación hoy y con cuánta confianza.
- [[index]] — todo lo que existe, con un resumen por página.
- [[log]] — la historia: `grep "^## \[" log.md | tail -5` da las últimas cinco entradas.
- [[Preguntas abiertas]] — lo que falta, ordenado por lo que bloquea.
