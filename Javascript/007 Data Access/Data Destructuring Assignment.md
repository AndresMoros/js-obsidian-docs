### Tabla de contenido
- [[#Object Destructuring]]
	- [[#Object default values]]
	- [[#Object property alias]]
- [[#String Destructuring]]

**Fuente:**
- [JavaScript Destructuring - W3School](https://www.w3schools.com/js/js_destructuring.asp)

---

La *destructuración* de datos funciona para *unpack* (desempaquetar, extraer) valores que se encuentran dentro de un arreglo, o bien para obtener propiedades de objetos y asignarlos a una variable. 

```js title:"Syntax"
let a, b, rest;
[a, b] = [10, 20];

console.log(a);
// output: 10

console.log(b);
// output: 20

[a, b, ...rest] = [10, 20, 30, 40, 50];

console.log(rest);
// output: Array [30, 40, 50]

```
---
## Object Destructuring

Para acceder a las propiedades de un [[Object||objeto]], deben conocerse primero los *nombres* de dichas [[Object#Propiedades de objetos||propiedades]], para así extraer su valor. Ejemplo:

```js
// Create an Object  
const person = {  
  firstName: "John",  
  lastName: "Doe",  
  age: 50  
};  
  
// Destructuring  
let {firstName, lastName} = person;
console.log(firstName)   // output: John
console.log(lastName)    //output: Doe
```

El orden en que se declaran las variables durante la asignación **NO** influye en cuanto a sus valores.

> **NOTA:** ==La destructuración **NO** destruye las propiedades, y tampoco modifica de alguna manera el objeto original.==

### Object default values

Igual que cuando se *llama* una variable que no está definida (`{js}undefined` o `{js}null`), esto puede ocurrir si declaramos una variables con un nombre que no existe entre las propiedades del objeto, o cuyo valor está vacío. Para evitar esto, usamos los [[Function Basics#Default Values||valores por defecto]]. Por ejemplo: 

```js
// Create an Object  
const person = {  
  firstName: "John",  
  lastName: "Doe",
  age: 50,
};  
  
// Destructuring  
let {firstName, lastName, country = "US"} = person;
console.log(firstName)   // output: John
console.log(lastName)    //output: Doe
console.log(country)    //output: US
```

### Object property alias

El *alias* de la propiedad de un objeto es una manera de declarar las variables para que obtengan el mismo valor de las propiedades referenciadas, pero que la variable tenga otro nombre. Por ejemplo: 

```js
// Create an Object  
const person = {  
  firstName: "John",  
  lastName: "Doe",
  age: 50,
};  
  
// Destructuring  
let {firstName : name} = person;
console.log(name)   // output: John
```
---

## String Destructuring

La destructuración de datos puede usarse para extraer caracteres de una [[Data Types#String||cadena]].

```js
// Create a String  
let name = "Kuker";  
  
// Destructuring  
let [a1, a2, a3, a4, a5] = name;
console.log(a1,a2,a3); //output: Kuk
```
---
## Array Destructuring

Se pueden asignar valores a variables provenientes de un [[WTF s an array||array]]. Por ejemplo:

```js
//Declare an array
const fruits = ["Bananas", "Oranges", "Apples", "Mangos"];  
  
// Destructuring  
let [fruit1, fruit2] = fruits;
console.log(fruit2) //output: Oranges
```

> **Nota:** En este caso el orden en que estén los elementos del array **SI** importa para asignar los valores de las variables.
---
### Skipping Array Values

```js
// Create an Array  
const fruits = ["Bananas", "Oranges", "Apples", "Mangos"];  
  
// Destructuring  
let [fruit1,,,fruit2] = fruits;
console.log(fruit2) //output: Apples
```
---
### Array Position Values

Es posible asignar el valor de un elemento específico de un array si se conoce el índice exacto. Por ejemplo:

```js
// Create an Array  
const fruits = ["Bananas", "Oranges", "Apples", "Mangos"]; 

// Destructuring  
let {[0]:fruit1 ,[3]:fruit2} = fruits;
console.log(fruit2) //output: Mangos
```
---
### The Rest Property

Puedes asignar valores de elementos específicos de un array, y guardar los sobrantes en una variables aparte. Esto se hace escribiendo una secuencia de tres puntos (`...`) antes de declarar el nombre de la nueva variable. Por ejemplo:

```js
// Create an Array  
const numbers = [10, 20, 30, 40, 50, 60, 70];  
  
// Destructuring  
const [a,b, ...rest] = numbers
console.log(rest) //output: [30, 40, 50, 60, 70]
```