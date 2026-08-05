# Manipulativos virtuales de tierradenumeros.com

Materiales manipulativos virtuales para matemáticas, implementados como páginas web.

Cada manipulativo es **un único archivo HTML autocontenido**: no usa librerías externas, no necesita servidor, no necesita conexión y no guarda nada en ningún sitio. Se abre haciendo doble clic y funciona. Eso es deliberado, porque así se puede meter en el Moodle del centro, dejarlo en una memoria USB o usarlo en un aula sin wifi.

Puedes probarlos aquí: **[pbeltranp.github.io/manipulativos-virtuales](https://pbeltranp.github.io/manipulativos-virtuales/)**

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
| [Tiras de papel](app/tiras-de-papel.html) | La fracción como medida: doblar la unidad hasta que encaje |
| [Manteles y servilletas](app/manteles-y-servilletas.html) | Lo mismo con áreas, donde la forma del trozo importa tanto como su tamaño |

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
