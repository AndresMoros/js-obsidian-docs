The `return` keyword is how we obstain an specific value from the fuction when it's call. 

If we don't use the `return` keyword, the fuction will return `undefined` by default. 

```javascript
// With return

function sum(num1, num2) {
  return num1 + num2;
}
console.log(sum(2, 1)) // output: 3

// Without return, so the function doesn't output the sum

function sum(num1, num2) {
  num1 + num2;
}
console.log(sum(2, 1)) // output: undefined
```
