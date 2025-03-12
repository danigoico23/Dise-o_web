## Operacion ternaria

Una forma de reescribir `if...else`. Se componen de tres partes:
1. Una expresion que se evalua.
2. Expresion que se ejecuta en caso de ser cierta
3. Expresion que se ejecuta en caso de ser falsa

- Simplifica la legibilidad, pero no se recomienda para anidar operaciones ternarias, o cuando el resultado de la operacion es muy complejo. 
- No se puede usar ternarias si no tengo el "else..." (solo me sirven si tengo truthy y falsy)
- Solo se puede utilizar cuando el resultado de la operacion posee mas de una linea.


```js
let numero = 10;
let numero;
if(numero % 2 == 0){
    mensaje = "es par";
}else{
    mensaje = "es impar";
}

// version ternaria:
let mensaje = numero%2 ===0 ? "es par" : "es impar";



if (edad >=18){
    mensaje = "es mayor de edad";
}else{
    mensaje = "es menor de edad";
}

//version ternaria:
let mensaje = edad >=18 ? "es mayor de edad" : "es menor de edad";

```
```js
// funcion que recibe 2 numeros y devuelve el mayor de los dos
function mayor(num1, num2){
    return num1>num2 ? num1 : num2;
}

numMayor = mayor (5,3); //5
numMayor = mayor(-5,7); //7
```

Crear una funcion que reciba 2 parametros (jugador1, jugador2) y que devuelva si el `jugador1` le gana al `jugador2` en pieda, papel o tijera.
```js
function juegoPiedraPapelTijera(jugador1, jugador2) {

  if (jugador1 === jugador2) {
    return "Empate";
  }
  if (
    (jugador1 === "piedra" && jugador2 === "tijera") ||
    (jugador1 === "tijera" && jugador2 === "papel") ||
    (jugador1 === "papel" && jugador2 === "piedra")
  ) {
    return "Jugador 1 gana";
  }

  return "Jugador 2 gana";
}

```

## Recorrer Arrays/Listas

### ForEach

- recorrer cada item de un array, y ejecuta una funcion dentro del mismo.
- Se le asigna una variable a cada item
ejemplo: listaAlumnos -> alumno

```js
const letras = ["a", "b", "c"];
letras.forEach((letra)=>{
    console.log(letra);
})



 ## Operaciones con bucles
 