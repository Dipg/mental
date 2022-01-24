- Frontera de Producción
  id:: 61ee2013-ba01-4b4c-ba53-dc30f15e62e5
	- La frontera de producción parte de la siguiente expresión
		-
		  $$
		  \ln \left(q_{i}\right)=\beta_{0}+\sum_{j=1}^{k} \beta_{j} \ln \left(z_{j i}\right)+\left(v_{i}\right)-u_{i}
		  $$
		- Donde:
			- $ln(q_i)$: Es el logaritmo del numero de unidades producidas por la empresa , medido en unidades
- Frontera de Costos
  id:: 61edfb56-65bd-400b-b36f-3815b0c8f671
	- La frontera de costo parte de la siguiente expresión
	  id:: 61ee1ef1-069d-4085-a8d8-5d61c255b089
	-
	  $$
	  \ln \left(c_{i}\right)=\beta_{0}+\beta_{q} \ln \left(q_{i}\right)+\sum_{j=1}^{k} \beta_{j} \ln \left(p_{j i}\right) \text { 㐲 } v_{i}+u_{i}
	  $$
	- Donde
		- $ln(c_i)$ : es el logaritmo del costo de la empresa medido en dólares
		- $ln(q_i)$: Es el logaritmo del numero de unidades producidas por la empresa , medido en unidades
		- $ln(p_{ji})$ : Es el logaritmo del precio de los insumos Capital, Trabajo, etc, medido en dólares a diferencia de la estimación de la ((61ee2013-ba01-4b4c-ba53-dc30f15e62e5))
	- Estimación
	  collapsed:: true
		- Estimación de la Frontera de costos para el sector manufacturero de Ecuador
			- 1. Datos
				- Los datos se obtuvieron de superintendencia de compañías, mismo que pertenece al sector manufacturero de Ecuador para el año 2017, los datos a utilizar son:
					- Costos: Como el total de costo de las empresas en el año
					- Ventas: El total de ventas que se genero en dólares en el año
					- Precio Laboral: Se tomo el sueldo junto con los salarios y demás remuneraciones
					- Precio del Capital: Se tomo el total de Activos fijos
			- 1. Obtención de Datos
				- Los datos se obtuvieron de superintendencia de compañías para el año 2017, las cuentas que se seleccionaron con sus respectivos códigos fueron ; Costos con el código 7991 ;
			- 2. Estimación de Frontera de Costos
				- Escogemos la estimación de modelo de función de costos, para esta estimación se seleccionó una distribución de tipo half-normal para el termino de eficiencia.