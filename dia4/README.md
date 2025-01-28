# dia 4

## Selectores CSS

Hoy en dia se usa solo clases para CSS y id mas para javascrypt.

```css
/*selector de id*/

#caja{  }

/*selector de clase*/

.caja{  }

/*selector de etiqueta*/


/*selector de multiples items*/

p,h1,h2{
    color: red;
}

/*selector de multiples items*/

img[alt="Foto1" ]{
    color: brown;
}

/* selector de hijos directos*/
Este dice que exactamente todos los "a" que sean hijos directos de h1 que sean hijos directos de un nav sean...

nav > h1 > a {

}

/* selector de todos los descendientes */
Este dice que todos los elemtnos "a" que sean hijos de un nav sea...
Este se usa mucho

nav a {

}

p + a {

}

Hay reglas de reseteo en CSS
meyerweb es un sitio que lo explica
```

```html
<div class="caja" id="caja">soy un div</div>
<img src="./img/foto.png" alt="Foto1" >
<nav>
    <h1>
        <a href="foto"></a>
    </h1>
</nav>
```

# Reset CSS

Una reset stylesheet sirve para que todos los navegadores inicien nuestros proyectos con los mismos estilos sin aplicar los propios del navegador en concreto.

Ejemplos de reset CSS:

-Meyer web (esta un poco anticuado)

-Eduardo Fierro https://raw.githubusercontent.com/eduardofierropro/Reset-CSS/refs/heads/main/css/app.css

-Top 10 de paginas de reseteo https://cssauthor.com/css-reset-stylesheets/

```css
/*El asterico significa agarra todas las etiquetas de la pagina*/
/*El border-box utiliza el borde de la caja como ancho en vez del contenido*/

*{
    margin: 0px;
    padding: 0px;
    box-sizing: border-box;
}

```
# Mini - actividad
1. Crear una pagina con 2 cajas que contenga parrafos y con la clase      ".caja"
2. Agregar estilos a tus cajas para visualizar bordes, margenes y padding.
3. A la segunda caja agregar la clase ".alternativa"
4. A la clase alternativa, agregar el estilo box-sizing: border-box y comparar la diferencia.
5. Por ultimo buscar en internet alguna hoja de reset e implementar en la web.