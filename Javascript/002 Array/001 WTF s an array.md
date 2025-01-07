An arrays is a [[Data Types||data type]] as a grupo of elements that are saves on the memory in 'manera secuencial', and can be access with [[Data Types#Number and BigInt||integer values]], [[Data Types#String||strings]], called *index.

**Content table**
- [[#Array's construction]]
- [[#How to access an array's element]]
## Array's construction

```javascript
let new Array();

// or

let array = [];
```
## How to access an array's element

To access at an array element we have to use the index between brackets `[]`.

```javascript
let array = [1, 2, 3, 4, 5, 6];

console.log(array[0]);        // return 1
console.log(array[3]);        // return 4
```

The structure of an array start on the ZERO index, if we want to access to it last element we have to search it length (`.length`) and substract `1`. 

```javascript
let array = [1, 2, 3, 4, 5, 6];

console.log(array[array.length - 1]);    // output 6
```
