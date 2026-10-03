# Changelog

Versions are the `APP.version` value shown in the footer and in «About».
Las versiones son el valor `APP.version` que aparece en el pie y en «Acerca de».

## 27 — 2026-10-03

**La etiqueta dice de qué sistema es, y la prosa dice quién la hizo.** Hasta ahora no lo
decía ninguna de las dos. Una etiqueta sin nombre de sistema es huérfana: si el código QR
se rompe, se recorta al imprimir o el PDF va sin enlaces, quien encuentre `AI: ED+TR` en
un artículo no tiene cómo saber qué notación es eso.

- **En la etiqueta**, arriba a la izquierda, dentro de la tarjeta: `AIMLS 1.0 ·
  Declaración de uso de IA`. El nombre y la versión son invariantes, como el código; el
  descriptor sigue el idioma de la etiqueta. No crece la etiqueta: vive en el hueco que
  ya había sobre el icono.
- **En la prosa**, como frase de cierre: «Las personas autoras elaboraron esta
  declaración con AIMLS 1.0 (AI Manuscript Labelling System), disponible en […]». La
  prosa viaja aparte dentro del manuscrito, así que necesita su propia procedencia.

**Dos números de versión, y no son lo mismo.** La **versión del programa** se mueve con
cada cambio, por pequeño que sea: ayer pasamos de la 25 a la 26 por cambiar un botón. La
**versión de la notación** es el sistema de códigos y reglas de composición, y solo se
mueve si esas cambian. En la etiqueta se imprime la de la notación, que arranca en `1.0`.

Si imprimiéramos la del programa, dos artículos que declaran exactamente lo mismo
llevarían números distintos por haber cambiado un botón, y eso es lo contrario de
comparable, que es la razón de ser del sistema. «Acerca de» explica la diferencia.

**La línea se mide y se encoge sola.** Con ocho tareas la cadena canónica baja mucho por
la izquierda y en español llegaba a solaparse. Ahora el cuerpo baja hasta 7,5 y, si ni
así cabe, se queda el nombre y la versión, que es lo que no puede faltar. Comprobado en
doce combinaciones de idioma y contenido: margen mínimo positivo y el alto sin cambiar.

**La prosa decía «extensión».** La unificación a «nivel de uso» de la versión 26 no llegó
ahí, y la prosa es justo lo que se pega en el manuscrito. Corregido con dos puntos,
«(nivel de uso: mayoritaria)», porque los grados son femeninos por concordar con
«extensión» y un cambio directo habría producido «nivel de uso mayoritaria».

Manual, «Acerca de», README y `CONTRIBUTING.md` documentan lo nuevo en los tres idiomas.

**Corrección dentro de la misma versión.** El párrafo que explica los dos números de
versión quedó insertado entre la línea de versión y la frase que dice qué es la
herramienta, así que «Acerca de» abría explicando numeración antes de decir para qué
sirve. Ahora el dato va en la línea de arriba, `AIMLS · versión 27 · notación 1.0 ·
fecha`, y la explicación bajo «Cómo citar», que es donde esos números se usan.

Ninguna prueba lo vio, porque todas comprobaban que los textos **existieran**, no dónde
estaban. Se añaden dos guardas: que «Acerca de» y el manual tengan la misma estructura en
los tres idiomas, y que «Acerca de» abra por su orden, título, versión y qué es, sin nada
intercalado. Comprobado que se ponen en rojo con un párrafo intruso en esa posición.

Batería: **1446 aserciones con conexión · 1437 sin conexión**, con un bloque omitido.

## 26 — 2026-09-29

**El control de extensión era confuso y lo dijo una estudiante.** Había un guion en la
primera casilla de cada actividad, y un guion es un símbolo que hay que aprender. Peor:
puesto en fila con los números se leía como «nivel cero», que es lo que significa `N` y
no lo que significaba ese guion. Ahí la confusión dejaba de ser estética.

