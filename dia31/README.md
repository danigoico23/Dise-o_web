# dia 31
## Listeners para eventos de usuario

Son funciones que se ejecutan en respuesta a eventos a especificos que ocurren en el DOM, como por ejemplo clicks, movimientos de mouse, teclas presionadas, teclas levantadas... Para agregar un evento usamos `addEventListener(evento, funcion)`

```js
// seleccionar item del DOM
const boton = document.querySelector('buton');

//Agregar un event listener para el evento del click
boton.addEventListener("click, miFunction");

function miFunction(){
    console.log(`HOLA`);
}
```

## Pasar parametros a funciones con eventos

A veces necesitamos enviar parametros adicionales a la funcion que maneja el evento

```js
boton.addEventListener("click", function(){
    miFuncion("Tomi");
})

// Ejecutar la funcion sin enviar parametro
boton.addEventListener("click", miFuncion);
// Ejecutar la funcion enviando parametro, la debo meter dentro una funcion flecha
boton.addEventListener("click", ()=> miFuncion("Maria"));


function miFuncion(usuario){
    console.log(`HOLA ${usuario}`)
}
```

Ejercicio:
1. Cambiar el color de un elemento al hacerle click:
Crear un boton que cambie su color de fondo

2. Mensaje al pasar el mouse:
Crear un elemento que muestre un mesnsaje cuando el raton pase por encima de el.

### Paremetro "e" (event/evento)

Es un objeto que contiene informacions sobre ele vento ocurrido. Este se pasa automaticamente a la funcion que maneja el evento.

```js
function handleClick(e){
    console.log("El boton ha sido clickeado");
    console.log("Coordenadas del Mouse:", e.clientX, e.clientY);
}

boton.addEventListener('click',  handleClick);

```

