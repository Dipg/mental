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
  id:: 61b659d4-74eb-40c9-9bfd-0f741c201c32
	- ```python
	  data['logarithm_base10'] = np.log10(data['Salary'])
	  ```
	- https://www.geeksforgeeks.org/log-and-natural-logarithmic-value-of-a-column-in-pandas-python/
- OLS → Mínimos cuadrados en Python regresión
-
-