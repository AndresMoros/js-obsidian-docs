The sintax of an `arrow fuction` does not requiere the [[Function Basics||function]] keyword, and implemate a fat arrow ==`=>`== to separate the parameters from the function's body.

The arrow functions have the following characteristics or variants:

- The arrow fuctions with only one parameter don't requiere `()` around the parameter list. 
- The ones without parameter and a list of them requiere `()` 

Arrow function with no arguments:

```javascript
const printHello = () => {
  console.log('hello');
};

printHello();
// Output: hello`
```

Arrow function with a single argument:

```javascript
const checkWeight = (weight) => {
  console.log(`Baggage weight : ${weight} kilograms.`);
};

checkWeight(25);
// Output: Baggage weight : 25 kilograms.
```

Arrow function with two arguments:

```javascript
const sum = (firstParam, secondParam) => {
  return firstParam + secondParam;
};

console.log(sum(2, 5));
// Output: 7
```

Concise arrow function:

```javascript
const multiply = (a, b) => a * b;

console.log(multiply(2, 30));
// Output: 60
```
