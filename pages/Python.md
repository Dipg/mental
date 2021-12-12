- Manejo de datos
	- Usamos la librería [[Pandas]]
- Graficas
	- [[Plotly]]
- Generales
	- Redondear Numeros
	- ```python
	  import numpy as np
	  myList = list(np.around(np.array(myList),2))
	  ```
- Convertir valores de una columna a logaritmos
	- ```python
	  data['logarithm_base10'] = np.log10(data['Salary'])
	  ```