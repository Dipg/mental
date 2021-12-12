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
	- ```python
	  result = df.sort(['A', 'B'], ascending=[1, 0])
	  sorted_df = df.sort_values(by=['Column_name'], ascending=True)
	  
	  ```
	- https://pandas.pydata.org/pandas-docs/version/0.19/generated/pandas.DataFrame.sort.html
	- Seleccionar valores de una columna  con condicionales
	- ```python
	  df.loc[df['A'] > 2, 'B'] = new_val
	  ```
	- https://www.it-swarm-es.com/es/python/como-lidiar-con-settingwithcopywarning-en-pandas/1044277694/
	- ```python
	  df.loc[(df.a < 0), 'a'] = 0
	  ```
	- ```stata
	  df.loc[df["gender"] == "male", "gender"] = 1
	  ```
	- https://www.geeksforgeeks.org/how-to-replace-values-in-column-based-on-condition-in-pandas/
- Buscar Valores  mediante expresiones regulares
- ```python
  df.filter(regex=("d.*"))
  ```
- https://intellipaat.com/community/28342/how-to-select-columns-from-dataframe-by-regex
-