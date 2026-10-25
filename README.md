# Manipulativos virtuales de tierradenumeros.com

Materiales manipulativos virtuales para matemáticas, implementados como páginas web.

Cada manipulativo es **un único archivo HTML autocontenido**: no usa librerías externas, no necesita servidor, no necesita conexión y no guarda nada en ningún sitio. Se abre haciendo doble clic y funciona. Eso es deliberado, porque así se puede meter en el Moodle del centro, dejarlo en una memoria USB o usarlo en un aula sin wifi.

Puedes probarlos aquí: **[pbeltranp.github.io/tierradenumeros-manipulativos](https://pbeltranp.github.io/tierradenumeros-manipulativos/)**

Cada uno, con su explicación didáctica —para qué sirve, qué preguntas funcionan y qué conviene no contar antes de tiempo—, está en [tierradenumeros.com/manipulativos](https://tierradenumeros.com/manipulativos/). Algunos de estos manipulativos están pensados más específicamente para formación del profesorado.

Para crearlos hice uso de Claude. Existen webs que ya disponían de algunos similares, por ejemplo, para las plaquetas y policubos, pero he tratado de añadir alguna funcionalidad que echaba en falta. Otros, como las geotiras, yo no los había encontrado por otro sitio. 

## Qué hay

| Manipulativo | De qué va |
|---|---|
| [Geotiras](app/geotiras.html) | Tiras perforadas unidas con encuadernadores. El triángulo aguanta y el cuadrilátero se desmonta |
| [Poliminós](app/poliminos.html) | Cuadrados unidos por los lados, con giros exactos y simetría respecto de un eje que se marca |
| [Policubos](app/policubos.html) | La versión 3D, en perspectiva isométrica, con giros por cada eje y plano de simetría |
| [Plaquetas numéricas](app/plaquetas.html) | Las placas de Herbinière-Lebert, superponibles para comprobar sumas |
| [Geoplano cuadrado](app/geoplano.html) | Trama cuadrada sin límites, con goma que se estira y cordel que no |
| [Geoplano isométrico](app/geoplano-isometrico.html) | Trama triangular, con una opción de luz que convierte los dibujos planos en cuerpos |
| [Corcho geométrico](app/corcho.html) | Chinchetas libres y un rotulador atado con cordel que traza circunferencias y elipses |
| [Tangram mínimo de Brügner](app/tangram-brugner.html) | Tres triángulos semejantes con los lados en razón √φ |
| [Pattern blocks](app/pattern-blocks.html) | Las seis piezas de siempre, con imán, grupos y simetría axial |
| [Tiras de papel](app/tiras-de-papel.html) | La fracción como medida: una tira unidad que se dobla en partes iguales para medir otras |
| [Manteles y servilletas](app/manteles-y-servilletas.html) | Lo mismo con áreas: medir manteles cubriéndolos con servilletas |
| [En busca de la unidad perdida](app/unidad-perdida.html) | El mantel llega ya medido y lo que hay que reconstruir es la unidad |
| [Manteles a medida](app/manteles-a-medida.html) | Llega un encargo con la medida puesta y hay que fabricar el mantel |
| [Tiras a medida](app/tiras-a-medida.html) | Lo mismo con longitudes: fabricar la tira desde la unidad o desde otra tira |
| [Figuras equivalentes](app/figuras-equivalentes.html) | Cortar una figura con tijeras y recomponer un rectángulo con todas las piezas |
| [Reparto de tortillas](app/reparto-de-tortillas.html) | Repartir tortillas por fases, con la tabla y la división en caja al lado |
| [Tortillas y platos](app/tortillas-y-platos.html) | Partir tortillas en trozos iguales y armarlas de nuevo en cada plato |
| [Dados a medida](app/dados-a-medida.html) | Un dado configurable: caras, valores y probabilidades, con tiradas de una en una o de mil en mil |
| [Chinchetas](app/chinchetas.html) | Tirar un puñado de chinchetas y contar cuántas caen boca arriba, con el porcentaje tapado |
| [Cuál sobra](app/cual-sobra.html) | Generador de carteles de «¿cuál sobra?» con figuras geométricas |
| [Palotes numéricos](app/palotes-numericos.html) | Los *number sticks* de Baroody: regletas divididas en bloques que cuentan, no solo miden |
| [Billetes](app/billetes.html) | Billetes que se agrupan y desagrupan a mano, en la base que se elija |
| [Constructor de algoritmos](app/constructor-de-algoritmos.html) | Montar un algoritmo de suma o resta, verlo ejecutarse y buscar los casos en los que falla |
| [Sistemas numéricos](app/sistemas-numericos.html) | El mismo número en sistemas históricos, y un sitio para inventarse uno |
| [La operación «de»](app/operacion-de.html) | Una fracción como cantidad y otra como operador que actúa sobre ella |
| [Longitud × Longitud](app/longitud-x-longitud.html) | El producto de dos fracciones como área de un rectángulo construido desde la unidad |
| [Longitud × Área](app/longitud-x-area.html) | El producto de una longitud por un área como volumen de un prisma, en 3D |
| [Bloques de Dienes](app/bloques-de-dienes.html) | Los 48 bloques lógicos, con cuerdas, cuadros y tarjetas para clasificar, y la variante de Touyarot |
| [Dicotominó](app/dicotomino.html) | 64 piezas con seis variables de dos valores, para buscar y crear patrones |

## Si vas a modificar alguno

Añade `#test` al final de la dirección:

```
geotiras.html#test
```

Se lanzan solas las comprobaciones que lleva dentro cada archivo, y sale un informe con un botón para copiarlo. No son pruebas de adorno: comprueban sobre todo la geometría, que es donde están los errores que no se ven mirando la pantalla. En el tangram de Brügner, por ejemplo, destaparon que dos de las figuras de ejemplo que yo había colocado a mano tenían las piezas solapadas.

Si cambias algo, pásalas antes de dar el archivo por bueno. Y si añades una función, añade su prueba: están todas juntas al final de cada archivo, en la sección `AUTOCOMPROBACIÓN`.

## Cómo está organizado

```
app/         los manipulativos, un archivo cada uno
portadas/    imágenes de portada, opcionales
index.html   la portada con la lista
```

Para añadir uno nuevo: deja su HTML en `app/` y añade una línea al array `MANIPS` que hay al final de `index.html`.

El código está comentado en castellano, y los comentarios cuentan **por qué** está hecho así, no qué hace cada línea. Donde hay una decisión rara suele haber una razón geométrica detrás, y está escrita.

## Se agradecen

Las *issues*, sobre todo estas:

- **Cosas que no funcionan en tabletas o en las pizarras digitales del aula.** Es donde menos he podido probar y donde más papeletas hay de que algo falle.
- **Errores matemáticos.** Si un recuento, un área o una construcción no cuadra, me gustaría saberlo.
- **Cómo te fue en clase o trasteando con el manipulativo.** Si has usado alguno y algo estorbaba, sobraba o faltaba.

Y por supuesto los *forks*: si te sirve mejor cambiado, cámbialo.

## Licencia

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.es). Puedes usarlos, copiarlos, modificarlos y repartirlos, también en clase y también modificados, citando la autoría.

Cada archivo lleva dentro, en su panel `?`, la autoría y la licencia. 
Para citar:

> Beltrán-Pellicer, P. (2026). *Manipulativos virtuales de tierradenumeros.com*. https://tierradenumeros.com/manipulativos/
