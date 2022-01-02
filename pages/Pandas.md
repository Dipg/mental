- Crear dataframe en Pandas
  collapsed:: true
	- collapsed:: true
	  ```python
	  import pandas as pd
	  data = {'spike-2': [1,2,3], 'hey spke': [4,5,6], 'spiked-in': [7,8,9], 'no': [10,11,12]}
	  df = pd.DataFrame(data)
	  ```
- Bases de datos del Banco Mundial en Python pandas
  collapsed:: true
	- ```python
	  import wbpy
	  from pprint import pprint
	  api = wbpy.IndicatorAPI()
	  Paises = ["CHN", "FR", "JP"]
	  PIB = "NY.GDP.MKTP.CD"
	  dataset = api.get_dataset(PIB, Paises, date="2010:2012")
	  dataset.as_dict()
	  ```
	- Se importa en formato de diccionario ((61d1f212-cddf-4b19-9497-3d511d30ab26))
- # Diccionarios a Pandas
	- Importar diccionarios como dataframe pandas
	  id:: 61d1f212-cddf-4b19-9497-3d511d30ab26
	  collapsed:: true
		- ```python
		  df = pd.DataFrame.from_dict(dataset.as_dict()) 
		  ```
	- extraer valor de diccionario en pandas
	  collapsed:: true
		- ```python
		  dataset.as_dict()["CN"]
		  ```
		- ![image.png](../assets/image_1641153066343_0.png){:height 344, :width 615}
	- Crear Datos de panes a partir de un diccionari en Pandas
		- Seleccionamos el diccionario
	- ```python
	  diccionarioPIB
	  ```
	- ![image.png](../assets/image_1641153371827_0.png)
	- Convertimos el diccionario en un dataframe Pandas
	- ```python
	  df = pd.DataFrame.from_dict(diccionarioPIB) 
	  df
	  ```
	- ![image.png](../assets/image_1641153461121_0.png)
	- Transponemos el Dataframe y reseteamos el índice de ser necesario
	- ```python
	  df1=df.T
	  df1=df1.reset_index()
	  df1
	  ```
	- ![image.png](../assets/image_1641153565051_0.png)
	- Creamos el nuevo
-
- ¿Cómo cargamos datos .sav  , datos de SPSS?
  collapsed:: true
	- Importar datos SPSS a Pandas
	- collapsed:: true
	  ```python
	  ```
- Importar datos csv
  collapsed:: true
	- collapsed:: true
	  ```python
	  df = pd.read_csv("ejemplo.csv")
	  ```
- Crear Index en Daaframe Pnadas
  collapsed:: true
	- https://www.javatpoint.com/how-to-create-a-dataframes-in-python
	- collapsed:: true
	  ```python
	  df = pd.DataFrame(data, index =['position1', 'position2', 'position3', 'position4'])  
	  ```
- Importar Excel en Pandas
  collapsed:: true
	- collapsed:: true
	  ```python
	  df = pd.read_excel('example.xlsx', sheet_name='example')
	  ```
