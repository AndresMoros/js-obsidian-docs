
### **Content Table**

- [[#Arithmetic Operators]]
- [[#Other Assignment Operators]]
- [[#Comparison Operators]]
- [[#Logical Operators]]
- [[#Conditional Operator]]

**Source:**
- [Codecademy | JavaScript's Operators](https://www.codecademy.com/resources/docs/javascript/operators)

---

## Arithmetic Operators

These operators are used to perform arithmetic on numeric values:

- `+`: Adds to a value; can also be used to concatenate [[Data Types#String||strings]]
- `-`: Subtracts from a value.
- `*`: Multiplies by a value.
- `/`: Divides by a value.
- `%`: [Modulo](https://www.codecademy.com/resources/docs/general/modulo) finds the remainder after dividing two values.
- `**`: Returns the exponentiation of the first value raised to the power of the second value (first introduced in ES2016).
- `++`: Returns the value incremented by 1.
- `--`: Returns the value decremented by 1.

The operators can be implemented as seen below:

```javascript
let sum = 5 + 5; // print 10

let difference = 10 - 5; // print 5`

let product = 5 * 10; // print 50`

let quotient = 10 / 5; // print 2`

let remainder = 10 % 5; // print 0`
```
---
## Other Assignment Operators

An assignment operator assigns a value to its left operand based on the value of its right operand:

- `+=`: Adds and assigns a new value to a variable.
- `-=`: Subtracts and assigns a new value to a variable.
- `*=`: Multiplies and assigns a new value to a variable.
- `/=`: Divides and assigns a new value to a variable.
- `%=`: Assigns the returned remainder (modulo) as a new value to a variable.
- `**=`: Assigns the left operand raised to the power of the right operand.

The following example showcases how these operators are a combination of using an assignment and arithmetic operator in one statement:

```javascript
let number = 100;

// Both statements will add 10

number = number + 10;

number += 10;

console.log(number);

// Output: 120
```
---
## Comparison Operators

These operators compare values and return a [boolean](https://www.codecademy.com/resources/docs/general/data-types/boolean) value of `true` or `false`.

- ==`==`==: Returns `true` or `false` based on whether the value of two operands are equal.
- ==`===`==: Returns `true` or `false` based on whether the value and type of two operands are equal.
- ==`!=`==: Returns `true` or `false` based on whether the value of two operands are not equal.
- ==`!==`==: Returns `true` or `false` based on whether the value and type of two operands are not equal.
- ==`>`==: Returns `true` or `false` based on whether the first value is greater than the second value.
- ==`<`==: Returns `true` or `false` based on whether the first value is less than the second value.
- ==`>=`==: Returns `true` or `false` based on whether the first value is greater than or equal to the second value.
- ==`<=`==: Returns `true` or `false` based on whether the first value is less than or equal to the second value.

**NOTE:** The `==` and `===` comparison operators are not to be confused with the single equality sign `=` operator that is used for assignment.

The following example showcases some of these comparison operators:

```javascript
let tenString = '10';

let numberTen = 10;

console.log(tenString == numberTen);

// Output: true

console.log(tenString === numberTen);

// Output: false

console.log(tenString != numberTen);

// Output: false

console.log(tenString !== numberTen);

// Output: true
```

## Logical Operators

These operators combine multiple boolean expressions or values to provide a single boolean output:

- ==`&&`== (AND): Returns `true` if all operands evaluate to `true`.
- ==`||`== (OR): Returns `true` if one or more operands evaluate to `true`, also can be used for set a value from a expected variable.
- ==`!`== (NOT): Returns the logical opposite of an operand’s boolean value (i.e., `!(true)` returns `false` and `!(false)` returns `true`).

The following example showcases the usage of logical operators:

```javascript
const walksLikeADuck = true;
const talksLikeADuck = true;

// AND Operator
let isDuck = walksLikeADuck && talksLikeADuck;
console.log(isDuck);
// Output: true

const isBird = true;
const isPlane = false;

// OR Operator
isDuck = isBird || isPlane;
console.log(isDuck);
// Output: true
const anotherBird = isBird || isPlane
// Output: true

// NOT Operator
const isPenguin = !isDuck;
console.log(isPenguin);
// Output: false
```

> **About OR (||) operator:**
> This operator check the first statement at the beggining, if it's `true` the second one won't be check. 

## Conditional Operator

The conditional, or ternary, operator uses the question mark `?` and colon `:` to assign a value to a variable based on a conditional statement:

```javascript
variable = condition ? assignedIfTrue : assignedIfFalse;
```

This operator combines the functionalities of the assignment, comparison, and logical operators.

For example

```javascript
const anyNumber = 10;
const otherNumber = 5;

let passOrNotPass = (anyNumber > otherNumber) ? console.log('Correct') : console.log ('Incorrect')

// this will print 'Correct' because anyNumber actually is greather than otherNumber
```