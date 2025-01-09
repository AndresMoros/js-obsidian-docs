
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
