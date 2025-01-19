**Fuente:**
- [Cómo entender la recursividad en JavaScript](https://www.freecodecamp.org/espanol/news/como-entender-recursividad-en-javascript/)


---
```js
const countDownAndUp = (number) => {
  console.log(number);
  if (number === 0) {
    console.log("Reached base case");
    return;
  } else {
    countDownAndUp(number - 1);
    console.log(number);
  }

};
countDownAndUp(3);
```
