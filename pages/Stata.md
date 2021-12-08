- Importar un archivo csv
- ```Stata
  import delimited "\Trabajos\3. Endogenidad\Items\endogeneidad\broiler.csv"
  ```
- Definir Color de tema standar
- ```stata
  set scheme s2color
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
- Crear grafico  de barras