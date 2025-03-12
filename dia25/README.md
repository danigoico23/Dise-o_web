```js

const edad = 25;
const tienePermiso=true;

//para que cumpla ambas opciones usar &&
const edad = 25;
if(edad<=120 & edad >=18){
    console.log("eres mayor de edad");
}

// para que cumpla alguna de las 2 opciones usar ||
if(edad>=18 || tienePermiso == true){
    cosole.log("puedes entrar");
}

```
## Forma de escribir funciones

```js

//esta funcion tiene dos parametros y devuelve la suma de ambos
function sumar(num1, num2){
return num1+num2;
}

//este llamado a la funcion envia como "argumento" dos numeros
const resultado = sumar(2,3);

console.log(resultado);

//esta funcion tiene 2 parametros y devuelve la suma de ambos
function sumar(num1, num2){
    return num1+num2;
}

//funcion sin nombrar
const sumar = function(num1, num2){
    return num1+num2;
}

//funcionflecha
const sumar=(num1, num2) => {
    return num1+num2;
}

//funcion flecha reducida
// solo sirve si mi funcion tiene 1 sola linea.
const sumar=(num1, num2) => num1+num2;



```

## Truthy / Falsy

En JS podemos tener un valor Truthy o Falsy. Un valor Truthy es aquel que se evalua como verdadero en un contexto booleano, mientras que falsy se evalua como falso.

Podemos utilizar este concepto para la toma de decisiones en nuestro codigo.

Valores falsy: `undefined, null, NaN, 0, "", y false`
Valores truthy: todos los demas

Ejemplos de valores que parecen falsy pero que son truthy:
```js
const val = "false";
const val= -1;
const val= " "; // tiene un espacio, es trythy
const val= 0.1;
const val= "0";
const val = "null"
```

```js
edad=19;
if(edad>18){
//truthy
}
else{
    //falsy
}

if(""){
    console.log("No me ejecutan nunca");
}
else{
    console.log("siempre se ejecuta");
}
```