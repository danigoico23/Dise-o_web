
# Que es un Media Query (MQ)

- Declaraciones en CSS que nos permite definir que arreglas aplicar a partur de unas reglas asignadas por nosotros

# Sintaxis de una MQ

Una media query se compone de las siguientes partes:
- un @media la cual es una palabra reservada [keyword]
- un tipo de media (screen, print, all, speech) [MediaType]
- Operadores (and, not, only) [Operators]
- Breakpoints, que es una condicion (max-width., min-width, etc)
- Un bloque de CSS (nuesstras reglas CSS)

```css
/* keyword MediaType Operador/es (breakpoint)*/
/* @media screen and (breakpoint) {  } */

@media not|only|"" screen and|or (min-width 600px) {

body {
    background-color: lightblue;

}
h1{
    color: red;
}

} 

/* Combinar breakpoints*/
@media screen and (min-width: 600px) and (max-width: 800px){
    body {
    background-color: lightblue;
}
}

/* cuando la pantalla esta horizontal (vertical seria portrait)*/
@media screen and (orientation: landscape){
    body {
    background-color: lightblue;
}
}

/*Reglas para hacer modo oscuro*/
@media screen and (prefer-color-schema: dark){
    body { background-color: darkgray;
}
}
```


### Media Types (screen/print)

- all: todos los dispositivos
- print: material de vista previa de impresion
- screen: pantallas a color (tablets, movil. computadora)
- speech: dispositivos de conversion de texto a voz

- otros: pueden aparecer types DEPRECIATED tv, handheld, speech, braille, etc... 

Ejemplo de impresion:
```css
@media print{
    .no-print{
        display: none !important;
    }
}
```

### Tips para utilizarlos:

- Las MQ Sobreescriben las reglas de CSS normales, pero no posee una mayor especificidad por lo tanto las media queries deben estar por debajo de las reglas que quiera reemplazar.
- Deben tener el mismo selector para que reemplace la regla que deseamos. Como excepcion podemos utilizar las reglas principales en vez de especificas (background para reemplazar background-color)
- Pensar bien los breakpoints
- Podemos utilizar un @media para cada selector, o una sola para todos los selectores (recomendado)
- Mobile First!!!!!

## Mobile First
Intentamos desarrollar siempre primero para el movil, y luego para pantallas mas grandes. De esta manera nos aseguramos de que se vea bien dispositivos moviles.

[2024](https://www.browserstack.com/guide/common-screen-resolutions)

```css

/*Mobile First*/


/* Tablet */
@media only screen and (min-width: 768px){

}

/* Desktop*/
@media only screen and (min-width: 1024px){
}

```

# Ejemplo de Media Queries en Imagenes (usando Picture)

```html
 <picture>
    <source media="(min-width:650px)" srcset="./foto/unafoto">
    <source media="(min-width:450px)" srcset="./foto/unafoto">
    <img src="./foto/unafoto" alt="mascota">
</picture>
```
https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Using_media_queries

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

## Links de Interés

[CSS MQ w3Schools](https://www.w3schools.com/css/css3_mediaqueries.asp)
[Responsive Design w3Schools](https://www.w3schools.com/css/css_rwd_mediaqueries.asp)
[Responsive Design MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Media_queries)
[SCSS + MQ](https://www.freecodecamp.org/news/learn-css-media-queries-by-building-projects/)




