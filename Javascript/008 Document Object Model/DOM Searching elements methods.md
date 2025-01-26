### **Tabla de contenido**
- [[#Traditional Methods]]

**Fuente:**
- [DOM - manz.dev (LanguajeJS.com)](https://lenguajejs.com/dom/introduccion/que-es/)
- [HTML JS Document Object Model - W3Schools](https://www.w3schools.com/js/js_htmldom_methods.asp)

---

En caso de  querer usar JavaScript para manipular, crear o eliminar elementos dentro de tu [[DOM document Object|document]] deberás acceder a ellos mediante un método. De estos métodos están los [[#Traditional Methods |tradicionales]] y los [[#Modern methods|modernos]]. A continuación se hace explicación de cada tipo.

---
## Traditional methods

| Métodos de búsqueda              | Descripción                                       | Si no lo encuentra... |
| -------------------------------- | ------------------------------------------------- | --------------------- |
| `.getElementById(id)`            | Busca el elemento HTML por su `id`.               | Devuelve .            |
| `.getElementsByClassName(class)` | Busca elementos con la clase `class`.             | Devuelve `[]`.        |
| `.getElementsByName(value)`      | Busca elementos con el atributo `name` a `value`. | Devuelve `[]`.        |
| `.getElementsByTagName(tag)`     | Busca etiquetas HTML `tag`.                       | Devuelve `[]`.        |
Es necesario acotar que el parámetro entre los paréntesis debe escribirse entre comillas.

---
## Modern methods

Los siguientes métodos pueden ser usados como remplazos de los anteriores, e incluso permiten hacer más cosas que los anteriores. Estos ocupan como parámetros `{css}sel` un selector avanzado o básico de CSS.

|Método de búsqueda|Descripción|Si no lo encuentra...|
|---|---|---|
|`.querySelector(sel)`|Busca el primer elemento que coincide con el selector CSS `sel`.|Devuelve .|
|`.querySelectorAll(sel)`|Busca todos los elementos que coinciden con el selector CSS `sel`.|Devuelve `[]`.|
Por ejemplo, podemos seleccionar un elemento que cumpla con varios criterios, como varias clases.

```js
const page = document.querySelector("#page");        // <div id="page"></div>
const info = document.querySelector(".main .info");  // <div class="info"></div>
```
