-
- {{renderer :toc_cqtnwk}}
	- # 1. Configuraciones
	  collapsed:: true
		- ## Instalar Paquetes
			- ```r
			  install.packages("tidyverse")
			  ```
		- ## Coocer versión de R que utilizo
			- ```terminal
			  version
			  ```
	- # 2. Graficas
	  collapsed:: true
		- # Cambiar Imagen de tamaño en r  
		  collapsed:: true
			- Cambiar plot de tamaño en r en Jupyter
			- ```R
			  options(repr.plot.width=22, repr.plot.height=15)
			  ```
			- ![image.png](../assets/image_1639531345532_0.png){:height 182, :width 239}
			- ![image.png](../assets/image_1639531351044_0.png){:height 473, :width 683}
			- {{renderer :linkpreview,https://blog.revolutionanalytics.com/2015/09/resizing-plots-in-the-r-kernel-for-jupyter-notebooks.html}}
	- # 3. Manejo de Data
		- ## Importar datos de Spss en R
		  collapsed:: true
			- Importar dataframe sps en R
			- ```r
			  library(haven)
			  enaho17_m1_A <- as.data.frame(read_sav("Enaho01-2017-100.sav"))
			  ```
			- Referencia
			  collapsed:: true
				- {{renderer :linkpreview,https://rpubs.com/dsulmont/475703}}
		- ## Seleccionar  columnas Especificas
		  collapsed:: true
			- Seleccionar un Subconjunto especifico de  de columnas por nombre en R
			- ```r
			  df[,c("A","B","E")] 
			  ```
			- {{renderer :linkpreview,https://stackoverflow.com/questions/10085806/extracting-specific-columns-from-a-data-frame}}
		- ## Eliminar NaN en datafrane  R
		  collapsed:: true
			- - Eliminar valores ausentes de dataframe en R
			- ```r
			  df2<−na.omit(df2)
			  ```
			- https://www.tutorialspoint.com/how-to-remove-rows-from-data-frame-in-r-that-contains-nan
		- ## Detalles de las variables en Dataframe R
			- ```r
			  str(df)
			  ```
			-
	- # 4. Análisis Multivariado
	  collapsed:: true
		- ## Análisis Clústers
		  collapsed:: true
			- K-Means
				- {{renderer :linkpreview,https://www.youtube.com/watch?v=c1E_4lzfUBw}}
				- {{renderer :linkpreview,https://www.youtube.com/watch?v=WM3VfPLVFNw}}
		- ## Árbol de Decisiones
			- ### aw