-
  <div id="toc_container">
  <p class="toc_title">Contents</p>
  <ul class="toc_list">
    <li><a href="#First_Point_Header">1 First Point Header</a>
    <ul>
      <li><a href="#First_Sub_Point_1">1.1 First Sub Point 1</a></li>
      <li><a href="#First_Sub_Point_2">1.2 First Sub Point 2</a></li>
    </ul>
  </li>
  <li><a href="#Second_Point_Header">2 Second Point Header</a></li>
  <li><a href="#Third_Point_Header">3 Third Point Header</a></li>
  </ul>
  </div>
- Importar un archivo csv
- ```Stata
  import delimited "\Trabajos\3. Endogenidad\Items\endogeneidad\broiler.csv"
  ```
- Definir Color de tema standar
- ```stata
  set scheme s2color
  ```
# Gráficas en Stata
collapsed:: true
	- Librerías Necesarias
	  collapsed:: true
		- ```stata
		  ssc install blindschemes
		  ```
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
# Loop for en Stata
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
-
- /t
-
-
  <style>      
  
  
  </style>
- #toc_container {
    background: #f9f9f9 none repeat scroll 0 0;
    border: 1px solid #aaa;
    display: table;
    font-size: 95%;
    margin-bottom: 1em;
    padding: 20px;
    width: auto;
  }
- .toc_title {
    font-weight: 700;
    text-align: center;
  }
- #toc_container li, #toc_container ul, #toc_container ul li{
    list-style: outside none none !important;
  }
-
  ---
-
- {{renderer :linkpreview,https://journals.sagepub.com/doi/pdf/10.1177/1536867X1701700313}}
- {{renderer :linkpreview,https://www.stata.com/meeting/switzerland16/slides/bischof-switzerland16.pdf}}