- El botón dice **«omitir»**. En la etiqueta impresa nunca hubo guion, así que esto no
  toca la notación.
- La columna va **enmarcada bajo un rótulo que dice «opcional»**, una sola vez en vez de
  repetirlo en las ocho filas. El rótulo es la tapa del recuadro y mide exactamente lo
  que la columna; hay una prueba que lo comprueba, porque si se descuadra se ve roto.
- El rótulo va **debajo de la fila de N**, que no tiene niveles: encima quedaba colgando
  sobre una columna vacía.
- La guía flotante explica que es una decisión: «Elige no declarar qué parte de esta
  actividad hizo la inteligencia artificial. Esta opción también es válida.»

**Un solo nombre para el eje 2.** Se llamaba «extensión» en la columna y en la nota, y
«nivel de uso» en las preguntas frecuentes: dos nombres para lo mismo, que es la
ambigüedad que este sistema existe para evitar. Ahora todo dice **nivel de uso**, incluida
la etiqueta impresa, y hay una guarda que impide que el término viejo vuelva.

El motivo de elegir ese nombre y no el otro: en contexto editorial «extensión» significa
largo, «la extensión del artículo». Quien se encontrara la etiqueta impresa sin conocer
el sistema podía leer «EXTENSIÓN NO DECLARADA» como «no declararon cuán largo es», que es
un sentido falso y verosímil.

**«Opcional» no significa que nadie se lo vaya a pedir.** La app lo repetía en cuatro
sitios sin aclarar nunca que la revista puede exigirlo, así que alguien podía omitir y
que se lo devolvieran. Ahora dice, donde se decide y en el manual: «Es opcional, a menos
que la revista o entidad que publica le pida que indique el nivel de uso. En ese caso
debe indicarlo.»

**El aviso de nivel no declarado se dibuja un punto y medio más pequeño** que la cadena
canónica: es una nota sobre lo que falta, no el dato. Se dibuja más pequeño pero **se
sigue midiendo al tamaño normal**, porque la altura de la etiqueta sale de una cadena de
referencia a ese cuerpo y medirla pequeña habría roto el alto constante de 196.

**Las referencias cruzadas a las actividades se pueden seguir.** La explicación de `ED`
decía «eso es la actividad 2» mientras la fila decía «STM 2»: dos maneras de nombrar lo
mismo. Ahora dice «eso es **TG**, la actividad 2», y el manual abre atando los números
con los distintivos que se ven en pantalla.

**Portugués menos europeo.** «pedir-lhe», «lho peça» y «carregar em» se cambiaron por
formas que se entienden en los dos lados del Atlántico. Sigue sin revisar por hablante
nativo y sigue sin ofrecerse en el selector.

**En celular**, la columna de botones le robaba 34 píxeles a la descripción de la tarea.
Por debajo de 560 de ancho los botones bajan a su propia línea y el texto recupera el
ancho completo. El bloque queda algo más alto, y se desplaza un poco más: es el precio de
no tener texto en una columna de 82 píxeles.

README y `LICENSE-CONTENT.md` quedan alineados con el vocabulario nuevo.

Batería: **1404 aserciones con conexión · 1395 sin conexión**, con un bloque omitido.

## 25 — 2026-09-29

**El campo de la herramienta sugiere nombres mientras se escribe.** Era texto libre, así
que una misma herramienta entraba como «ChatGPT», «chatgpt», «Chat GPT» o «GPT-4o»:
cuatro cadenas para una cosa. La app promete que el dato sea comparable entre artículos,
y ese campo lo incumplía.

Se usa **`datalist`, no `select`**. Es la diferencia entre sugerir y cerrar la puerta:
quien use algo que no esté en la lista lo escribe a mano y vale exactamente lo mismo, sin
tener que elegir una opción «Otra» ni pasar por ningún paso extra. Una lista cerrada
habría dejado fuera a esas personas y roto el sistema en silencio para ellas. Hay una
prueba que lo vigila: si alguien cambiara el `datalist` por un `select`, se pone en rojo.

