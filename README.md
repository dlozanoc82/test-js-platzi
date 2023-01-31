# Test JavaScript PLATZI 🚀
## Instrucciones

* Evalúa muy críticamente tu conocimiento.
* Si logras resolver la prueba, no importa cuánto te cueste, puedo asegurarte que tienes todo para continuar a las siguientes clases y tomar el resto del curso.
* Si no lo logras, no te preocupes, absolutamente nadie puede juzgarte, solo tú.
* Vuelve al Curso Básico de JavaScript, anota los temas clave donde puedes mejorar,
ubica las clases donde puedes aprenderlos y estudia vigorosamente.
* Es completamente válido hacer búsquedas en Google, cursos y tutoriales de Platzi, incluso usar tu cuaderno de notas sin importar si es físico o virtual.

Recuerda que el éxito no se mide por cuánto tiempo te toma aprender, esa métrica es relativamente inútil. Mejor concéntrate en completar los cursos de tu ruta de aprendizaje profesional y desarrollar los proyectos que realmente demuestran que dominas cada tecnología.

¡Mucha suerte!

## Variables y Operaciones
1️⃣ Responde las siguientes preguntas en la sección de comentarios:

* ¿Qué es una variable y para qué sirve?
> Una variable es un espacio en memoria, que se encarga de almacenar un tipo de dato.
* ¿Cuál es la diferencia entre declarar e inicializar una variable?
> Declarar corresponde a la accion de crear una variable con algun nombre significztivo. En cambio, Inicializar corresponde a asignarle un valor a esa variable.
```js
var edad; //Declarar
edad = 30; // Inicializar 
```
* ¿Cuál es la diferencia entre sumar números y concatenar strings?
> La concatenacion consiste en unir dos bloques String para formar una frase, en cambio, sumar dos numeros arroja el resultado de una operacion aritmetica de suma.
* ¿Cuál operador me permite sumar o concatenar?
> El operador aritmetico suma (+)

2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:

* Nombre: string 
* Apellido: string 
* Nombre de usuario en Platzi: string
* Edad: number
* Correo electrónico: string
* Mayor de edad: boolean
* Dinero ahorrado: number
* Deudas: number

3️⃣ Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.
```js
let nombre = 'Daniel';
let apellido = 'Lozano';
let username = 'dlozano82';
let edad = 22;
let email = 'dcardoso122@gmail.com';
let esMayorDeEdad = true;
let dineroAhorrado = 1200000;
let deudas = 0;
```
4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:
* Nombre completo (nombre y apellido)
* Dinero real (dinero ahorrado menos deudas)
```js
let nombreCompleto = nombre + ' ' + apellido;
let dineroReal = dineroAhorrado - deudas;
console.log(nombreCompleto);
console.log(dineroReal);
```

## Funciones

1️⃣ Responde las siguientes preguntas en la sección de comentarios:
* ¿Qué es una función?
> Las funciones son bloques de código que solucionan un problema especifico. 
* ¿Cuándo me sirve usar una función en mi código?
> Cuando existen tareas repetitivas (variables o bloques de codigo), para que puedan ser facilmente reutilizadas. Además nos sirve para mejorar la legibilidad de nuestro codigo. 
* ¿Cuál es la diferencia entre parámetros y argumentos de una función?
> Los parametros son los datos que necesita una funcion para ejecutar el bloque de codigo. En cambio, los argumentos son los datos que se envian cuando se invoca la función.

2️⃣ Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

```js
function saludo(name, lastname, nickname){
   let completeName = name + ' ' + lastname;
   console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
}

saludo('Daniel Alexander', 'Lozano Cardoso', 'Dani');
```

## Condicionales
1️⃣ Responde las siguientes preguntas en la sección de comentarios:
* ¿Qué es un condicional?
> Un condicional es una estructura que permite evaluar dos o mas expresiones y realizar determinadas acciones en JavaScript.
* ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?
> IF(else y else if) y switch. 
> En el caso de Switch se valida siempre con la misma variable o condicion definida en el switch. Mientras que el condicional IF(else y else if) permite hacer combinaciones completamente distintas. 
* ¿Puedo combinar funciones y condicionales?
> Si, las funciones pueden encapsular cualquier bloque de codigo.

2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:
> Original
```js
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
> Replica
```js
let tipoDeSuscripcion = "Basic";

if (tipoDeSuscripcion == 'Free'){
   console.log("Solo puedes tomar los cursos gratis");
}else if (tipoDeSuscripcion == 'Basic'){
   console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
}else if (tipoDeSuscripcion == 'Expert'){
   console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
}else if (tipoDeSuscripcion == 'ExpertPlus'){
   console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
}else {
   console.log("No tienes una cuenta en platzi");
}
```

3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).
💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays u objetos y un solo condicional. 😏

```js

const tipoDeSuscripciones = {
   free: 'Solo puedes tomar los cursos gratis',
   basic: 'Puedes tomar casi todos los cursos de Platzi durante un mes',
   expert: 'Puedes tomar casi todos los cursos de Platzi durante un año',
   expertPlus: 'Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año',
}

function conseguirTipoSuscripcion(suscripcion){
   if(tipoDeSuscripciones[suscripcion]){
      console.log(tipoDeSuscripciones[suscripcion])
      return;
   }
   console.warn('Este tipo de suscripcion no existe')
}

```

## Ciclos
1️⃣ Responde las siguientes preguntas en la sección de comentarios:
* ¿Qué es un ciclo?
> Es la forma de ejecutar un bloque de codigo hasta que se cumpla cierta condicion
* ¿Qué tipos de ciclos existen en JavaScript?
> While, for, do while
* ¿Qué es un ciclo infinito y por qué es un problema?
> Es cuando la validacion de nuestros condicionales no se cumple y termina dañando la aplicacion.
* ¿Puedo mezclar ciclos y condicionales?
Si. los ciclos pueden encapsular cualquier bloque de codigo

2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:
>Original
```js
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}
```
>Replica
```js
let i=0;

while(i<5){
   console.log("El valor de i es: " + i);
   i++;
}

let j=10;

while(j>=2){
   console.log("El valor de j es: " + j);
   j--;
}

```
3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es 2 + 2. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.
💡 Pista: puedes usar la función prompt de JavaScript.
```js

let respuesta;

while(respuesta != '4'){
   let pregunta = prompt('¿Cuanto es 2 + 2?')
   respuesta = pregunta;
}

```
## Listas 

1️⃣ Responde las siguientes preguntas en la sección de comentarios:
* ¿Qué es un array?
> Es una lista de elementos.
```js
const array = [1, "Dos", true, false];
```
* ¿Qué es un objeto?
> Es una lista de elementos, pero cada elemento tiene un nombre clave.
```js
const obj = {
   nombre: 'Fulanito',
   edad: 12,
   comidasFavoritas: ['Pollo', 'Helado'],
};
```
* ¿Cuándo es mejor usar objetos o arrays?
> Arrays cuando lo que haremos en un elemento es lo mismo que en todos los demás(la regla se puede incumplir). Mientras que en un objeto cuando los nombres de cada elemento son importantes para nuestro algoritmo.
* ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?
> Si. Los arrays pueden guardar objetos, y los onjetos pueden guardar arrays entre sus propiedades.

2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.
```js
function imprimirPrimerElementoArray(arr){
   console.log(arr[0]);   
}

```


3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).
```js
function imprimirElementoPorElemento(arr){
   for(i=0; i < arr.length; i++){
      console.log(arr[i])
   } 
}
```


4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).
```js
Object.values(obj);
```
