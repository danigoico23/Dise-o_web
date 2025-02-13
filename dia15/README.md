# CSS GRID

Grid es un sistema de maquetacion bidimensional para crear interfaces y layouts tipo tablas. Se compone de filas y columnas y se pueden anidar unos de otros. Se pueden crear layouts complejos con muy pocas lineas de codigo.

- Nos sirve para crear layouts.
- No es opuesto a Flex, se pueden combinar entre ellos.
- Grid si sustituye a las <tables> para el armado de layouts

Utilizamos `display:grid` para crear un grid y `grid-template-columns` y `grid-template-rows` para definir el numero de columnas y filas.

```css
/*layout de 3 x 3*/
.container{
    display: grid;
    grid-template-columns: 100px 100px 100px;
    grid-template-rows: 100px 100px 100px;
}
```

Pueden visualizar el layout de GRID desde la consola de chrome

Podemos indicar a cada item, donde posicionarlo usando `grid-row-start`, `grid-row-end`, `grid-column-start` y `grid-row-start`, teniendo en cuenta que las filas y col empiezan en 1 (no en 0)

Si queremos que ocupe 3 columnas y 1 fila, debemos indicar que comience en la col 1, y termine en la col 4. Y que la fila comience en la 1 y termine en la 2.

```css

.item-1{
    grid-column-start:1;
    grid-column-end:4;
    grid-row-start:1;
    grid-row-end:2;
}
```

Se pueden invertir el start y el end y funcionara igual.

```css
/* item de 3 cols y 1 fila*/
.item-1{
    grid-column-start:1;
    grid-column-end: span 2; /*se amplia un bloque mas*/
    grid-row-start: 1;
    grid-row-end: span 3; /*se amplia 2 bloques mas*/
}
```
Para reducir grid-column-start y grid-column-end en una sola linea, podemos usar `grid-column`. Lo mismo con `grid-row`.

```css
.item-2{
    grid-column:1/3; /*col start / end*/
    grid-row:2/4; /* row start / end */
}
```

Podemos utilizar una forma aun mas corta usando `grid-area`, donde definimos grid-row-start, grid-column-start, grid-row-end, grid-column-end.

```css
.item-2{
    grid-area:1/1/4/4
}
```

con Grid es mmuy simple crear un elemento por encima de otro.

Podemos utilizar grid-gap para definir un espacio entre las columnas y filas. El mismo soporta un valor para fila y columna, o 2 valores para diferenciarlos. El mismo soporta un valor para fila y columna o 2 valores para diferenciarlos.

```css
.container{
    display: grid;
    grid-template-columns: 100px 100px 100px;
    grid-template-rows: 100px 100px 100px;
    grid-gap: 1em 3em; /* separacion independiente para filas y para cols */
    grid-gap: 10px; /*separacion entre filas y col*/
}
```

Existe la opcion repeat () que nos permite repetir el numero de veces que quiero para una fila o columna

```css
.container{
    display: grid;
    grid-template-columns: repeat (3, 100px);
    grid-template-rows: repeat (3, 3em);
    grid-gap:10px;
}
```

Si agregamos mas bloques dentro de nuestro grid, se intentara ubicarlo en la primera posicion libre disponible. Si no quedan posiciones libre, se creara una nueva fila. Esta nuevas celdas no tendran el tamaño asignado en nuestro grid'template y a esta se le llaman ¨grid implicitas¨. Podemos usar `grid-auto-rolls: 100px` para definir el tamano de nuestras nuevas filas.


```css
.container{
    display: grid;
    grid-template-columns: repeat (3, 100px);
    grid-template-rows: repeat (3, 3em);
    grid-gap:10px;
    grid-auto-rows:100px;
}
```
Tambien el `grid-auto-flow` que nos permite definir si las nuevas celdas se crearan como filas o columnas.


```css
.container{
    display: grid;
    grid-template-columns: repeat (3, 100px);
    grid-template-rows: repeat (3, 3em);
    grid-gap:10px;
    grid-auto-rows:100px;
    grid-auto-flow:column;
}
```

Las unidades que podemos utilizar son px, %, em, rem, pero se le suma una nueva de valor fraccional o fr. Este valor nos permite fraccionar el tamaño disponible.

Por ejemplo, si tenemos 3 columnas y definimos que la primera columna tenga un tamaño de 1fr, la segunda columna ocupara el doble de espacio que las otras 2.

```css
.container{
    display: grid;
    grid-template-columns: 1fr 2fr 1fr;
    grid-template-rows: repeat (3, 3em);
    grid-gap:10px;
}
```