**21 sugerencias**, ordenadas por tarea y no alfabéticamente, porque quien abre la lista
sin escribir la recorre mejor así; en cuanto escribe, el navegador filtra. Son nombres
propios y no se traducen, igual que los códigos.

- **«Copilot» se separa en dos.** Hay dos productos distintos con ese nombre, uno para
  escribir en Office y otro para código, y declarar «Copilot» no decía cuál, que es justo
  lo que el sistema quiere evitar. `Microsoft Copilot` va primero por ser el de uso más
  extendido entre quienes escriben manuscritos.
- **Las actividades 4 y 6 no llevan sugerencia propia, a propósito.** En formato de datos
  y visualizaciones no hay una herramienta dominante como DeepL lo es en traducción: esas
  tareas se hacen con los asistentes generales que ya están en la lista. Añadir un
  producto de nicho para tapar el hueco le daría prominencia a algo que casi nadie usa.
- **Nada de detección**, tipo Turnitin. Con eso no se prepara un manuscrito, se revisa, y
  son dos cosas que el sistema separa a propósito.
- **El campo del modelo sigue en texto libre.** Los modelos cambian cada pocos meses y
  serían lo primero en quedar desfasado.

**Se dice en claro que son ejemplos**, en el manual en los tres idiomas y en las dos
mitades del README: que no es una lista aprobada ni exhaustiva, y que nada queda excluido
por no estar. Sin esa aclaración, veintiún nombres dentro de algo que se propone como
norma se leen como respaldo. Una prueba comprueba que la aclaración esté en los tres
idiomas.

**En «Acerca de», la afiliación pasa debajo de quienes colaboraron**, con la misma forma
que en el bloque de autoría, en vez de ir metida en la línea de entrada.

**Nota de marcas.** Los nombres sugeridos son marcas de sus titulares, y ahora se dice.
Va en «Acerca de» dentro de la propia app, además de en el README y en
`THIRD-PARTY-NOTICES.md`: esto se distribuye como un archivo único, y quien se descargue
`index.html` suelto no se lleva los demás archivos. Dice que se usan solo para
identificar las herramientas, que no implican afiliación ni respaldo, y que la ausencia
de una no excluye nada. Cumple dos funciones a la vez, porque también ataja la lectura de
«lista aprobada».

Corregido de paso un falso positivo de la guarda de tuteo: llevaba «marcas» en la lista
de formas de tú, y el sustantivo la disparaba. En español ese término es ambiguo de
verdad, así que se saca de la guarda. Una comprobación que obliga a retorcer un texto
correcto es peor que no tenerla.

Batería: **1361 aserciones con conexión · 1352 sin conexión**, con un bloque omitido.

## 24 — 2026-09-29

**Quienes colaboraron llevan identificador y correo, igual que la autoría.** En la 23
solo aparecían los nombres en una frase corrida. Con el identificador y el correo dentro,
esa frase se volvía ilegible, así que ahora cada persona tiene su propio bloque, sangrado
y con los dos datos enlazados:

> **Colaboración:** Unidad de Ciencia Abierta. Revisión de textos, revisión del inglés,
> pruebas de uso y sugerencias de interfaz.
>
> **Carolina Seas Carvajal** · ORCID 0000-0002-2102-1973 · cseas@uned.ac.cr
> **Steven Segura Jiménez** · ORCID 0009-0005-6475-8798 · ssegura@uned.ac.cr

Listarlos aparte, y no dentro del párrafo, tiene una razón práctica además de la
legibilidad: cada quien puede señalar su propia línea.

Los identificadores se comprobaron dos veces antes de publicarlos. Primero el **dígito de
control**, que llevan incorporado: si no cuadra, el identificador está mal escrito aunque
tenga la forma correcta. Después se consultó el **registro público**, y ambos resuelven a
las personas que son. Un identificador con un dígito cambiado acreditaría a otra persona,
y eso no se corrige después de repartirlo.

