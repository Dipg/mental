- ¿Cómo cargamos datos .sav  , datos de SPSS?
	- ```python
	  ```
- Importar datos csv
	- ```python
	  df = pd.read_csv("ejemplo.csv")
	  ```
-
- Columnas
	-
	- Cambiar nombres de columnas
	- ```python
	  df.columns = df.columns.str.replace(', '')
	  ```
	- Poner nombre de columnas
	- ```python
	  df.columns = ['V', 'W', 'X', 'Y', 'Z']
	  ```
	- https://stackoverflow.com/questions/11346283/renaming-column-names-in-pandas
	- Ordenar Columnas Short columns
	-