# Third-party notices · Avisos de terceros

Nothing listed here is covered by the licences of this repository. Each item keeps its
own terms and is named here so that anyone redistributing the app knows what travels
with it.

Nada de lo que aparece acá queda cubierto por las licencias de este repositorio. Cada
elemento conserva sus propios términos y se nombra para que quien redistribuya la app
sepa qué viaja con ella.

---

## 1. Activity classification — STM Association

**STM Association (2025).** *Recommendations for a Classification of AI Use in Academic
Manuscript Preparation.*

The nine activities and their descriptions in English are reproduced from this source and
adopted **without redefining them**. Cited with attribution; no licence over this material
is claimed or granted.

The Spanish and Portuguese renderings of those descriptions are translations made for
this project and are covered by [CC BY 4.0](LICENSE-CONTENT.md). One of them departs from
a literal translation on purpose: `RF` reads «Ayuda en la recopilación y búsqueda de
referencias», because the English *gathering* covers locating the sources and
«recopilación» alone was narrower than the original. The departure is recorded in the
test suite.

## 2. QRious — QR code generation

- Author: Alasdair Mercer
- Licence: **GPL-3.0**
- Version: **4.0.2**, pinned in the URL
- Source: <https://github.com/neocotic/qrious>
- Loaded at runtime from `cdnjs.cloudflare.com`; **no QRious code is contained in this
  repository.**
- Loaded with **subresource integrity** (`sha512-…`). If the file served by the CDN ever
  differed by a single byte, the browser refuses to execute it and the app carries on
  without QR codes. The hash was computed from the actual file and matches the one
  cdnjs publishes.

This file links the library from a CDN; the browser combines them when the page runs.
Because the distributed HTML contains none of its code, the MIT licence of this
repository is not in conflict with the GPL of the library. This is a practical reading,
not legal advice.

Consequence to be aware of: **without a connection the QR code cannot be generated.**
The label still composes and the QR area comes out empty, as a square with a dashed
outline. The failure is not silent: the app shows a warning saying the library did not
load. The same happens if the integrity check fails.

## 3. Inter — typeface

- Author: Rasmus Andersson
- Licence: **SIL Open Font License 1.1 (OFL-1.1)**
- Version: **5.0.16** of the `@fontsource/inter` package, pinned in the URL; weights
  500, 600 and 700
- Source: <https://rsms.me/inter/>
- Loaded at runtime from `cdn.jsdelivr.net` and **embedded as base64 inside exported
  SVG files**, which the OFL expressly permits.

Anyone redistributing an exported SVG is redistributing an OFL font with it. The OFL
allows this; it does not allow selling the font on its own, and it requires that modified
versions not use the reserved font name.

## 4. Tool names — trademarks · Nombres de herramientas

The tools field suggests a list of frequent tool names so that the same tool is always
written the same way and the records can be compared. Those names are **trademarks of
their respective owners**. They are used nominatively, only to identify the tools
themselves. No affiliation with, or endorsement by, their owners is implied or claimed,
and no logos or other brand assets are reproduced anywhere in this repository.

The list is **not approved, exhaustive or exclusive**: a tool's absence rules nothing
out, and any other tool is typed by hand and counts exactly the same. The field uses an
open suggestion list, not a closed menu, precisely so that this stays true.

The CC BY 4.0 licence of this repository covers the texts written for this project. It
does **not** extend to those trademarks, which remain their owners'.

El campo de herramientas sugiere una lista de nombres frecuentes para que la misma
herramienta se escriba siempre igual y los registros se puedan comparar. Esos nombres son
**marcas de sus titulares** y se usan de forma nominativa, solo para identificar las
herramientas. No se implica ni se reclama afiliación ni respaldo de sus titulares, y en
este repositorio no se reproduce ningún logotipo ni otro elemento de marca.

La lista **no es aprobada, exhaustiva ni excluyente**: que una herramienta no esté no
excluye nada, y cualquier otra se escribe a mano y vale exactamente lo mismo. El campo usa
una lista de sugerencias abierta, y no un menú cerrado, precisamente para que eso siga
siendo cierto.

La licencia CC BY 4.0 de este repositorio cubre los textos escritos para este proyecto.
**No** se extiende a esas marcas, que siguen siendo de sus titulares.
