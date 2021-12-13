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
	- ### Heatplot de correlacones
	- ```stata
	  pwcorr q  pchick y pf pcor pbeef pop, star(0.05)
	  matrix C = r(C)
	  heatplot C, values(format(%9.3f)) color(hcl, diverging intensity(.6)) ///
	  legend(off) aspectratio(1)
	  ```
	- ![image.png](../assets/image_1639387544335_0.png)
	- ```stata
	  heatplot C, values(format(%9.3f)) color(hcl, diverging intensity(.6)) ///
	  legend(off) aspectratio(1) lower nodiagonal
	  ```
	- ![image.png](../assets/image_1639387566123_0.png)
	- {{renderer :linkpreview,https://www.stata.com/meeting/germany19/slides/germany19_Jann.pdf}}
	- Scatterplot en Stata
	- ![image.png](../assets/image_1639387661252_0.png)
	- ```stata
	   scatter  pchick q, ///
	  title("Precio del Pollo - Demanda de Pollos" ///
	  , span size(medium)) ///
	  ytitle("Precio del Pollo") ///
	  xtitle("Cantidad Demandad de Pollo") ///
	  note("Fuente: Dennis Epple y Bennett McCallum                                                        Elaboración: Autor  ")  
	  ```
	- Simple Scatter
	- ```stata
	  scatter mpg weight
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
	- Rezagar una variable mas de un periodo a la vez
	- ```stata
	  L(1/5).Ingreso
	  ```
- # [](#6.)  Test Econométricos
  collapsed:: true
	- Test de Heterocedasticidad
		- Test de White
		  collapsed:: true
			- id:: c923113e-05a6-4186-8401-3015d4c07281
			  ```stata
			  estat imtest
			  ```
			-
		- Test Breush y pagan
			- id:: 36eea4e8-4e33-4daf-bae6-f81bb09a4813
			  ```stata
			  estat hettest
			  ```
			- Si deseamos conocer mayor especificación de que variables pueden estar causando homocedasticidad  añadimos las variables exógenas y ' ' `,mtest`
			- ```stata
			  estat hettest ingreso educación, mtest
			  ```
			-
		- Video
		  collapsed:: true
			- Clase 6 Econometría II
			- {{renderer :linkpreview,https://drive.google.com/file/d/1fyWKT-bprk0qKy1dzQGLzBogxzjB-tTV/view?usp=sharing}}
	- Test de Endogenidad
		- Tets de Wu- Durbin -Hausman
			- id:: 8cead2be-c19c-4986-a218-9a2dea1256e5
			  ```stata
			  estat endogenous
			  ```
	- Test de Especificación del Modelo
		- Test de Ramsey
			- id:: 8d3feec9-0966-42ae-8d02-8186b4043d5a
			  ```stata
			  estat ovtest
			  ```
	- Test de Sobre instrumentación
		- Test de sargan
		- ```stata
		  estat overid
		  ```
# [](#7.)  Regresiones
collapsed:: true
	- MCO
	- IV (Variables instrumentales)
		- ```stata
		  ivregress 2sls lgq (lgpchick = lgpf lgpcor)
		  ```
		- Donde `lgq`  es la variable endógena, `lgpchick` es la variable exógena que se supone que sufre endogeneidad, `lgpf, lgpcor` son las varaibles instrumentales
# Correlaciones
	- Correlación de Pearson
	- ```stata
	  pwcorr,star(.05)
	  ```
	- ![image.png](../assets/image_1639387840831_0.png)
	-
	-
	  ---
-
- {{renderer :linkpreview,https://journals.sagepub.com/doi/pdf/10.1177/1536867X1701700313}}
- {{renderer :linkpreview,https://www.stata.com/meeting/switzerland16/slides/bischof-switzerland16.pdf}}