-
- Importar un archivo csv
- ```Stata
  import delimited "\Trabajos\3. Endogenidad\Items\endogeneidad\broiler.csv"
  ```
- #  [](#1.) Gráficas en Stata
  collapsed:: true
	- Librerías Necesarias
		- ```stata
		  ssc install blindschemes
		  ```
	- Definir Color de tema standar de las graficas
	- ```stata
	  set scheme s2color
	  ```
	- Mas temas para stata
		- {{renderer :linkpreview,https://blog.stata.com/2018/10/02/scheming-your-way-to-your-favorite-graph-style/}}
	- Cambiar estilo de presentación de gráficos
	- ```stata
	  set scheme s2color
	  grstyle init
	  . grstyle color background white
	  . grstyle color major_grid dimgray
	  . grstyle linewidth major_grid thin
	  . grstyle yesno draw_major_hgrid yes
	  . grstyle yesno grid_draw_min yes
	  . grstyle yesno grid_draw_max yes
	  ```
	- Pagina para cambiar el diseño, referencia de lo anterior
		- {{renderer :linkpreview,https://www.stata.com/meeting/germany18/slides/germany18_Jann.pdf}}
		-
	- Crear grafico  de barras , con todos los detalles. Donde $q$ es la variable en el eje de la las $Y$ y $year$ es la variable en el eje de las $X$
	- ```stata
	  graph bar q, ///
	  over(year , label(labsize(2) angle(90) labgap(1)  ) relabel(`r(relabel)')) ///
	  title("Demanda de Pollos 1990-1960" ///
	  , span size(medium)) ///
	  ytitle("Demanda de Pollos") ///
	  blabel(bar, format(%4.1f) size(1.5) ) ///
	  note("Fuente: Dennis Epple y Bennett McCallum            Elaboración: Autor  ")  
	  ```
	- ![image.png](../assets/image_1638964870055_0.png)
	- Cambiar el angUlo de los axis en Stata
	- ```stata
	  graph bar q, ///
	  over(year , label(angle(90)) ///
	  ```
# [](#2.) Loop for en Stata
collapsed:: true
	- Loop for en todo el rango de variables. Donde la primera coluna (variable es  `year` y la ultima es `time`). Generamos los logaritmos de cada variable
	- ```stata
	  foreach v of var year-time {
	  gen lg`v'= log(`v')
	   }
	  ```
	- Resultado
		- ![image.png](../assets/image_1638965003258_0.png){:height 199, :width 689}
		- ![image.png](../assets/image_1638965051829_0.png){:height 189, :width 689}
# [](#3.)  Modificar elementos de variable(Columna)
collapsed:: true
	- Cambiar nombres por labels en elementos de columna/variable Stata
	- ```stata
	  > label define sector 1 "SECTOR 1" 2 "SECTOR 2" 3 "SECTOR 3"
	  > label values sector sector
	  ```
- # [](#4.)  Series de Tiempo
  collapsed:: true
	- Rezagar una variable un periodo en Stata
	- ```stata
	  *Rezag la variable ingreso un periodo
	  L1.ingreso
	  *Si deseo rezagar mas periodos solo aumento el umero
	  *Ej: Rezago de la varaible ingreso 3 periodos
	  L3.ingreso
	  ```
# [](#6.)  Test Econométricos
	- Test de Heterocedasticidad
	  collapsed:: true
		- Test de White
			- id:: c923113e-05a6-4186-8401-3015d4c07281
			  ```stata
			  estat imtest
			  ```
			-
		- Test Breush y pagan
		  collapsed:: true
			- id:: 36eea4e8-4e33-4daf-bae6-f81bb09a4813
			  ```stata
			  estat hettest
			  ```
	- Test de Especificación del Modelo
		- Test de Ramse
		-
-
  ---
-
- {{renderer :linkpreview,https://journals.sagepub.com/doi/pdf/10.1177/1536867X1701700313}}
- {{renderer :linkpreview,https://www.stata.com/meeting/switzerland16/slides/bischof-switzerland16.pdf}}