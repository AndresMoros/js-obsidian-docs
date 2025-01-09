## **Tabla de contenido**

- [[#Add new elements]]
- [[#In Array's elements insertion]]
- [[#Most use methods for arrays]]

**Fuente:**
[Integración de componentes de software en páginas web (2023)](https://www.ra-ma.es/libro/mf0951-2-integracion-de-componentes-software-en-paginas-web_148555/)

Métodos para interactuar y trabajar con arrays en JavaScript. 
## Add new elements

### `{javascript}.push()`
Con el método `.push()` se puede agregar un elemento nuevo a un array existente. El método `.push()` toma un parametro, que es el elemento que deseamos introducir en el array. Por ejemplo:

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7];
arr[6] = 13;
arr.push(21);

console.log (arr);                                //output: [1, 2, 3, 4, 5, 13, 7, 21]
console.log (arr[7]);                             //output: 21
```

##### In Array's elements insertion
NO es posible añadir elementos a elementos dentro de un mismo array si estos no están configurados como un array en sí mismo. Por ejemplo: 

```javascript
const array = new Array(0, 1, 2, 3, 4, 5);
array[0] = new Array()
array[0].push('doritos', 'cheese', 'rice');

console.log(array);                  //output [["doritos","cheese","rice"],1,2,3,4,5]

array[0][0] = 'milk';

console.log(array);                  //output [["milk","cheese","rice"],1,2,3,4,5]
```

## Delete elements from Arrays
Hay dos métodos o instrucciones para eliminar elementos de un array: `delete(index)` y `.splice(index, numOfElements)`. 

### `{javascript}delete` sentence
La instrucción de  `delete` establece el valor del elemento como `empty`, pero conserva la posición en el índice y la memoria.

```javascript
const array = new Array(0, 1, 2, 3, 4, 5);
delete(array[4]);

console.log(array);                // [0,1,2,3,null,5]
```

### `{javascript}.splice()` method
El método `.splice()` es capaz eliminar elementos especificados en el array original, y con ello de devolver (`return`) un array nuevo con los elementos eliminados. Este método toma dos parámetros, el primero indica el índice desde el cual se empezarán a eliminar los elementos, y el segundo cuántos elementos se deben eliminar desde la posición indicada en el primero. Por ejemplo: 

```javascript
const array = new Array(0, 1, 2, 3, 4, 5);
console.log(array);                         // [0, 1, 2, 3, 4, 5]

// -----------------------------------------------

const substracElements = array.splice(3, 2);
console.log(substracElements);              // [3, 4]
console.log(array);                         // [0, 1, 2, 5]
```

## Most use methods for arrays

### `{javascript} .filter()`
El m `.filter()` funciona por medio de una `function` y da como resultado un array con los elementos que cumplan con la condición que se específique, sin alterar el array original. Por ejemplo:

```javascript
// .filter() para Arrays:

let fruits = ['Apple', 'Orange', 'Banana', 'Pear'];
let largeFruits = fruits.filter(x = (x) => {
	return x.length > 4;
});

console.log(largeFruits) 
// Output: ["Apple","Orange","Banana"]

// -----------------------------------------------

// .filter() para Objects: 
const personas = [
  { nombre: "Juan", edad: 20 },
  { nombre: "Ana", edad: 25 },
  { nombre: "Carlos", edad: 15 }
];

const mayoresDeEdad = personas.filter(persona => persona.edad >= 18);
console.log(mayoresDeEdad);
// Output: [ { nombre: "Juan", edad: 20 }, { nombre: "Ana", edad: 25 } ]
```

### `{javascript}.join()`
El método `.join()` da como resultado un [[Data Types#String|string]] con todos los elementos de un array. Es capaz de recibir un argunmento, que es lo que se usará para separar a los elementos del array dentro de la cadena de texto, por defecto es una coma (`,`). Por ejemplo:

```javascript
let numbers = [1, 2, 3, 4, 5];
let stringNumbers = numbers.join("|");

console.log(stringNumbers) // Output: "1|2|3|4|5"
```

### `{javascript}.indexOf()`

Este método devuelve como resultado el primer índice de un elemento de un [[WTF s an array||array]]. Tiene dos parámetros: el elemento buscado (obligatorio) y el índice apartir del cual se empieza la búsqueda (opcional). Por defecto, el índice es `0`, por lo que, a menos que se le indique desde qué índice debe comenzar la búsqueda siempre lo hará desde el principio. Por ejemplo:

```javascript
const brands = ['Apple', 'Samsung', 'Google', 'OnePlus', 'Huawei', 'Xiaomi', 'Oppo', 'Vivo'];

// indexOf con una función anónima: 

const whereIsMyBrand = (brand) => {
    return brands.indexOf(brand);
};
console.log((whereIsMyBrand('Apple')));                 // Output: 0

// -----------------------------------------------

// Can also be used like

const iSearchinMyBrand = brands.indexOf('Vivo');

// -----------------------------------------------

```

Si NO encuentra el elemento específicado devolverá el valor de `-1`, por ejemplo:

```javascript
const brands = ['Apple', 'Samsung', 'Google', 'OnePlus', 'Huawei', 'Xiaomi', 'Oppo', 'Vivo'];

const imNotGonnaFindMyBrand = brands.indexOf('Google', 3);
const myBrandNotExist = brands.indexOf('Nokia');

console.log(imNotGonnaFindMyBrand)        // Output: -1
console.log(myBrandNotExist)              // Output: -1
```

Importante mencionar que es *case sensitve*. 

### `{javascript}lastIndexOf()`

