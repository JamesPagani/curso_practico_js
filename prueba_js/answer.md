# Test de JavaScript - Respuestas

## Variables y operaciones

### 1. Responde las siguientes preguntas:
1. ¿Qué es una variable y para qué sirve?
    - Una variable es un espacio de memoria donde se pueden guardar (y actualizar) valores.
2. ¿Cuál es la diferencia entre declarar e inicializar una variable?
    - ***Declarar*** una variable significa reservar espacio en la memoria para guardar un valor despues. ***Inicializar*** una variable significa asignar un valor a dicho espacio de memoria.
3. ¿Cuál es la diferencia entre sumar números y concatenar strings?
    - Sumar numeros implica hacer la operacion matematica de adicion entre dos numeros. Concatenar cadenas/strings involucra "pegar" dos cadenas.
4. ¿Cuál operador me permite sumar o concatenar?
    - Ambas operaciones se hacen con el operador +

### 2. Determina el nombre y tipo de dato para almacenar en variables la siguiente información
- Nombre: string
- Apellido: string
- Nombre de usuario en Platzi: string
- Edad: number
- Correo electrónico: string
- Mayor de edad: boolean
- Dinero ahorrado: number
- Deudas: number

### 3. Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios
```javascript
let nombre = 'Jaime Andres';
let apellido = 'Galvez Villamarin';
let username = 'JameSpaghetti';
let edad = 24;
let email = 'jaimeagalvezv@gmail.com':
let mayorDeEdad = edad >= 18;
let dinero = 1000000;
let deudas = 0;
```

### 4. Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:
- Nombre Completo (nombre y apellido)
- Dinero real (dinero ahorrado - deudas)
```javascript
let fullName = `${nombre} ${apellido}`;
let totalMoney = dinero - deudas;
```

## Funciones

### 1. Responde las siguientes preguntas
- ¿Qué es una función?
    - Una funcion es un bloque de codigo que realiza una operacion o *funcion* especifica. Opcionalmente, estas pueden recibir parametros/argumentos para ayudar o modificar la operacion que se realiza.
- ¿Cuándo me sirve usar una función en mi código?
    - Las funciones son MUY utiles cuando necesitas hacer una operacion varias veces, disminuyendo la repeticion de codigo.
- ¿Cuál es la diferencia entre parámetros y argumentos de una función?
    - Aunque ambos terminos pueden usarse de manera intercambiable, los parametros se refieren a los valores que pasan a la funcion y los argumentos los valores que dicha funcion recibio.

### 2. Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:
```javascript
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");

// My answer
function introduction(name, lastName, nickname) {
    console.log(`Mi nombre es ${name} ${lastName}, pero prefiero que me digas ${nickname}`);
}
```

## Condicionales

### 1. Responde las siguientes preguntas
- ¿Qué es un condicional?
    - Un condicional es una instruccion que realiza una operacion siempre y cuando un valor  cumpla con un(os) requisito(s). Opcionalmente, otra operacion se ejecuta si esta no cumple con dicho(s) requisito(s).
- ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?
    - `if`, `else`, `else if`: El clasico de casi cualquier lenguaje de programacion, si la condicion en la instruccion *if* se cumple, se ejecuta la operacion asociada a ella. De lo contrario, y si existe, la operacion asociada al *else* se corre. El *else if* se usa para evitar indentar una condicional *if* dentro del *else*, en caso que se tenga que otra comparasion se deba hacer.
    - `switch` `case`: Otra manera de escribir las condicionales, segun el valor asociado al `switch`, se corre la operacion al `case` respectivo. Opcionalmente, se puede correr una operacion asociada a un `default` si ningun `case` corre.
    - `?`: El operador ternario se usa para asignar valores segun una condicional.

```javascript
//Examples of each conditional operator/keyword
let value = 2;

// if, else, else if
if (value === 1) {
    //If the comparison returns true, the code here will run. The other conditionals will be skipped.
} else if (value === 2) {
    //Should the above comparison return false, but this one return true, THIS code block will be run.
} else {
    // If all other statements did not run, this code block will run.

    // Also, the else if helps to avoid the following "syntatic mess":
    if (...) {
    } else {
        if (...) {
        } else {
            // And this can go on, and on, and on. If the language allows it, please use the else-if, but do not forget to check the syntax for it.
        }
    }
}

// switch case
switch (value) {
    case 1:
        // If value is 1, run this block of code.
        break;
        //IF YOU FORGET TO ADD THE BREAK STATEMENT, THE NEXT CASE WILL RUN REGARDLESS OF THE COMPARISON RESULT.
    case 2:
        // If value is 2, run this block of code.
        break;
    default:
        // If none of the blocks of code above ran, this one will run.
        // No need to put a break here since the switch block ends anyway.
}

// Ternary operator ?
let result = value == 1 ? true : false;
```

