# Dia 3

Si quiero poner un link a una cosa que tengo en la misma carpeta donde el html en el que estoy trabajando
Un punto sirve para indicar que busque en la misma carpeta

<a href="././">

para poner un link a otra carpeta en la que no estoy
dos puntos significa que estoy saliendo de la carpeta y yendo hacia atras hacia carpeta general

<a href="../../la otra carpeta">

Shortcut para convertir codigo en comentario (no lo se hay que descubrirlo)

atributo <a href="bla bla" target="_blank"> es para que un link cargue en una pestaña nueva

atributo target="_self" es para que un link se cargue en la misma pestaña pero esto ya ocurre por defecto asi que no se usa mucho

Para mover codigo hacia arriba o abajo, se subraya y alt+flechitas

<span> Span se usa para escoger palabras o frases en concreto dentro de un parrafo y darles color

span{ 
    color: green;
}

<div> Esta etiqueta se utiliza para generar divisiones en el documento

Existen etiquetas en bloque y las inline:

<span> es inline
<div> es en bloque
<p> es en bloque

<button> Para hacer un boton WOW!
<button onclick="alert('Clickkkk')"> para que salga el mensaje Clickkkk al pulsar el boton

<id> si quiero aplicar un cambio a una etiqueta especifica, todas las etiquetas pueden llevar <id>

Para aplicarle cambios en CSS a un <id> hay que usar #nombre-del-id {}

Para seleccionar un class hay que usar .nombre-de-class {}

# Box model

Cuando creamos un archivo CSS tenemos 
-Padding (Espacio entre el contenido y el borde del elemento)
-Margin (Espacio entre el borde del elemento y otros elementos)
-Border (La linea que rodea el contenido)
-Content (Espacio donde se muestra nuestro contenido como es texto,imagenes...)



