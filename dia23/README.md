## Variables referenciales vs primitivas

Referenciales es la llave del camion donde guardamos muchos datos `objetos arrays funciones` estos son siempre `const`

Primitivas es la caja donde guardamos algun dato `strings numeros booleanos` estas pueden ser `let` o `const`

```js

const num = 25;
num=30; //ERROR no se pyede modificar una constante

const alumnos=["Juan","Maria"];
alumnos[0]="Tomas"; //OK se puede modificar el contenido de un array

```

## Comentarios en JS

- Comentario simple: se utiliza `//` para 1 sola linea
- Comentario simple en linea puede usarse `//` al final de la linea
- Comentario en bloque `/*...*/` para hacer comentarios de multiples lineas
- Comentarios de documentacion: se utiliza `**....*/` para iniciat un bloque informativo. Se usa mucho para funciones.


# Operadores aritmeticos

Tenemos operadores de asignacion comparacion logicos

los aritmeticos mas comunes son:

- Suma +
- resta -
- Incrementar un valor ++
- decrementar un valor --
- multiplicar *
- division /
- modulo %