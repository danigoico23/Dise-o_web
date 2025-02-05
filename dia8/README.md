# Dia 8

- Los formularios utilizan las etiquetas envolventes de <form>

- Utilizamos etiquetas <input> para ingresar datos. Algunos tipos de ellos eran: radio, checkbox, text, email, password, submit

- Todos los inputs requieren el atributo `name` para enviar la infomación. Este debe ser único, excepto <input type="radio">

- Utilizamos otras etiquetas para algunos tipos de datos por ej: <textarea> 
<select> + <option>

- Los inputs suelen estar acompañados de un <label> como descripcion.

## Metodos de GET y POST para enviar información

- Normalmente GET se utiliza para obtener informacion y POST para enviarla.

- GET tiene un limite de 2048 caracteres y POST no (se utiliza para enviar información de mayor tamaño, incluyendo el upload de archivos)

- GET es visible en la URL y POST utiliza el cuerpo de la peticion.

Ejemplos de formularios con GET:
- Buscadores
- Filtros
- Paginacion

ejemplos de formulario con POST:
- Formulario de contacto
- Formulario de login/registro
- Formulario de Pago

Hacer un `login-form.html` sin estilos enviando informacion al atributo action="asdfasdf"

<form action="./" metod="GET"></form>

- Investigar los siguientes types, explicar que hacen, crrear un ejemplo en `otros-inputs.html`. number, color, date, file, reset, hidden, range

esto es solo para cuando tenemos un formulario que hace carga o upload de archivos
<form method="POST" enctype="multipart/form-data">
  <input type="file">
</form>

- Nuevas etiquetas/tipos: tel, url, search, time, week, month, dateime-local.

# Introduccion a Nomenclaturas CSS y BEM

Forma de nombrar nuestras clases CSS para mantener codigo limpio y ordenado. Buscamos codigo comprensible predecible y facil de mantener.

## Nombres de variables/selectores/archivos

- UPPERCASE
- lowercase
- Title Case
- camelCase: `miClaseDeHtml`
- PascalCase: `MiClaseDeHtml`
- kebab-case: `mi-clase-de-html` (se utiliza para nombrar archivos)
-snake_case: `mi_clase_de_html`

## Nomenclatura BEM (Block-element-modifier)

- [BEM](https://getbem.com/naming)

- block: class="carta"
- elemento: class="carta_header"
- modifier: class="carta_header--izq"

