Un objeto en JavaScript, igual que en otros lenguajes, es posible compararlos con objetos de la vida real. Por ejemplo, una taza: una taza es un objeto que cuenta con propiedades tales como sus dimensiones, peso, color y diseño. 

Existen varios tipos de objetos. Algunos tiene propiedades ligadas a funciones, los cuales se determinan *métodos*, por ejemplo el método [[Array methods|.push()]] de los objetos [[WTF s an array||array]]. 

---
## Propiedades de objetos
Los objetos pueden contener en su interior varias *propiedades*, las cuales pueden tomarse como una variable relacionada con el mismo objeto. Pueden ser tratadas como variables normales en JavaScript, con la diferencia de estar ligadas al objeto al que pertenecen. Se puede acceder a las propiedades de los objetos con una notación de punto (`.`), por ejemplo:

```javascript title:"Accediendo a una propiedad"
//Ejemplo genérico
objectName.propertyName;

//Ejemplo práctico:
const carsMaker = ["Ford", "Chevrolet", "Ferrari", "Volkswagen"]
// Los arrays son objetos que cuentan con la propiedad 'length', y se accede a ella de la siguiente manera.

console.log(carsMaker.length) // output: 4
```

**NOTA:** Nombre de las propiedades 
Al igual que las variables comunes, son sensibles a las minúsculas y mayúsculas

---
## Crear propiedades de un objeto
Las propiedades puedes crearse usando la notación del punto antes mencionada y asignándoles un valor. Para demostrarlo, vamos a crear un objeto llamada `myCar` y se le agregarán propiedades con este método:

```javascript title:"Agregando propiedades a un objeto"
var myCar = new Object();
myCar.make = "Ford";
myCar.model = "Mustang";
myCar.year = 1969;

```

## Iniciador de objeto

Lo anterior también puede hacerse con un *iniciador de objetos*, que se trata de una lista de 0 o más nombres de propiedades y valores, delimitados entre sí por comas, y se encierran entre llaves (`{}`). Por ejemplo:

```javascript title:"Usando iniciador de objetos"
// Ejemplo de estrutura
var obj = {
	propertyName: propertyValue,
	propertyName: propertyValue,
}

// Ejemplo práctico
var myCar = {
	make: "Ford",
	model: "Mustang",
	year: 1969,
}
```

En caso de que la propiedad no esté definida, su valor estará como `undefined` (y `null`).

```javascript title:"Consultando una propiedad vacía"
console.log(myCar.color) //output: undefined
```

