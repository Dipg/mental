- Frontera de Producción
  id:: 61ee2013-ba01-4b4c-ba53-dc30f15e62e5
  collapsed:: true
	- La frontera de producción parte de la siguiente expresión
		-
		  $$
		  \ln \left(q_{i}\right)=\beta_{0}+\sum_{j=1}^{k} \beta_{j} \ln \left(z_{j i}\right)+\left(v_{i}\right)-u_{i}
		  $$
		- Donde:
			- $ln(q_i)$: Es el logaritmo del numero de unidades producidas por la empresa , medido en unidades
			- $ln(z_{ji})$_: Es el logaritmo del nivel de uso de los insumos, es decir cuanto se ha usado de capital, cuanto se ha usado de trabajo y ase sucesivamente con los demás [[Factores de Producción]] que se tomen en cuenta, por lo general que construyen índices de cantidades para estimar estas variables.
- Frontera de Costos
  id:: 61edfb56-65bd-400b-b36f-3815b0c8f671
	- Teoría
	  collapsed:: true
		- Expresión Matematica
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
			- Interpretación de resultados
				-
				  $$
				  \lambda=\sigma_{u} / \sigma_{v}
				  $$
				- Si $\lambda$ es mayor a uno , esto quiere decir que la desviación estándar debido a la ineficiencia es mayor que la desviación estándar debido a un componente idiosincrático o aleatorio, es decir la ineficiencia se debe mas a términos internos de la empresa
				- Si $\lambda$ es menor a uno la ineficiencia de la empresa esta dada por un componente aleatorio
				- ![image.png](../assets/image_1643001183951_0.png)
				- el sigma mu no mide directamente el parámetro de eficiencia, sino que tanto de costo mas esta añadiendo cada una de las empresas en su forma de producir
				- Cuando se estima la función de costo, no solamente tengo la eficiencia técnica sino también  tengo la eficiencia productiva, es decir la eficiencia técnica mas la asignativa
				- Mientras mayor sea el costo de eficiencia mas ineficiente soy, esto se da por que la empresa estaría produciendo de forma mas ineficiente , por lo tanto mas costosa, no lo esta haciendo al mínimo costo
	- Aplicación
		- Estimación de la Frontera de costos para el sector manufacturero de Ecuador
		  collapsed:: true
			- 1. Datos
				- Los datos se obtuvieron de superintendencia de compañías, mismo que pertenece al sector manufacturero de Ecuador para el año 2017, los datos a utilizar son:
					- Costos: Como el total de costo de las empresas en el año
					- Ventas: El total de ventas que se genero en dólares en el año
					- Precio Laboral: Se tomo el sueldo junto con los salarios y demás remuneraciones
					- Precio del Capital: Se tomo el total de Activos fijos
			- 1. Obtención de Datos
				- Los datos se obtuvieron de superintendencia de compañías para el año 2017, las cuentas que se seleccionaron con sus respectivos códigos fueron ; Costos con el código 7991 ;
			- # Descripción de los datos
			- 2. Estimación de Frontera de Costos
				- Escogemos la estimación de modelo de función de costos, para esta estimación se seleccionó una distribución de tipo half-normal para el termino de eficiencia.
-