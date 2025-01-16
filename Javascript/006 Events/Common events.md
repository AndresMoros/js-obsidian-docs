### **Tabla de contenido**

- [[#`{javascript}click`||click]]
- [[#`{javascript}change`|change]]
- [[#{js}keydown||keydown]]

**Fuente:**
- [Learn Recursion by Building a Decimal to Binary Converter](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures-v8/learn-recursion-by-building-a-decimal-to-binary-converter/)
- [Element: evento keydown](https://developer.mozilla.org/es/docs/Web/API/Element/keydown_event)

---

## `{javascript}click`

Detecta cuando el elemento HTML sobre el cual se aplica se le hizo clic. Comúnmente se usa en botones, pero puede ser hecho sobre cualquier elemento visible por el usuario con el que se espera una interacción. 

```javascript
<button id="my-button">Haz clic aquí</button>
<script>
	const button = document.getElementById("my-button");
	button.addEventListener("click", () => {
		console.log("El botón fue clickeado");
	});
</script>
```

- **`addEventListener("click", ...)`**: Se usa para escuchar el evento `click` en el botón. El evento se dispara cuando el usuario hace clic en el elemento.
- **La función**: Cuando ocurre el clic, se ejecuta el código dentro de la función, en este caso, un mensaje en la consola.
---
## `{javascript}change`

El evento `change` detecta cuando el elemento HTML sobre el que se está aplicando sufre algún cambio. 

```html
<select id="options-selector">
	<option value="default">Default</option>
	<option value="1">Option 1</option>
	<option value="2">Option 2</option>
</select>
<script>
	const selector = document.getElementById("options-selector");
	selector.addEventListener("change", () => {
		console.log(`Selected value: ${selector.value}`);
		console.log(`Selected text: ${selector.selectedOptions[0].textContent}`);
	});
</script>
``` 

- **`value`**: Se utiliza para obtener el valor asignado al atributo `value` de la opción seleccionada.
- **`selectedOptions[0].textContent`**: Proporciona el texto visible de la opción seleccionada.
- **Evento `change`**: Se dispara cuando el usuario cambia la selección en el `<select>`.

---
## `{js}keydown`

El evento `keydown` produce cuando se presiona una tecla en el teclado del usuario, independientemente de si esta contiene un valor de carácter. Igual que el evento `keyup`, regresa el valor del código de carácter que se ha presionado. 

Los eventos de teclado solo son generados por `<input>`, `<textarea>`, `<summary>` y cualquier cosa con el atributo `contentEditable` o `tabindex`

