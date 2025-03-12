# BEM (Block, element, modifier)

# Suite CSS

- Block pasa a ser "Component"
- Element pasa a ser "Elemento"
- Modifier pasa a ser "Modifier"

Nuevos
- Utilities
- Estados

## Utilities

- Se escribe con una `u-utilityName` por ejemplo `u-red`
- Se escribe con "u-" y despues camelCase
- Se utiliza para aplicar un estilo a cualquier elemento

```css
.u-red{
    background-color: red;
    color:white;
}

.u-big{
font-size; 5rem;
}

/*utilities responsive*/
.u-sm-text{
    /*texto pequeño*/
}

.u-md-text{
    /*texto mediano*/
}

.u-lg-text{
    /*texto grande*/
}

```

# Componente

Igual al bloque de BEM, pero se escribe con PascalCase. Por ejemplo `Header`, `MiBoton`, `SeccionHero`, `Card`, `Tweet`

# Element (Part, DescendentName)

Igual que el elemento en BEM, pero se escribe con camelCase. Por ejemplo `Header-title`, `Card-imageFront`, `Tweet-bodyImage`

- Por ejemplo en `Card-imageFront` Card es el componente y imageFront es el elemento

```html
<article class="Tweet">
   <header class="Tweet-header">
   <img class="Tweet-headerImg" src="./img" alt="imagenchula">
   </header>
   <div class="Tweet-bodyText">
      ...
   </div>
</article>
```

## Modificadores

Al igual que en BEM y se utiliza `Componente--nombreModificador` y se utiliza camelCase

```html
<button class="Button">Boton normal</button>
<button class="Button Button--navidad">Boton de navidad</button>
```
## Estados

Nuevo: Clases para elementos que marcan el estado de un componente/elemento. Se escribe con camelCase y usa la palabra `is-` delante.

```css

.Tweet{
    /*estilos de un Tweet comun*/
}
.Tweet.is-expanded{
    /*solo cambios para Tweet abierto*/
}
```

```html
<article class="Tweet">
    ...
</article>
<article class="Tweet is-expanded">
    ...
</article>
```

# Grid continuacion (2/2)

Existe la opcion minmax() que nos permite definir un tamaño minimo y maximo para las columnas y filas.

```css

.container{
    display:grid;
    grid-template-columns: minmax(100px), minmax(100px, 2fr) minmax (100px, 1fr);
    grid-template-rows: 100px 100px 100px;
    grid-gap: 10px; 
}
```

# Grid Template Areas

Podemos nombrar las celdas utilizando `grid-template-areas` y asignando un nombre a cada una:

```css

container{
    display:grid;
    grid-template-columns: repeat (3, 1fr);
    grid-template-rows: repeat (3, 100px);
    grid-gap:10px;
    grid-template-areas: 
    "header header header"
    "main main sidebar"
    "footer footer footer";
}
/*si se pone un punto en vez de por ejemplo sidebar no se pondra pero seguira ocupando el espacio*/

.item-1{
    grid-area: header;
}

.item-2{
    grid-area: main;
}

.item-3{
    grid-area: footer;
}

.item-4{
    grid-area: footer;
}

```

Podemos utilizar`justify-items` y `align-items` para alinear los elementos dentro de las celdas. Sus opciones posibles son: start, end, center, stretch y baseline. Por defecto se aplica stretch. 

```css

container{
    display:grid;
    grid-template-columns: repeat (3, 1fr);
    grid-template-rows: repeat (3, 100px);
    grid-gap:10px;
    justify-items: start;
    align-items: end;
}

```

Podemos decirle a un item especifico que se alinee de manera diferente utilizando `justify-self` y `align-self`. Sus opciones son: start, end, center, stretch y baseline


```css

.item-1{
    justify-self:center;
    align-self: stretch;
}

```

Podemos alinear nuestro grid en base a su contenedor utilizando `justify-content`
y `align-content`. Sus opciones son: start, end, center, stretch, space-around, space-between y space-evenly.

```css

container{
    display:grid;
    grid-template-columns: repeat (3, 1fr);
    grid-template-rows: repeat (3, 100px);
    grid-gap:10px;
    justify-content: center;
    align-content: center;
}

```

Podemos crear un grid responsive con el uso de `auto-fit`. Esto nos permite que los elementos se ajusten al tamaño del contenedor.

```css

.container{
    display:grid;
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
    grid-template-rows: repeat (4, 1fr);
    grid-gap: 10px;
}

```
