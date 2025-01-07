**Content Table**
- [[#String]]
- [[#Number & BigInt]]
- [[#Boolean]]
- [[#Null and Undefined]]
- [[#Objects]]
**Source:
[Codecademy | JavaScript's Data Type](https://www.codecademy.com/resources/docs/javascript/data-types)

## String
The string can be declareted using double quotes (`""`) or single qoutes (`''`). Even, with inverted quotes, this one is use for make templates literals on JavaScript using interpolation.

For example:

```javascript title:"String data type"
let stringX = 'single quotes'
let stringY = 'double quotes'

let varible = 'quotes'
let stringZ = `inverted ${variable}` // Will print 'inverted quotes'

```
---
## Number and BigInt

In JavaScript the numbers are stored as double-precision floating point number, it means that can represent integers and decimal numbers, as `1` or `0.82`. 

==For example:==

```javascript
let num = 12;
console.log(num) // The input will be 12
```

However, the `Number` data type is limited to a number of 15 digits. Above that number, the precision of `Number` is lost, leading to errors. That is where `BigInt` is applied.

If we wanna represent whole big number, we have to write the number with a `n` at the end of it.

==For example:==

```javascript
let num = 9999999999999999;
let bigNum = 9999999999999999;

console.log(num);    // the output will be 10000000000000000
console.log(bigNum); // the output will be 9999999999999999n
```
---
## Boolean

A `boolean` data type use truthy or falsy values, as `true` or `false`.

The `boolean` types can be use for conditional structures, logical operators and conditional operators.

==For example:==

```javascript
let isEarthRound = true;
let isEarthFlat = false;
```
---

## Null and Undefined

The type `null` and `undefined` represent the absence of a value, but they have diferents meanings.

```javascript
// Undefined means there should be some values, but it is undefined now

let finishCourseTime = undefined;

// Null means there is no value here

let finishStudyingDate = null;
```

`undefined` is applies when a value is not returned, like a empty variable's call. 

`null` is used intentionally for developers to indicate to the variable doesn't need a value at the moment. 

> **NOTE: Falsy with `null` and `undefined`**
> Both values can be understan as `false` on boleean contexts, 'cause any value under one *(0, -1, -2...)* incluiding, and empty strings are interpreted as `false`. To be more precise with using these, we have to do use of strict comparition operator (`===`).


