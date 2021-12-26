- Crear bucle for en JavaScript con lista
	- ```js
	  const cars = ["BMW", "Volvo", "Saab", "Ford", "Fiat", "Audi"];
	  
	  let text = "";
	  for (let i = 0; i < cars.length; i++) {
	    text += cars[i] + "<br>";
	  }
	  
	  document.getElementById("demo").innerHTML = text;
	  ```
	- Ref
		- {{renderer :linkpreview,https://www.w3schools.com/js/tryit.asp?filename=tryjs_loop_for}}
		  id:: 61c8a154-7f34-4c92-ad7b-feff53cffba4