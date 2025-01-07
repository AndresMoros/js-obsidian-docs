Las expresiones regulares pueden usarse para detectar patrones en una [[Data Types#String||cadena de texto]].

```javascript title:"Verifica los elementos HTML"
//------- Verify the string on the input element
function verifyFormat(str) {
  const regex = /<.*?>/g; // Coincide con el contenido de cada conjunto de <...>, uno a la vez
  return str.match(regex) || []; // Devuelve las coincidencias o un array vacío si no hay
}

```

```javascript title:"Verifica los caracteres alfanumericos"
const verifyFormat = (str) => {
  const regex = /[^a-z0-9]/gi; // Detecta caracteres que no sean letras ni números
							  // g: Busca todas las coincidencias globalmente.
							  // i: Ignora si son mayusculas o minusculas
  return str.match(regex, "");
};

```
