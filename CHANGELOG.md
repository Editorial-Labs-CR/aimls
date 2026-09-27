# Changelog

Versions are the `APP.version` value shown in the footer and in «About».
Las versiones son el valor `APP.version` que aparece en el pie y en «Acerca de».

## 21 — 2026-09-27

**El sistema pasa a llamarse AIMLS — AI Manuscript Labelling System.** El nombre propio y
su descriptor no se traducen: son la denominación oficial y se leen igual en todos los
idiomas. Sustituye a «AI Labelling System» / «Sistema de etiquetado AI».

The system is now named **AIMLS — AI Manuscript Labelling System**. The name and its
descriptor are not translated.

- El eje 2 deja de apoyarse en la palabra «componente», que la app nunca definía. Las
  cuatro etiquetas se sostienen solas y la guía de cada número **nombra lo que mide**:
  «de lo que se tradujo», «de las imágenes y figuras», «de las referencias». La
  aclaración de que la extensión es de la tarea y no del artículo queda donde hace
  falta: en la leyenda general, la nota y el manual.
- El título deja de decir «manuscritos científicos». El sistema sirve igual para una
  tesis o un informe técnico; «manuscrito» ya acota el alcance heredado de STM.
- Quien pide la declaración o fija el umbral deja de ser solo «la revista»: se unifica
  en **«la revista o entidad que publica o evalúa»**, que cubre editoriales,
  universidades y congresos.
- En español y portugués se explica que **AI** es la sigla inglesa de *artificial
  intelligence*, en su primera aparición.
- El selector de arriba deja de llamarse «Idioma de la herramienta» y pasa a
  **«Idioma de la pantalla»** (*Screen language*, *Idioma da tela*). Los dos selectores
  se entienden por oposición y «herramienta» no se oponía a nada: la etiqueta también
  la produce la herramienta. «Pantalla» contra «etiqueta y prosa» se entiende sin
  explicación. Cambia también en el manual, las preguntas frecuentes y «Acerca de».
- Ese selector **se ve como un control**: rótulo, globo y lista dentro de un solo
  recuadro. Antes era un rótulo gris diminuto junto a una lista suelta, encajonado
  entre dos botones, y pasaba desapercibido siendo el primer ajuste que se hace.
- El manual abre con un **índice interactivo**. Se arma leyendo los propios títulos de
  sección, así que no puede quedar desfasado, y salta dentro del diálogo sin mover la
  página de atrás.
- Imagen de vista previa regenerada con el nombre nuevo.

El repositorio pasa a llamarse **`aimls`**, en minúsculas. La dirección pública queda en
`editorial-labs-cr.github.io/aimls/`, que es la que viaja dentro del código QR de cada
etiqueta. Se cambia ahora, antes de publicar, porque una vez que haya etiquetas impresas
circulando esa dirección ya no se puede tocar sin romperlas.

Limpieza y endurecimiento, sin cambio visible:

- El script de terceros (QRious, desde cdnjs) se carga con **verificación de
  integridad**. Si ese archivo cambiara aunque fuera un byte, el navegador se niega a
  ejecutarlo y la app sigue funcionando sin código QR, en vez de ejecutar lo que
  llegue. El hash se calculó del archivo real y coincide con el que publica cdnjs.
- `applyLang` cae al inglés si recibe un idioma inexistente, en lugar de dejar la
  pantalla en blanco.
- Se elimina la regla `.sr-only`, muerta desde que el rótulo del selector es visible.
- Pruebas nuevas: el índice del manual en los tres idiomas, una guarda contra el nombre
  viejo del selector, comillas angulares y números de apartado sobre el texto ya
  renderizado (antes solo se miraban los diccionarios, y el manual se escapaba), la
  caída a inglés, y que el valor por defecto del QR y los tres metadatos de enlace
  apunten todos a la misma dirección. La batería pasa de 1312 a 1337.

Corrección: el commit de la versión 20 dejó `CITATION.cff` y el README en la 19, por un
error al rehacer los commits. Ambos quedan en la 21, coherentes con el resto.

Batería: **1311 aserciones con conexión**, con el bloque del QR omitido sin conexión.

## 20 — 2026-09-24

Cambios sobre la 19, que ya estaba publicada. Changes on top of the published 19.

- El **idioma de la etiqueta y la prosa se escoge primero**, en «Antes de empezar»; la URL
  del QR pasa a opciones de producción.
- Los dos ejes de idioma se distinguen en pantalla: «Idioma de la herramienta» arriba,
  «Idioma de la etiqueta y la prosa» abajo. El primero no tenía rótulo visible.
- **Se explica cuál es el umbral de declarabilidad**, que antes se nombraba sin definir:
  etiqueta «UMBRAL · OPCIONAL» junto a la actividad 1, nota junto a la lista de tareas,
  sección «Qué se declara y qué no» en el manual, y dentro de la propia prosa de N, que
  se publica con el artículo.
- La actividad 1 muestra en su fila los ejemplos y el «no incluye» de la lámina de STM,
  que es lo que la separa de la actividad 2.
- El **QR apunta a la app publicada**.
- Se declara la **codificación asistida por IA** con la fórmula de las demás herramientas
  del autor.
- Metadatos de vista previa (Open Graph, Twitter Card) e imagen de 1200×630 para
  compartir el enlace. El `<title>` del archivo llevaba el nombre anterior del sistema.
- Redacción: comillas dobles, sin guiones largos haciendo de paréntesis, sin siglas sin
  explicar y sin números de sección del artículo en el texto visible.

Correcciones / fixes:

- Dos casos de la batería usaban el código `GE`, retirado en favor de `TG`: se ignoraban
  en silencio y no probaban lo que decían probar.
- La batería se detenía **sin conexión** al comprobar los avisos del QR. Ahora el bloque
  que depende de la librería se **omite**, se informa en el registro y el resto termina.

Batería: **1299 aserciones con conexión · 1290 sin conexión**, con un bloque omitido.
La cifra de la entrada 19 (1282) era la correcta en su momento y se deja como está.

## 19 — 2026-09-23 · first public release / primera publicación

Versions 1–18 were internal iterations and are not published.
Las versiones 1–18 fueron iteraciones internas y no se publican.

State at first release / Estado en la primera publicación:

- Label and prose generated from a single declarative act, verified to agree on 600
  reconstructed cases.
- Two language axes: interface language and label language, independent of each other.
  The **code is invariant in English** in both; only the descriptions follow the label
  language. Spanish and English offered; Portuguese translated and tested but held back
  pending review by a native speaker (`LANGS` in the source).
- Constant label height across languages, so labels align on a page.
- Content-driven width from measured text; no magic numbers.
- Optional extent axis, optional tools and models, reserved space for a future third axis.
- QR guard against the silent truncation of the QR library past its capacity.
- Test suite of 1282 assertions, run with `window.__app.runSelfTest()`.

Known limitations / Limitaciones conocidas:

- The QR points to the published app itself. A journal that adopts the system will
  normally replace it with its own editorial policy page. A printed QR cannot be revoked,
  so check the address before going to print.
- The QR needs a connection: the library is loaded from a CDN.
- One description departs on purpose from the preprint that documents the system (`RF`);
  the divergence is declared in the test suite.
