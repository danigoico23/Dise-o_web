# Javascript

Es un lenguaje de alto nivel, es interpretado y orientado a objetos. Lo utilizamos para crear contenido dinamico e interactivo en sitios web.

Alto nivel: esta disenado para ser facil de leer y escribir por humanos.
Interpretado: se ejecuta en tiempo real, linea por linea y no necesita ser compilado.

```js

let numero = 1;
console.log("linea 1 y numero vale:", numero);
// imprime en consola el texto linea 1 y numero vale : 1
numero = numero + 2;
console.log("linea 2 y numero vale:", numero);
//imprime el cnsola el texto linea 2 y numero vale : 3

```

Orientado a objetos:

Js utiliza un paradgima (OOP - Object Oriented Programing), significa que organiza su codigo en "objetos". Un objeto es una coleccion de `propiedades` (caracteristicas) y `metodos` (funciones) que se pueden leer y manipular.

Perro:
// Propiedades 
- color: blanco y negro
- nombre: Lasie
// metodos
- ladran()
-moverCola()

```js
//ejemplo de propiedades y metodos
const alumno = {
    nombre: "Lucia",
    edad: 35,
    saludar: function(){
        console.log("Hola, mi nombre es Lucia");
    }
}

// para imprimir el nombre del alumno usamos algo como:
console.log(alumno.nombre)
console.log("Me llamo", alumno.nombre, "y tengo", alumno.edad, "años");
//Me llamo Lucia y tengo 35 años

//para ejecutar un metodo/funcion tenemos que usar () al final
alumno.saludar();

```

## Donde podemos probar/codificar con JS

- En el navegador: en la pestana de consola
- En etiquetas de `<script>` dentro del html y se suelen poner al final antes de cerrar el `body`
- Se puden usar archivos externos con la extension `.js` linkeado en nuestro html
- Usar extension de VSC -> Quokka. Para empezar a usar: "Command+P" ">Quokka"
- Usar en paginas externas como `playcode.io`, `codepen.io`

# Funcionalidades Javascript

- Manipulacion del DOM (Document Object Model): agregar, modificar o quitar elementos HTML y CSS
- Procesar formularios: verificar datos ingresador por el usuario y realizar formularios complejos de multiples secciones
- Manejo de animaciones: Manipular efectos visuales y animaciones en nuestra web.
- Manejo de eventos: responder a las acciones del usuario como por ej  (hacer click, mover el mouse, desplazarse...)
- Comunicacion asincrona con servidores mediante AJAX/Fetch: enviar y recibir datos de un servidor sin tener que recargar la pagina

## Tipos de datos

- Numeros: enteros, decimales, positivos, negativos
- Cadenas de textos (strings): textos, palabras, frases. Entre comillas simples o dobles o backticks.
- Booleanos: verdadero o falso
- Listas de cosas (arrays): se escriben con corchetes [] y los items se separan con coma.
- Objetos (object): Coleccion  de propiedades (caracteristicas) y metodos (funcionalidades) y se escriben con {}

```js

// PRIMITIVOS

let texto = "Hola alumnos de CEI";
let textoConComillas = 'Hola estoy muy bien';
let textoConComillasDobles = "Im Tommy"
let texto = `Quiero comillas 'simples' y tambien quiero usar "dobles" ` //template string

let numero = 123;
let numero2 = "123"; // 123
numero2= Number(numero2); //123

let entero = 25;
let decimal = 22.30;
let negativo = -5;
const PI = 3.14159;

let estaEncendido = false;
let isPrimary= true;

// REFERENCIALES

//objeto
const alumno= {
    nombre: "Mario";
    edad: 33,
    isRecibido: false,
    presentarProyecto: function()=> {
        this.isRecibido= true;
        this.edad= 34;
    },
    irseDeVacaciones: function() {...}
}

alumno.presentarProyecto(); //presenta el proyecto
alumno.edad; // 33

// Listas o ARRAYS

const alumnosDeDW = ["Jhon", "Maria", "Miriam", "Sonia"...];
const edades = [15,20,30,23,14];
const listaMixta = [1, "Juan", true, {val1: "hola", val2: "chau"}];

console.log( alumnosDeDW[0]) // Jhon
console.log( alumnosDeDW[1]) // Maria

//Para escribir un valor en una lista
alumnoDeDW[0] = "Jhon Edward";
console.log(alumnosDeDW[0]) //Jhon Edward;

```

ejercicio1
`frutas=["manzana, "banana", "naranja];`
`console.log(frutas[0]);`
`frutas[1]="Mango";`
`console.log(frutas);`
`console.log(frutas.length);`