- ¿Puedo combinar funciones y condicionales?
    - Para alistar los parametros a pasar a las funciones o como funcion que va a correr si cierta condicion se cumple, ¡Claro que si!

### 2. Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:
```javascript
const tipoDeSuscripcion = "Basic";

switch (tipoDeSuscripcion) {
   case "Free":
       console.log("Solo puedes tomar los cursos gratis");
       break;
   case "Basic":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
       break;
   case "Expert":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
       break;
   case "ExpertPlus":
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
       break;
}

// Answer
if (tipoDeSuscripcion == "Free") {
    console.log("Solo puedes tomar los cursos gratis");
} else if (tipoDeSuscripcion === "Basic") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
} else if (tipoDeSuscripcion === "Expert") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
} else if (tipoDeSuscripcion === "ExpertPlus") {
    console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
}

// No default case, no else conditional
```

### 3. Replica el comportamiento de tu condicional anterior con if, else y else if, ***pero ahora solo con if*** (sin else ni else if)
```javascript
// This is a cardinal sin. I'll see you all in the ninth circle of hell.
const tipoDeSuscripcion = "Basic";

if (tipoDeSuscripcion == "Free") {
    console.log("Solo puedes tomar los cursos gratis");
}
if (tipoDeSuscripcion == "Basic") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
}
if (tipoDeSuscripcion === "Expert") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
}
if (tipoDeSuscripcion === "ExpertPlus") {
    console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
}
```

## Ciclos

### 1. Responde las siguientes preguntas
- ¿Qué es un ciclo?
- ¿Qué tipos de ciclos existen en JavaScript?
- ¿Qué es un ciclo infinito y por qué es un problema?
- ¿Puedo mezclar ciclos y condicionales?

### 2. Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:
```javascript
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}

// Answer

let j = 0;
while (j < 5) {
    console.log(`El valor de j es: ${j}`);
    j++;
}

let k = 10;
while (j >= 2) {
    console.log(`El valor de j es: ${j}`);
    j--;
}
```

### 3. Escribe un código en JavaScript que le pregunte a los usuarios cuánto es 2 + 2. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.
```javascript
let answered = false;

while (!answered) {
    if (prompt("Cuanto es 2 + 2") != 4) {
        alert("Nope");
    } else {
        alert("Correcto!");
        answered = true;
    }
}
```

## Listas

### 1. Responde las siguientes preguntas
- ¿Que es un array?
    - Un "array", o arreglo o matriz para los hispano hablantes, es una estructura de datos congruente donde se puede almacenar varios valores/datos, a diferencia de una variable que solo puede almacenar uno. Para sacar el valor de un arreglo, se especifica el "indice" donde se ha guardado. (CABE RESALTAR QUE USUALMENTE LOS ARREGLOS INICIAN CON EL INDICE 0).
- ¿Qué es un objeto?
    - Un objeto es una estructura de datos que puede guardar valores como los arreglos. Sin embargo, en vez de usar indices los objetos usan una pareja llave-valor, donde al especificar la llave te devuelve el valor guardado. Algo a resaltar es que, aunque se parezcan a los hashmaps/diccionarios, los objetos tienen mas funcionalidad, teniendo en cuenta que se pueden crear "prototipos" de estos. Despues de todo, JS es un lenguaje orientado a objetos (aunque ***internamente*** no se usan clases).
- ¿Cuándo es mejor usar objetos o arrays?
    - Los arreglos son utiles cuando necesites iterar sobre los valores a guardar o no importa mucho que es lo que se almacena. Si necesitas control/nombrar los datos que quieras guardar, o vas a hacer programacion orientada a objetos, es mejor usar objetos.
- ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?
    - Puedes hacer arrays que guarden objetos y/u objetos cuya propiedad es un arreglo.
### 2. Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento
```javascript
function firstElement(array) {
    console.log(array[0]);
}
```
### 3. Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo)
```javascript
function printAllElements(array) {
    for (i of array) {
        console.log(i);
    }
}
```
### 4. Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo)
```javascript
function printAllProperties(obj) {
    for (i in obj) {
        console.log(`${i}: ${obj[i]}`);
    }
}
```