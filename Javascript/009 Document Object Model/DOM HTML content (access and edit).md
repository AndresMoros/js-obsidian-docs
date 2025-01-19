---

---
### **Tabla de contenido**
- [[#`{js}element.nodeName|.nodeName]]
- [[#{js}element.textContent|.textCotent]]
- [[#element.innerText|.innerText]]
- [[#{js}element.innerHTML|.innerHTML]]

**Fuente:**
- [DOM - manz.dev (LanguajeJS.com)](https://lenguajejs.com/dom/introduccion/que-es/)
- [HTML JS Document Object Model - W3Schools](https://www.w3schools.com/js/js_htmldom_methods.asp)

Se puede acceder al contenido de un elemento HTML (y modificarlo), por medio de una serie de propiedades dentro de los elementos HTML que nos permiten realizar esta tarea.

| Propiedades        | Descripción                                                                              |
| ------------------ | ---------------------------------------------------------------------------------------- |
| `.nodeName`        | Devuelve el nombre del nodo (etiqueta en mayúsculas). Sólo lectura.                      |
| Contenido de texto |                                                                                          |
| `.textContent`     | Devuelve (o cambia) el contenido de texto del elemento.                                  |
| `.innerText`       | Devuelve (o cambia) el contenido de texto renderizado (tiene en cuenta los estilos CSS). |
| `.innerHTML`       | Idem a `.textConent`, pero devuelve (o cambia) la estructura HTML.                       |
| `.setUnsafeHTML`   | Funciona para crear contenido HTML con un *Shadow DOM declarativo*                       |

---

## `{js}element.nodeName`

Con esto solo seremos capaces de conocer el nombre de la etiqueta del elemento, pero solo eso. No permite modificarla.

---
## `{js}element.textContent`

Esta propiedad permite acceder (o modificar) el texto de un elemento HTML concreto. Para modificar el texto de un elemento HTML se puede hacer usando esta propiedad y asignado su valor como a cualquier otra variable.

```html title:"HTML"
<div class="container">
  <div class="parent">
    <p>Hola a todos.</p>
    <p class="message">Mi nombre es <strong>Kuker</strong>.</p>
  </div>
</div>
```

```js title:"JavaScript"
const element = document.querySelector(".message");

element.textContent;                   // "Mi nombre es Kuker."
element.textContent = "Hola a todos";  // Modificamos el contenido de texto
element.textContent;                   // "Hola a todos"

```

Usar esta propiedad para modificar el texto de un elemento obviará todas las etiquetas que puedan estar anidadas. En el ejemplo de arriba se ha eliminado la etiqueta `{html}<strong>`. 

---
## `{js}element.innerHTML`

La propiedad `{js}element.innerHTML` permite acceder y modificar al contenido de un elemento, pero, a diferencia de `{js}element.textContent`, también se ve reflejado el contenido HTML del documento. Asimismo, las etiquetas HTML que se escriban con esta propiedad serán interpretados por el navegador, al contrario que con `{js}element.textContent`.

```js
const element = document.querySelector(".message");

element.innerHTML;    // "Mi nombre es <strong>Kuker</strong>."
element.textContent;  // "Mi nombre es Kuker."

```

---
