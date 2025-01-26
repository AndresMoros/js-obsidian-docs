### **Tabla de contenido**
- [[#bubbleSort]]
- [[#selectionSort]]
- [[#insertionSort]]

**Fuente:**
- [Bubble sort - Include Poetry](https://www.include-poetry.com/Code/C++/Metodos/Ordenamientos/Bubble-sort/)
- [Selection sort - Geeks for Geeks](https://www.geeksforgeeks.org/selection-sort-algorithm-2/)
- [Insertion sort - Geeks for Geeks](https://www.geeksforgeeks.org/insertion-sort-algorithm/)

---
## bubbleSort

```js
const bubbleSort = (array) => {
  for (let i = 0; i < array.length; i++) {
    for (let j = 0; j < array.length - 1; j++) {
      if (array[j] > array[j + 1]) {
        const temp = array[j];
        array[j] = array[j + 1];
        array[j + 1] = temp;
      }
    }
  }
  return array;
};
```

### Explicación

Este algoritmo lo que hace es en la línea 2 establecer un bucle [[for|for]] que se ejecutará N veces por el largo del [[WTF s an array|array]] que reciba como parámetro. En cada iteración ejecuta otro *for*, en el que se se usa una declaración [[if else|if]] para determinar si el elemento del *índice* actual del array `{js}array[j]` es mayor (>) que el siguiente `{js}array[j + 1]`. Si esta condición es `{js}true` se guarda el valor de `{js}array[j]` en la constante `{js}temp` y se le asigna a el valor de `{js}array[j]` a `{js}array[j + 1]` (*ya que al ser mayor deberá estar por delante del índice actual*). Como último paso se agrega el valor de`{js}temp` al elemento `{js}array[j + 1]`.  

**NOTA:** ¿Qué ocurre con el último elemento del array?
El último elemento del array ya se encuentra ordenado cuando se interpreta el penúltimo. Si `{js}array[array.length - 2]` es mayor que `{js}array[array.length - 1]` entonces el penúltimo pasará a ser el último y viceversa. Por ello no es necesario una iteración del array completo.

```js title:"Bubble Sort optimizado"
const bubbleSort = (array) => {
  let n = array.length; 
  let swapped;

  do {
    swapped = false; // Marcamos si hubo intercambio
    for (let i = 0; i < n - 1; i++) {
      if (array[i] > array[i + 1]) {
        // Intercambiamos si el actual es mayor que el siguiente
        const temp = array[i];
        array[i] = array[i + 1];
        array[i + 1] = temp;
        swapped = true; // Marcamos que hubo un intercambio
      }
    }
    n--; // Reducimos el rango de comparación
  } while (swapped); // Si no hubo intercambios, terminamos

  return array;
};

// Ejemplo de uso:
const numbers = [5, 3, 8, 4, 2];
console.log("Array ordenado:", bubbleSort(numbers));


```

---
## selectionSort

```js
const selectionSort = (array) => {
  for (let i = 0; i < array.length; i++) {
  
	// Se asume que la posición 
	// actual tiene el menor valor.
    let minIndex = i;

	// Se hace una iteración sobre los elementos
	// que aún no se han ordenado  para hallar el menor  
    for (let j = i + 1; j < array.length; j++) {
      if (array[j] < array[minIndex]) {
      
	// Si el próximo elemento en el array es menor
	// se actualiza el valor de minIndex al menor
	// elemento encontrado.
        minIndex = j;
      }
    }

	// Se coloca el elemento más pequeño en su
	// posición correcta asignándole su valor 
	// al elemento iterado en ese momento.
    const temp = array[i];
    array[i] = array[minIndex];
    array[minIndex] = temp;
  }

	// Se entraga el array ordenado como resultado
  return array;
}
```

### Explicación

El *selection sort* funciona comparando el valor del *índice* que tiene la iteración del primer bucle *for*, con el valor de índice que tiene el elemento siguiente iterado por el segundo bucle *for*. 

Se declara la variable `{js}minIndex` con el valor de la primera iteración (`{js}i`), y se inicia la segunda iteración, cuyo valor de índice (`{js}j`) es el elemento siguiente en el array. Se declara un bloque `{js}if` cuyo parámetro es el resultado de `{js}array[j] < array[minIndex]`. Si esta expresión resulta `{js}true`, se asigna el valor de `{js}j` (el elemento siguiente) a `{js}minIndex`.

Se genera una variable `{js}temp` para almacenar el valor de la iteración actual `{js}array[i]`, y al saber que el valor del próximo elemento está en `{js}minIndex` se lo asignamos a `{js}array[i]`, cambiando así la posición del número menor encontrado. Ahora, `{js}minIndex` deberá obtener le valor de temp. 

#### **Ejemplo:**

Supongamos que queremos ordenar el arreglo:  
`{js}[29, 10, 14, 37, 13]`

**Paso 1:**  
Busca el menor número en `{js}[29, 10, 14, 37, 13]` → el menor es `{js}10`.  
Intercámbialo con el primer número (`{js}29`):  
`{js}[10, 29, 14, 37, 13]`.

**Paso 2:**  
Busca el menor número en `{js}[29, 14, 37, 13]` → el menor es `{js}13`.  
Intercámbialo con `{js}29`:  
`{js}[10, 13, 14, 37, 29]`.

**Paso 3:**  
Busca el menor número en `{js}[14, 37, 29]` → el menor es `{js}14`.  
Como ya está en su posición, no se intercambia.

**Paso 4:**  
Busca el menor número en `{js}[37, 29]` → el menor es `{js}29`.  
Intercámbialo con `{js}37`:  
`{js}[10, 13, 14, 29, 37]`.

El arreglo ya está ordenado: `{js}[10, 13, 14, 29, 37]`.

---

## insertionSort

```js
const insertionSort = (array) => {
  for (let i = 1; i < array.length; i++) {
    const currValue = array[i];
    let j = i - 1;

    while (j >= 0 && array[j] > currValue) {
      array[j + 1] = array[j];
      j--;
    }
    array[j + 1] = currValue;
  }
  return array;
}
```
