## What a `{js}fuction` is

A `function` is a reusable set of statements used to perform a task or get a value. A `fuction` can be passed one or more values and it'll return a value at the end of the execution. 

## Function declaration

Fuction declaration are used to create 'named fuctions'. These fuctions can be *called* using the declared name. The structure used to declare a fuction is: 

- Use the `fuction` keyword for indicate that the next will be the fuction's name. 
- The fuction's name. Is recomended use camel case type with this. 
- Parentheses.
- An optional list of parameters separetes by comas (`,`) enclosed by the parentheses.
- A fuction body enclosed in a set of curly braces `{}`.

For example:

```javascript
function sum(number1, number2) {
	console.log(sum(number1 + number2));
}
sum(30, 2) // Prints 31
```

## Calling Fuctions

Functions can be called, or executed, elsewhere in code using parentheses following the function name. When a function is called, the code inside its function body runs. Arguments are values passed into a function when it is called.

```javascript
// Defining the function

function sum(num1, num2) {

  return num1 + num2;

}

// Calling the function

console.log(sum(2, 4));

// Output 6
```

## Optional Arguments

In JavaScript functions will run whether or not they have the intended number of arguments. If more than the number required are submitted, the function will use the required number and ignore the rest. If fewer arguments are provided than required, the other values will be set to `undefined`.

```javascript
console.log(sum(2, 4, 8)); // Output 6  

console.log(sum(2)); // Output NaN
```

## Default Values

Functions can also be defined with default values for one, or all of the parameters. If no arguments are passed the default values are used, if arguments are included they will override the default values.

```javascript
// Defining the function with default values

function sum(num1 = 6, num2 = 1) {

  return num1 + num2;

}

// Calling the function

console.log(sum(8));

// Output 9
```
