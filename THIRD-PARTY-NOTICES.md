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
