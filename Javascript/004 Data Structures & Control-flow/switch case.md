Una sentencia `{js}switch` es una instrucción para el flujo de trabajo, que lleva el control sobre una `{js}expression` contra varios casos de lo que debe hacer el programa.  

**Fuente:**
[ES - JavaScript switch case: Ejemplo de sentencias switch en JS](https://www.freecodecamp.org/espanol/news/javascript-switch-case-ejemplo-de-sentencias-switch-en-js/)
[EN - JavaScript Switch Case – JS Switch Statement Example](https://www.freecodecamp.org/news/javascript-switch-case-js-switch-statement-example/)
## Sintaxis básica de una sentencia switch

```js title:"Ejemplo genérico"
switch (expression) {
  case 1:
   //this code will execute if the case matches the expression
    break;
  case 2:
   //this code will execute if the case matches the expression
    break;
  case 3:
   //this code will execute if the case matches the expression
    break;
  default:
    //this code will execute if none of the cases match the expression
    break;
}
```

## Funcionamiento

Para llevar a cabo el control de flujo, la computadora deberá verificar cada caso en la sentencia `{js}switch`, comparándola estrictamente (`{js}===`) cada `{js}case`. Si alguno de los casos coincide con la `{js}expression`, el código de esa cláusula se ejecutará.

#### Sin coincidencias

En caso de que ninguno de los casos coincida con la expresión, la cláusula `{js}default` (por defecto) se ejecutará. 

#### Múltiples coincidencias

En caso de que varios casos coincidan con la expresión, la cláusula a ejecutar será la primera en coincidir, es decir, la primera que haga `{js}match` leída de arriba hacia abajo. 

#### `{js}break`

La declaración `break` le dice a la computadora que, una vez terminada la tarea descrita en la cláusula, se detenga y así no ejecute las instrucciones o casos siguientes. Si no se usa, la computadora ejecutará los casos siguientes. 

Si el código dentro de la cláusula `case` posee la palabra clave [[Return keyword||return]] entonces no hace falta usar `{js}break`