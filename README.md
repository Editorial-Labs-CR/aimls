# AIMLS

**AI Manuscript Labelling System**

Graphic declaration of artificial intelligence use in manuscripts.
Declaración gráfica de uso de inteligencia artificial en manuscritos.

**[▶ Open the app / Abrir la app](https://editorial-labs-cr.github.io/aimls/)**

Unidad de Ciencia Abierta · **Vicerrectoría de Investigación**
Universidad Estatal a Distancia (UNED), Costa Rica

[![Licence: MIT](https://img.shields.io/badge/code-MIT-black.svg)](LICENSE)
[![Licence: CC BY 4.0](https://img.shields.io/badge/content-CC%20BY%204.0-black.svg)](LICENSE-CONTENT.md)

---

## English

### What it is

A tool that turns a single declarative act into a **graphic label** that can be placed
on a prominent page of an article, and into a **prose declaration** ready to paste into
the manuscript. Both come from the same input, so they cannot contradict each other.

```
AI: ED+TR+CO          the declared tasks
AI: ED:1+TR:3+CO:2    the same, with the extent of each one
AI: N                 no use above the disclosable threshold
```

The label **does not replace** the prose declaration the journal or publishing body
asks for: it accompanies it, so the record is comparable across articles, aggregable at
scale and transportable as metadata.

It is an open notation system, **proposed for any journal or publishing body**. Adoption
is gradual and does not require changing current policies.

### Vocabulary

Built on the nine activities of the STM Association (2025), *Recommendations for a
Classification of AI Use in Academic Manuscript Preparation*. The activities are adopted
**without redefining them**: eight are disclosable and the ninth is not, because the STM
guidelines recommend prohibiting it. The scope is that of the source: manuscript
preparation only, not the rest of the research process.

| Code | From | STM | Activity |
|------|------|-----|----------|
| `N`  | No use | — | No use above the disclosable threshold |
| `ED` | Editing | 1 | Refinement, correction, editing or formatting the manuscript to improve clarity of language |
| `TG` | Text Generation | 2 | Writing or drafting manuscript content |
| `TR` | Translation | 3 | Translation of manuscript text for the purpose of publishing |
| `DA` | Data | 4 | Refining or formatting of data reported in the manuscript |
| `IM` | Images | 5 | Generation, refinement, correction, editing or formatting of images, diagrams or other figures for illustrative purposes only |
| `VI` | Visualisations | 6 | Generation, refinement, correction, editing or formatting of visualisations of research data or results |
| `CO` | Code | 7 | Refinement or formatting of code reported in the submitted manuscript |
| `RF` | References | 8 | Assisting with gathering references |

**What gets declared.** Activities **2 to 8** always, however little they were used.
Activity **1** (spell checker, grammar, style) need not be: that is the threshold, set
by the 2023 STM Guidelines. If you used it alongside other activities, simply leave it unticked. If there was
nothing above it at all, the correct declaration is `AI: N`, which is exclusive and states
not that no tool was used but that none was used above the threshold. A journal or publishing body may set its threshold lower, and `ED` stays available for that.

A second, **optional** axis records the extent of each use: 1 incidental (<¼),
2 partial (¼–½), 3 majority (½–¾), 4 total (>¾). Omitting it is a valid declaration.
Human verification is not a level: it is a single statement covering everything declared.

### The code is never translated

`AI`, the `+` separator and the two-letter codes are **always in English**, in every
interface language. That is the whole point of a code: two articles declaring the same
use must produce the same string, in any country, so that it can be searched, compared
and aggregated. What *does* follow the label language is the natural-language text
inside the label, and the prose declaration.

The tool has **two independent language controls**: "Screen language", at the top,
changes what you see while working; "Label and prose language", further down, is the
language of the article and is what gets printed. An editor can work in one language and
publish in another.

### Running it

It is a **single HTML file with no build step**. Open `index.html` in a browser, or host
it anywhere static. It works from `file://` and from a shared drive.

Two dependencies load from a CDN: QRious (QR codes) and the Inter typeface. Without a
connection the label still composes, but the QR comes out empty and the system font is
used.

The test suite runs from the browser console:

```js
window.__app.runSelfTest()
```

### How to cite

> Chinchilla Serrano, A. (2026). *AIMLS: AI Manuscript Labelling System* (Version 21) [Computer software].
> Open Science Unit, Office of the Vice-Rector for Research, Universidad Estatal a
> Distancia. https://github.com/Editorial-Labs-CR/aimls

GitHub also reads [`CITATION.cff`](CITATION.cff).

### Licences

Two licences, each for what it was designed for. See [LICENSE](LICENSE),
[LICENSE-CONTENT.md](LICENSE-CONTENT.md) and
[THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

- **Code — MIT.** The HTML, CSS and JavaScript.
- **Content — CC BY 4.0.** The notation, the texts, the user guide, the label design and
  the logo.

Both live inside the same file; the boundary is explained in `LICENSE-CONTENT.md`.
The STM classification is third-party material, cited with attribution and **not**
covered by either licence.

---

## Español

### Qué es

Una herramienta que convierte un solo acto declarativo en una **etiqueta gráfica** para
colocar en una página destacada del artículo y en una **declaración en prosa** lista para
pegar en el manuscrito. Las dos salen de la misma captura, así que no pueden
contradecirse.

```
AI: ED+TR+CO          las tareas declaradas
AI: ED:1+TR:3+CO:2    lo mismo, con la extensión de cada una
AI: N                 sin uso por encima del umbral declarable
```

La etiqueta **no sustituye** la declaración en prosa que pide la revista o entidad
editora: la acompaña, para que el dato sea comparable entre artículos, agregable en
conjuntos grandes y transportable como metadato.

Es un sistema de notación abierto, **propuesto para cualquier revista o entidad
editora**. La adopción es gradual y no exige modificar las políticas vigentes.

### Vocabulario

Construido sobre las nueve actividades de STM Association (2025), *Recommendations for a
Classification of AI Use in Academic Manuscript Preparation*. Las actividades se adoptan
**sin redefinirlas**: ocho son declarables y la novena no, porque las guías de STM
recomiendan prohibirla. El alcance es el de la fuente: solo la preparación del
manuscrito, no el resto del proceso de investigación.

| Código | Viene de | STM | Actividad |
|--------|----------|-----|-----------|
| `N`  | No use (sin uso) | — | Sin uso por encima del umbral declarable |
| `ED` | Editing (edición) | 1 | Refinamiento, corrección, edición o formato del manuscrito para mejorar la claridad del lenguaje |
| `TG` | Text Generation (generación de texto) | 2 | Escritura o redacción de contenido del manuscrito |
| `TR` | Translation (traducción) | 3 | Traducción del texto del manuscrito con fines de publicación |
| `DA` | Data (datos) | 4 | Refinamiento o formato de los datos reportados en el manuscrito |
| `IM` | Images (imágenes) | 5 | Generación, refinamiento, corrección, edición o formato de imágenes, diagramas u otras figuras únicamente con fines ilustrativos |
| `VI` | Visualisations (visualizaciones) | 6 | Generación, refinamiento, corrección, edición o formato de visualizaciones de datos o resultados de investigación |
| `CO` | Code (código) | 7 | Refinamiento o formato del código reportado en el manuscrito enviado |
| `RF` | References (referencias) | 8 | Ayuda en la recopilación y búsqueda de referencias |

**Qué se declara.** Las actividades **2 a 8** siempre, por poco que se hayan usado. La
**1** (corrector, gramática, estilo) no hace falta: ese es el umbral, fijado por las guías
de STM de 2023. Si la usó junto con otras actividades, basta con dejarla sin marcar. Si no hubo nada por
encima en absoluto, la declaración correcta es `AI: N`, que es excluyente y no dice que no
se usara ninguna herramienta sino que no se usó ninguna por encima del umbral.
Una revista o entidad editora puede situar su umbral más abajo, y para eso `ED` sigue disponible.

Un segundo eje, **opcional**, registra la extensión de cada uso: 1 puntual (<¼),
2 parcial (¼–½), 3 mayoritaria (½–¾), 4 total (>¾). Omitirlo es una declaración válida.
La verificación humana no es un nivel: es una afirmación única que cubre todo lo
declarado.

### El código no se traduce

`AI`, el separador `+` y los códigos de dos letras van **siempre en inglés**, sea cual
sea el idioma de la interfaz. Esa es la razón de ser de un código: dos artículos que
declaran el mismo uso tienen que producir la misma cadena, en cualquier país, para que
se pueda buscar, comparar y agregar. Lo que *sí* sigue al idioma de la etiqueta es el
texto en lengua natural que va dentro, y la prosa de la declaración.

La herramienta tiene **dos controles de idioma independientes**: "Idioma de la
pantalla", arriba, cambia lo que se ve mientras se trabaja; "Idioma de la etiqueta y la
prosa", más abajo, es el idioma del artículo y es el que se imprime. Una persona editora
puede trabajar en una lengua y publicar en otra.

### Cómo se usa

Es un **archivo HTML único, sin compilación**. Se abre `index.html` en un navegador o se
aloja en cualquier servidor estático. Funciona desde `file://` y desde una unidad
compartida.

Dos dependencias se cargan desde CDN: QRious (códigos QR) y la tipografía Inter. Sin
conexión la etiqueta se compone igual, pero el QR sale vacío y se usa la fuente del
sistema.

La batería de pruebas se ejecuta desde la consola del navegador:

```js
window.__app.runSelfTest()
```

### Cómo citar

> Chinchilla Serrano, A. (2026). *AIMLS: AI Manuscript Labelling System* (Versión 21) [Software].
> Unidad de Ciencia Abierta, Vicerrectoría de Investigación, Universidad Estatal a
> Distancia. https://github.com/Editorial-Labs-CR/aimls

### Licencias

Dos licencias, cada una para lo que fue pensada. Ver [LICENSE](LICENSE),
[LICENSE-CONTENT.md](LICENSE-CONTENT.md) y
[THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

- **Código — MIT.** El HTML, el CSS y el JavaScript.
- **Contenido — CC BY 4.0.** La notación, los textos, el manual, el diseño de la etiqueta
  y el logotipo.

Las dos conviven en el mismo archivo; el límite se explica en `LICENSE-CONTENT.md`.
La clasificación de STM es material de terceros, citado con atribución y **no** cubierto
por ninguna de las dos.

---

## Autoría · Authorship

**Alexander Chinchilla Serrano** · [ORCID 0000-0001-9465-1522](https://orcid.org/0000-0001-9465-1522) · <fchinchillas@uned.ac.cr>
Unidad de Ciencia Abierta, Vicerrectoría de Investigación
Universidad Estatal a Distancia (UNED), Costa Rica

**Codificación · Coding:** Claude Opus 5 (Anthropic) — identificador del modelo
`claude-opus-5` — bajo instrucción, criterio y experiencia editorial humana / under human
editorial instruction, judgement and experience.
