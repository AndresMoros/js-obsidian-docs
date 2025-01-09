Una declaración o bloque `if` se entiende como una estructura 'condicional', ya que evalúa si una expresión es `true`, para así ejecutar una instrucción, o él código que contiene.

```javascript
if(5 < 8) {
	console.log(the expresion is true)
} else {
	console.log(the expresion is false)
}
```

Las expresiones pueden ser operaciones matemáticas, comparaciones de valores, llamadas a otras funciones o el valor de un variable. En caso de ser `false` se ejecutará el bloque de código seguido del `else`.

```javascript
let trueValue = 1;
let falsyValue = 0;

function compare(num1, num2){
	return num1 > num2 ? true : false;
}

if(compare(trueValue, falsyValue)) {
	console.log("That's true!");
} else {
	console.log("That's false!");
}
// output: "That's true!"

if(trueValue) {
	console.log("A truly value can be a number over 0 or a string with, at least 1 character");
} else {
	console.log("A falsy value can be 0 or an empty string");
}
// output: "A truly value can be a number over 0 or a string with, at least 1 character"

if(falsyValue) {
	console.log("A truly value can be a number over 0 or a string with, at least 1 character");
} else {
	console.log("A falsy value can be 0 or an empty string");
}
// output: "A falsy value can be 0 or an empty string";

```

Puedes concatenar varios `if` usando la estructura de `else if`, y así agregar más complejidad a tu código. Esto funciona si nuestra declaración puede tener más de dos (2) valores con los que queramos interactuar.

```javascript
let score = 10;

function winOrLose() {
	if (score == 10) {
		console.log('Perfect!');
	} else if (score >= 6) {
		console.log('Nice!');
	} else if (score >= 2) {
		console.log('You can do it better!');
	} else {
		console.log('You lose!');
	}
}

winOrLose(); // output: Perfect!

score = 8;
winOrLose(); // output: Nice!

score = 1; 
winOrLose(); // output: You lose!
```