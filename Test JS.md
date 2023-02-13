## Respuestas al Test de JavaScript
## Variables y operaciones
### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:
- ¿Qué es una variable y para qué sirve?
Cajitas (espacios en memoria) donde podemos guardar información (dependiendo de los tipos y estructuras de datos que soporte nuestro lenguaje).

- ¿Cuál es la diferencia entre declarar e inicializar una variable?
Declarar es cuando le decimos a JavaScript que vamos a crear una variable con el nombre tal mientras que inicializar (o reinicializar) es asignarle un valor a esa variable.

- ¿Cuál es la diferencia entre sumar números y concatenar strings?
- ¿Cuál operador me permite sumar o concatenar?

EL operador que nos permite sumar o concatenar es +. Este operador nos permite sumar números cuando lo usamos con números. Pero cuando los strings, lo que hace es unir (concatenar, así se dice) ambos strings.

### 2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:

- Nombre: string
- Apellido: string
- Nombre de usuario en Platzi: strig (@NaviG)
- Edad: number
- Correo electrónico: string (ivancarlosqp@gmail.com)
- Mayor de edad: boolean
- Dinero ahorrado: number
- Deudas: number

### 3️⃣ Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.

```
let nombre = 'Ivan Carlos';
let apellido = 'Quispe Patty';
let username = 'NaviG11';
let edad = 24;
let mail = 'ivancarlosqp@gmail.com';
let esMayorDeEdad = true;
let dineroAhorrado = 1000;
let deudas = 100;
```

### 4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

- Nombre completo (nombre y apellido)
- Dinero real (dinero ahorrado menos deudas)

```
let nombreCompleto = nombre + ' ' + apellido;
let dineroReal = dineroAhorrado - deudas;
```

## Funciones

### 1️⃣ Responde las siguientes preguntas:
- ¿Qué es una función?
   Un bloque de código que trabaja en un scope local.
   Nos permite encapsula en un bloques de código.
   Nos ayuda a reutilizarlos más adelante.
   
- ¿Cuándo me sirve usar una función en mi código?
   Nos sirve cuando tenemos variables o bloques de código muy parecidos que podemos encapsular para reutilizar más de una vez en el futuro.
   También nos sirve para ordenar y mejorar nuestro código.
   
- ¿Cuál es la diferencia entre parámetros y argumentos de una función?
   Usamos los parámetros al declarar nuestra función y argumentos en el momento de llamar dicha función.
   Funciones(parámetros)
   Enviamos argumentos cuando la ejecutamos.
   
   
### 2️⃣ Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

```
const name = "Ivan Carlos";
const lastname = "Quispe Patty";
const completeName = name + lastname;
const nickname = "NaviG";

console.log("Mi nombre es " + completeName + ", pero prefiero que me llames " + nickname + ".");
```
Solution to problem
```
function nombreCompleto(name, lastname) {
  return name +' '+ lastname;
}
function saludo(name, lastname, userName) {
	const completeName = nombreCompleto(name, lastname);
  console.log(`Mi nombre es ${completeName}, pero prefiero que me llames ${userName}`);
}
saludo("Ivan", "Quispe", "NaviEleven");
```

## Condicionales

### 1️⃣ Responde las siguientes preguntas:
- ¿Qué es un condicional?
   Son la forma en que ejecutamos un bloque de código u otro dependiendo de alguna condición o validación.
      
- ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?
   If (else, else if), Switch
   IF: nos permite hacer validaciones completamente distintas en cada validación o condicional.
   SWITCH: todos los cases sse comparan con la misma variable o condición que definimos en el switch.
   
- ¿Puedo combinar funciones y condicionales?
   Sí, las funciones pueden encapsular cualquier bloque de código, incluyendo condicionales.
   
### 2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:

```
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
```
Solution
```
if (tipoDeSuscripcion == 'Free') {
    console.log("Solo puedes tomar los cursos gratis");
} else if (tipoDeSuscripcion == 'Basic') {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
} else if (tipoDeSuscripcion == 'Expert') {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
} else if (tipoDeSuscripcion == 'ExpertDuo') {
    console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
}
```

### 3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).

> 💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays y un solo condicional. 😏
- Bonus
```
```
const tiposDeSuscripciones = {
    free: 'Solo puedes tomar los cursos gratis',
    basic: 'Puedes tomar casi todos los cursos de Platzi durante un mes',
    expert: 'Puedes tomar casi todos los cursos de Platzi durante un año',
    expertduo: 'Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año',
};

function conseguirTipoSuscripcion(suscripcion) {
    if (tiposDeSuscripciones[suscripcion]) {
        console.log(tiposDeSuscripciones[suscripcion]);
        return;
    }

    console.warn('Ese tipo de suscripción no existe')
}
```
```

## Ciclos

### 1️⃣ Responde las siguientes preguntas:
- ¿Qué es un ciclo?
   La forma de ejecutar un bloque de código hasta que se cumpla cierta condición.
   
- ¿Qué tipos de ciclos existen en JavaScript?
   While, Do while y For.
   
- ¿Qué es un ciclo infinito y por qué es un problema?
Es cuando la validación de nuestros condicionales nunca se cumple y termina toteando (dañando) la aplicación (e.j. cuando el navegador ya no puede más de tanta ejecución de ese bloque de código).

- ¿Puedo mezclar ciclos y condicionales?
   Sí, auque los ciclos son una especie de condicionales, nada nos impide agregar más condicionales dentro del ciclo.
### 2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:

```
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}
```
Solution
```
while (i < 5) {
    console.log("El valor de i es: " + i);
    i++;
}

while (i >= 2) {
    console.log("El valor de i es: " + i);
    i--;
}
```
### 3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es `2 + 2`. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.

> 💡 Pista: puedes usar la función prompt de JavaScript.
Solution
```
while (respuesta != '4') {
    let pregunta = prompt('¿Cuánto es 2 + 2?')
    respuesta = pregunta;
}
```
## Listas

### 1️⃣ Responde las siguientes preguntas:

- ¿Qué es un array?
   Es una lista de elementos.
```
const array = [1, 'jaja', true, false, { nombre: 'lala', edad: 3 }];
```
- ¿Qué es un objeto?
   Es una lista de elementos PERO cada elemento tiene un nombre clave.
```
const obj = {
   nombre: 'Fulanito',
   edad: 3,
   comidasFavoritas: ['Pollo frito', 'vegetales'],
};
```   
- ¿Cuándo es mejor usar objetos o arrays?
   Arrays cuando lo que haremos en un elemento es lo mismo que en todos los demás (la regla se puede incumplir).
   Mientras que un objeto cuando los nombres de cada elemento son importantes para nuestro algoritmo.
   
- ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?
   Sí, los arrays pueden guardar objetos. Y los objetos pueden guardar arrays entre sus propiedades.

### 2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.
```
function imprimirPrimerElementoArray(arr) {
    console.log(arr[0])
}
```
### 3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).
```
function imprimirElementoPorElemento(arr) {
    for (let i = 0; i < arr.length; i++) {
        console.log(arr[i])
    }
}
//Podemos usar la funcion forEach()
```
### 4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).
```
function imprimirElementoPorElementoObjeto(obj) {
    const arr = Object.values(obj);
    for (let i = 0; i < arr.length; i++) {
        console.log(arr[i])
    }
}
//Object.values(obj)
```
