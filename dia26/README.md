# Manipulacion de textos

1. Concatenacion

```js
const nombre="Lucia"
const apellido="Perez"

const nombreCompleto=nombre + "" apellido; //Lucia Perez

// concatenar usando +=

i++; // i = i+1

let saludo="Hola, ";
saludo += "Como estas?";
console.log(saludo;) // Hola, Como estas?

```

2. Interpolacion

Cuando usamos plantillas literales (`template literals` / template strings)
Se pueden insertar `variables` o `expresiones` dentro de una cadena de texto usando `${}`

```js
let nombre = "Ana";
let edad= 25;

//interpolacion

let mensaje=`Hola, mi nombre es ${nombre} y tengo ${edad} anos`;

//insertar expresion
const total=50;
const iva = 0.21;
log.console= (`El total con impuesto es ${total + (total*iva)}`);

```

3. Metodos de strings

JS nos ofrece multiples metodos/funciones para manipular mcadenas de texto.

- `toUpperCase()` y `toLowerCase()`
Convierte todas las letras de una cadena en mayusculas o minusculas.

- `split()`
Divide una cadena de texto en una lista/array basada en el separador elegido.

- `slice()`
Extraer una porcion de la cadena basada en indices de inicio y fin (sin incluir el indice final)

- `replace()`
Reemplaza una parte de la cadena por otra (la primera ocurrencia).
Soporta expresiones regulares (regex) para portenciar la busqueda. 

- `trim()`
Elimia todos los espacios al principio y al final de la cadena

- `includes()`
Verifica si una cadena contiene un asubcadena especifica

- `startsWith()` y `endsWidth()`
Verifica si una cadena comienza o termina con una subcadena especifica.

- `repeat()` 
Repite una cadena un numero especifico de veces


```js
let texto = "Me encanta Javascript";

//toUpperCase(), toLowerCase()

console.log(texto.toLowerCase()); // me encanta javascript
console.log(texto.toUpperCase()); // ME ENCANTA JAVASCRIPT

//split
const palabras = texto.split(" ");
console.log(palabras); //["Me", "encanta", "Javascript"];
const palabras2= texto.split ("encanta");
console.log(palabras2); // ["Me", "Javascript"];
const emeail="maria@alumnos.cei.es";
const separacion=email.split("@");
console.log(separacion); //["maria", "alumnos.cei.es"];

//slice
let frase = "Aprender javascripts es divertido";
console.log("Parte de la frase:", frase.slice(9,19)); // javascript;
console.log("Desde e; omdoce 9 al final:", frase.slice(9)); // javascript es divertido;

// Replace
let frase= "Hola mundo. hola hola hola hola universo"
console.log("Reemplazar 'hola' por 'Hola':", frase.replace("hola", "Hola")); //Hola mundo. Hola hola hola hola hola universo (cambia el primer "hola")
console.log ("Reemplazar 'hola' por 'Hola': ", frase..replaceAll("hola", "Hola")); //Remplaza todos los holas

//trim
let frase= "   Hola soy   Dani   ";
console.log(frase.trim()); // "Hola soy    Dani"

//includes
let frase="El sol brilla en el cielo";
console.log("Contiene 'sol'?" + frase.includes("sol")); //true
console.log("Contiene 'luna'?" + frase.includes("luna")); //false
```
podemos combinar los metodos

```js
//Cambiar para que ponga `ME ENCANTA JAVASCRIPT EN DISENO WEB`
let frase= "    No me gusta Javascript en diseno web     ";
let resultado = frase.trim().replace("No me gusta", "Me encanta").tuUpperCase();


const hobbies = ["Futbol", "Programar en JS", "Leer"];

for (i=0; i< hobbies.length ; i++){
    const hobbie = hobbies[0];
    console.log(hobbie); // Leer, Leer, Leer
}

```




