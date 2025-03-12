# Metodos de Arrays / listas

## Pop()
El metodo `pop()` elimina el ultimo elemento de un array y lo devuelve. Este metodo modifica la longitud array.

```js

const frutas=["manzanas", "naranja", "tomate", "uvas", "bananas"];
let ultimoElemento = frutas.pop();
console.log(frutas); // ("manzana", "naranja", tomate, uvas)
console.log(ultimoElemento); // "bananas"
```

## Push()
El metodo `push()` es uno de los mas comunes, anade uno o mas elementos al final de un array. Me devuelve la nueva longitud del array.

```js
const frutas=["manzanas", "naranja"];
let nuevaLongitud = frutas.push("pera","tomate");

console.log(frutas); // (4) [manzana, naranja, pera, tomate]
console.log(nuevaLongitud); // 4
```

## Shift()
El metodo `shift()` elimina el primer elemento del array y lo devuelve. Este metodo modifica la longitud del array.

```js
const frutas=["manzanas", "naranja", "tomate", "uvas", "bananas"];
const elementoQuitado= frutas.shift();

console.log(frutas); // (4) [naranja, tomate, uvas, bananas] 
console.log(elementoQuitado); // manzana
```

## Unshift()
El metodo `unshift()` podemos anadir uno o mas elementos al inicio del array. Devuelve la nueva longitud del array. 

```js
const frutas=["manzanas", "naranja", "tomate"];
let nuevaLongitud = frutas.unshift("pera", "ciruela");

console.log(frutas); // (5) [pera, ciruela, manzana, naranja, tomate];
console.log(nuevaLongitud); // 5
```

## Splice()
El metodo `splice()` cambia el contenido de un array eliminando, creando o reemplazando sus elementos. Modifica el valor original y recibe 3 parametros. 

- El indice del vector donde se va a realizar la operacion
- La cantidad de elementos a eliminar
- Los elementos que quiero agregar

```js
const frutas=["manzanas", "naranja", "tomate", "uvas", "bananas"];
let frutasEliminadas = frutas.splice(2, 2, "peras", "ciruela");

console.log(frutas); // ["manzanas", "naranja", "peras", "ciruela", "bananas"];
console.log(frutasEliminadas); // "tomate", "uvas"
```

Ejercicio de splice:
```js
let lenguaje = ["python", "java", "javascript", "php", "C++" "c#"];
lenguajes.splice(0,1); // elimina el primer valor del array elimina python (actua como shift)
lenguajes.splice(-1,1); // elimina el ultimo valor del array (pop) elimina "C#"
lenguajes.splice(-1, 0, "C", "CObol"); // se posiciona al final, no borra nada  agrega "C" y cobol"

// quitar 2 elementos a partir del indice 2
lenguajes.splice(2,2);
```

## ForEach

El forEach recorre cada elemento de una lista y ejecuta la funcion indicada dentro del mismo.

```js

["a", "b", "c"].forEach( (letra)=>{
    console.log(letra); //imprime cada letra en el console
})
```

## Map

Devolver el doble de cada elemento:

```js
const listaNumeros = [5,15,7];
 const listaNumerosDobles = listaNumeros.map( (num)=>{
    return num*2;
});
console.log(listaNumerosDobles); // [10, 30, 14]


// Codigo optimizado
// se puede optimizar cuando nuestra funcion tiene una linea y esa linea es un return
 const listaNumerosDobles = listaNumeros.map( num=> num*2);
```

## Buscar item

El metodo `find()` devuelve el PRIMER elemento del array que cumpla la funcion de prueba proporcionada. En caso contrario devuelve undefined.

```js
const numeros = [5, 12, 8, 130, 44, 12];
const item = numeros.find(num => num > 10);
console.log(item); // 12 se para en el primer numero que encuentre

```

## Buscar multiples items

la funcion `filter()` devuelve un array/lista con TODOS LOS ELEMENTOS que cumplan que cumplan la condicion especificada.

```js
const numeros = [5, 12, 8, 130, 44, 12];
const listaItems = numeros.filter( num => num > 10);
console.log(listaItems); // [12, 130, 44, 12]


const personas = [
    {nombre: "Juan", edad:33},
    {nombre: "Pedro", edad:18},
    {nombre: "Ana", edad:15},
    {nombre: "Luis", edad:9},
    {nombre: "Maria", edad:30},
];

//obtener una lista de las personas mayores de edad
const listaMayores = personas.filter(persona => persona.edad >= 18);
console.log(listaMayores); 

// {nombre: "Juan", edad:33},
// {nombre: "Pedro", edad:18},
// {nombre: "Maria", edad:30},
```

1. De una lista de numeros devolver solo los IMPARES.
```js
const numeros = [2, 35, 3, 7, 20, 4, 11]

const listaImpares = numeros.filter(num => num%2 != 0);
console.log(listaImpares); // [35, 3, 7, 11]
```

2. De una lista de objetos de personas, imprimir su nombre.

```js
const Personajes = [
    {nombre: "Juan", edad:33},
    {nombre: "Pedro", edad:18},
    {nombre: "Maria", edad:30},
]

const listaNombres = Personajes.map( persona => {
    console.log(persona.nombre);
    });

```

3. Encuentra un libro con el titulo especifico (buscar La Odisea)

```js
const libros = [
    {titulo: 'El Quijote', autor:'Miguel de Cervantes'},
    {titulo: 'Cien años de soledad', autor:'Gabriel Garcia Marquez'},
    {titulo: 'La Odisea', autor:'Homero'},
]

const ElLibroBuscado =  libros.find (libro => libro.titulo == 'La Odisea');
```

4. Dado una lista de numeros desordenados ordenar de menor a mayor (investigar)

```js
const numerors = [5, 20, 3, -10, 5, 25, 100005];
// const ordenados = numeros.sort (function (a,b) { return a - b;});
const ordenados = numeros.sort((a,b) => a - b);
```