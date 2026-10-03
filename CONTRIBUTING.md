# Contributing · Cómo contribuir

## The one rule / La regla

**Everything is one file.** `index.html` has no build step, no package manager and no
bundler, and it must keep working when opened straight from disk (`file://`) or from a
shared drive. Any change that breaks that is out of scope.

**Todo es un solo archivo.** `index.html` no tiene compilación, ni gestor de paquetes, ni
empaquetador, y tiene que seguir funcionando abierto directamente desde el disco
(`file://`) o desde una unidad compartida. Cualquier cambio que rompa eso queda fuera.

## Before opening a pull request / Antes de abrir un pull request

1. Open `index.html` in a browser.
2. Run the test suite in the console and check that nothing fails:

   ```js
   window.__app.runSelfTest()
   ```

3. If you changed anything visible, add an assertion. The suite is the documentation of
   what the system promises.

## Things that will fail the suite on purpose / Cosas que la batería rechaza a propósito

- Translating the **code** (`AI: `, `+`, the two-letter codes). It is invariant by design.
- Leaving a dictionary key in one language and not the others.
- Changing an activity description without declaring the divergence from the source.
- Making the label height depend on the language.
- Removing the system name or the notation version from the label. A label with no
  system name cannot be interpreted when the QR code fails.
- Printing the **program** version on the label instead of the **notation** version.
  They are different numbers on purpose: see the «About» panel.
- Text overlapping, or content leaving the canvas.

## Vocabulary / Vocabulario

The nine activities come from the STM Association (2025) and are adopted without
redefining them. A change to a description is a change to the documented system, not a
wording tweak: it has to be declared in `DIVERGENCIAS_41` inside the test suite and
mirrored in the article that documents the system.