- Convertir dataframe pandas en excel
  collapsed:: true
	- collapsed:: true
	  ```python
	  df.to_excel('example.xlsx', sheet_name='example')
	  ```
	- {{renderer :linkpreview,https://www.analyticslane.com/2018/07/30/guardar-y-leer-archivos-excel-en-python/}}
- Columnas
  collapsed:: true
	- Renombrar columnas especificas en pandas
		- Cambiar nombre de columnas en pandas
		- ```python
		  dta1=dta1.rename(columns = {'level_0':'coden','index':'code','level_2':'año',0:'PIB'})
		  ```
		- ![image.png](../assets/image_1641148764729_0.png){:height 147, :width 369}
		- ![image.png](../assets/image_1641148753086_0.png){:height 174, :width 369}
	- Cambiar nombres de columnas
	- collapsed:: true
	  ```python
	  df.columns = df.columns.str.replace(', '')
	  ```
	- Poner nombre de columnas
	- collapsed:: true
	  ```python
	  df.columns = ['V', 'W', 'X', 'Y', 'Z']
	  ```
	- https://stackoverflow.com/questions/11346283/renaming-column-names-in-pandas
	- Ordenar Columnas Short columns
	- collapsed:: true
	  ```python
	  result = df.sort(['A', 'B'], ascending=[1, 0])
	  sorted_df = df.sort_values(by=['Column_name'], ascending=True)
	  
	  ```
	- https://pandas.pydata.org/pandas-docs/version/0.19/generated/pandas.DataFrame.sort.html
	- Seleccionar valores de una columna  con condicionales
	-
	- collapsed:: true
	  ```python
	  df[(df.col1 == 'something1') | (df.col2 == 'something1')]
	  ```
	- https://stackoverflow.com/questions/37663931/selecting-columns-with-condition-on-pandas-dataframe
	- collapsed:: true
	  ```python
	  df.loc[df['A'] > 2, 'B'] = new_val
	  ```
	- https://www.it-swarm-es.com/es/python/como-lidiar-con-settingwithcopywarning-en-pandas/1044277694/
	- collapsed:: true
	  ```python
	  df.loc[(df.a < 0), 'a'] = 0
	  ```
	- collapsed:: true
	  ```stata
	  df.loc[df["gender"] == "male", "gender"] = 1
	  ```
	- https://www.geeksforgeeks.org/how-to-replace-values-in-column-based-on-condition-in-pandas/
- Buscar Valores  mediante expresiones regulares
- collapsed:: true
  ```python
  df.filter(regex=("d.*"))
  ```
- https://intellipaat.com/community/28342/how-to-select-columns-from-dataframe-by-regex
-
- Optener Promedio de Columna pandas
- collapsed:: true
  ```python
   df["weight"].mean()
  ```
- https://stackoverflow.com/questions/31037298/pandas-get-column-average-mean
- Seleccionar algunas columnas de dataframe pandas
  collapsed:: true
	- collapsed:: true
	  ```python
	  df['Fruit Total']= df.iloc[:, -4:-1].sum(axis=1)
	  ```
	- https://stackoverflow.com/questions/42063716/pandas-sum-up-multiple-columns-into-one-column-without-last-column
- ((61b659d4-74eb-40c9-9bfd-0f741c201c32))
- Obtener Lista de nombres de columnas pandas
  collapsed:: true
	- collapsed:: true
	  ```Python
	  list(data.columns)
	  ```
	- https://www.geeksforgeeks.org/how-to-get-column-names-in-pandas-dataframe/
- Conocer el formato de un a columna pandas
  collapsed:: true
	- Tipo de Columna Pandas
	- collapsed:: true
	  ```python
	  df['DataFrame Column'].dtypes
	  ```
	- https://datatofish.com/data-type-pandas-dataframe/
- Combinar Dataframe Pandas
  collapsed:: true
	- collapsed:: true
	  ```python
	  frames = [df1, df2, df3]
	  result = pd.concat(frames)
	  ```
	- ![image.png](../assets/image_1639340941350_0.png)
	- https://pandas.pydata.org/pandas-docs/stable/user_guide/merging.html
- Importar csv en python pandas
  collapsed:: true
	- collapsed:: true
	  ```python
	  import pandas as pd
	  df = pd.read_csv('./world-happiness-report-2019.csv')
	  ```
	- https://pretagteam.com/question/finding-all-regex-matches-from-a-pandas-dataframe-column
- Elegir valores de una columna pandas
  collapsed:: true
	- collapsed:: true
	  ```python
	  df.loc[:, df.columns.str.match('^d')]
	  ```
	- https://stackoverflow.com/questions/30808430/how-to-select-columns-from-dataframe-by-regex
- Crear rango de tiempo en pandas
  collapsed:: true
	- Crear Columna de tiempo pandas
	- collapsed:: true
	  ```python
	  ```
	- https://catriscode.com/2021/02/27/creating-time-range-in-python/
	- https://stackoverflow.com/questions/34915828/pandas-date-range-to-generate-monthly-data-at-beginning-of-the-month
- Extraer nombre de columnas Pandas como lista, opterner nombre de Columnas pandas
  collapsed:: true
	- collapsed:: true
	  ```python
	  df.columns
	  ```
	- Link
	  collapsed:: true
		- [https://cmdlinetips.com/2020/04/how-to-get-column-names-as-list-in-pandas/#:~:text=We%20can%20get%20the%20names,using%20Pandas%20method%20%E2%80%9Ccolumns%E2%80%9D.&text=Pandas'%20columns%20method%20returns%20the%20names%20as%20Pandas%20Index%20object.&text=We%20can%20convert%20the%20Pandas,using%20the%20tolist()%20method.&text=And%20now%20we%20have%20Pandas'%20dataframe%20column%20names%20as%20a%20list](https://datatofish.com/list-column-names-pandas-dataframe/)
- Contar numero de NAN pandas, contar valores faltantes Pandas
  collapsed:: true
	- collapsed:: true
	  ```Python
	  df.isna().sum()
	  ```
	- {{renderer :linkpreview,https://stackoverflow.com/questions/26266362/how-to-count-the-nan-values-in-a-column-in-pandas-dataframe}}
- Rellenar valores faltantes con promedio de columna en pandas,  Fill NaN whit average in data frame pandas
  collapsed:: true
	- collapsed:: true
	  ```python
	  df.fillna(df.mean())
	  ```
	- {{renderer :linkpreview,https://stackoverflow.com/questions/18689823/pandas-dataframe-replace-nan-values-with-average-of-columns}}
- Seleccionar lista de elementos en columna pandas
  collapsed:: true
	- collapsed:: true
	  ```python
	  class_23 = titanic[titanic["Pclass"].isin([2, 3])]
	  ```
	- ![image.png](../assets/image_1639648274136_0.png)
	- {{renderer :linkpreview,https://pandas.pydata.org/docs/getting_started/intro_tutorials/03_subset_data.html}}
- Eliminar columnas que contengan NaN pandas
  collapsed:: true
	- collapsed:: true
	  ```python
	  df.dropna(axis='columns')
	  ```
	- {{renderer :linkpreview,https://www.codegrepper.com/code-examples/python/pandas+drop+if+all+columns+are+nan}}
- Eliminar columnas sin nombre
  collapsed:: true
	- Eliminar columnas con NaN
	- ![image.png](../assets/image_1639648698403_0.png)
	- collapsed:: true
	  ```python
	   df = df.loc[:, df.columns.notnull()]
	  ```
	- ![image.png](../assets/image_1639648709196_0.png)
	- {{renderer :linkpreview,https://stackoverflow.com/questions/46101714/pandas-how-to-drop-multiple-columns-with-nan-as-col-name}}
- Buscar todas las columnas sin nombre
  collapsed:: true
	- Buscar todas las columnas con nana
	- collapsed:: true
	  ```python
	  df.columns[df.notna().all()]
	  ```
	- {{renderer :linkpreview,https://www.codegrepper.com/code-examples/python/get+columns+names+having+nan+values+pandas}}
- Llenar celdas nan
  collapsed:: true
	- Fill NaN values
	- collapsed:: true
	  ```python
	  df['a'] = df['a'].fillna(55)
	  ```
	- ![image.png](../assets/image_1639648921748_0.png)
	- {{renderer :linkpreview,https://stackoverflow.com/questions/38927099/keyerror-nan-in-dict}}
- Convertir todo un dataframe  a en formato numérico
  collapsed:: true
	- collapsed:: true
	  ```python
	  df.apply(pd.to_numeric)
	  ```
	- {{renderer :linkpreview,https://stackoverflow.com/questions/34844711/convert-entire-pandas-dataframe-to-integers-in-pandas-0-17-0/34844867}}
- Seleccionar rango de Columnas por nombre en Pandas
  collapsed:: true
	- collapsed:: true
	  ```python
	  df[['alcohol','hue']]
	  data[['A', 'B']]
	  df1 = df[['a', 'b']]
	  ```
	- ![image.png](../assets/image_1639706319518_0.png)
	- {{renderer :linkpreview,https://www.kite.com/python/examples/3182/pandas-select-columns-of-a-%60dataframe%60-by-column-names}}
	- {{renderer :linkpreview,https://towardsdatascience.com/interesting-ways-to-select-pandas-dataframe-columns-b29b82bbfb33}}
	- {{renderer :linkpreview,https://stackoverflow.com/questions/11285613/selecting-multiple-columns-in-a-pandas-dataframe}}
- Convertir en numero python pandas , convertir en entero
  collapsed:: true
	- collapsed:: true
	  ```python
	  int(float(a))
	  pd.to_numeric(s)
	  ```
- Convertir en flotante
  collapsed:: true
	- collapsed:: true
	  ```python
	  float(a)
	  ```
- Contar el numero de nan ausentes
  collapsed:: true
	- collapsed:: true
	  ```python
	  df['column name'].isna().sum()
	  ```
- Eliminar la primera  fila de un dataframe pandas
  collapsed:: true
	- collapsed:: true
	  ```python
	  df = df.iloc[1: , :]
	  df.drop(df.index[1])
	  ```
	- {{renderer :linkpreview,https://thispointer.com/drop-first-row-of-pandas-dataframe-3-ways/}}
	- {{renderer :linkpreview,https://www.codegrepper.com/code-examples/python/pandas+set+first+row+as+column+names}}
- Poner primera fila como columna pandas
  collapsed:: true
	- collapsed:: true
	  ```python
	  new_header = df.iloc[0] #Get the first row for the header
	  df = df[1:] #Take the data less the header row
	  df.columns = new_header #Set the header row as the df header
	  ```
	- {{renderer :linkpreview,https://poopcode.com/make-first-row-as-column-names-in-pandas/}}