La batería comprueba, en los tres idiomas, que cada persona aparezca con los tres datos y
que el identificador y el correo sean enlaces reales, no texto suelto. Y verifica el
dígito de control, para que un dato mal copiado no llegue a publicarse.

Siguen **sin aparecer en `CITATION.cff`**, por lo dicho en la 23: el formato solo admite
`authors`, y eso los volvería coautores del software.

Batería: **1351 aserciones con conexión · 1342 sin conexión**, con un bloque omitido.

## 23 — 2026-09-29

**Se acredita a quienes colaboraron.** Hasta ahora la app nombraba al autor y a la
herramienta que la codificó, y a ninguna persona más. En un sistema que propone declarar
contribuciones con precisión, esa omisión se notaba.

En «Acerca de» y en el README aparece una tercera línea, entre quién la desarrolló y la
codificación:

> **Colaboración:** Carolina Seas Carvajal y Steven Segura Jiménez, Unidad de Ciencia
> Abierta: revisión de textos, revisión del inglés, pruebas de uso y sugerencias de
> interfaz.

Tres decisiones que conviene dejar por escrito:

- **Colaboración, no desarrollo ni autoría.** Son papeles distintos y se nombran
  distinto. En el preprint estas mismas personas figuran como coautoras, que es otra
  cosa y también es correcto.
- **Se dice qué hizo cada quien**, no solo los nombres. El propio artículo critica que
  la contribución se recoja como declaración narrativa vaga; una línea que dijera solo
  «colaboradores: X e Y» sería justo eso.
- **No van en `CITATION.cff`.** Verificado contra el esquema del formato: solo admite
  `authors` y `contact`. Ponerlos en `authors` los convertiría en coautores del software
  en cada cita que generan GitHub y Zenodo, que no es lo que son.

Los nombres se escriben una sola vez, en `APP.collab`, y la frase que los rodea se
traduce. Una prueba comprueba que aparezcan completos en los tres idiomas, que la línea
vaya en su sitio, y que no se cuelen en los datos de cita.

Batería: **1348 aserciones con conexión · 1339 sin conexión**, con un bloque omitido.

## 22 — 2026-09-27

Tres correcciones de redacción encontradas en una revisión externa, todas reales y
verificadas una por una.

- **El manual tuteaba en un sitio.** La pregunta sobre las fórmulas matemáticas decía
  «decláralo» dentro de un texto que trata de usted de punta a punta. Sobrevivió a dos
  revisiones porque a simple vista no chirría. Ahora hay una prueba que lo vigila.
- **«Si tradujo el texto con ayuda de IA, es 4» era ambiguo, y además chocaba con la
  nota del Eje 2**, que usa el 3 como ejemplo de traducción. «Con ayuda» sugiere un uso
  parcial, que es justo lo contrario de lo que la frase quería decir. Queda: «Si la
  herramienta tradujo el texto entero, es 4 […]. Si tradujo usted y la herramienta solo
  revisó parte, es menos.» Corregido en los tres idiomas.
- **Las cifras de la batería en la entrada 21 se contradecían**: decía 1337 en un punto
  y 1311 en otro. Corregido con las cifras medidas.

Batería: **1338 aserciones con conexión · 1329 sin conexión**, con un bloque omitido.

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
  apunten todos a la misma dirección. La batería pasa de las 1299 de la versión 20 a
  1337.

Corrección: el commit de la versión 20 dejó `CITATION.cff` y el README en la 19, por un
error al rehacer los commits. Ambos quedan en la 21, coherentes con el resto.

Batería: **1337 aserciones con conexión · 1328 sin conexión**, con un bloque omitido.
Una versión anterior de esta entrada decía 1311 y se contradecía con la cifra de arriba:
era una cuenta intermedia que no se actualizó al añadir las últimas pruebas.

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
