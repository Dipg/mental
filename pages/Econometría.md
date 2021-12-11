- Heterocedasticidad ![📑](../assets/2.2_Expo-Test_Heterocedasticidad_1639186036848_0.pdf)
  collapsed:: true
	- La varianza de los errores no es constante
	  collapsed:: true
		- ![image.png](../assets/image_1639184149358_0.png){:height 282, :width 473}
	- ¿Cómo detectamos la heterocedasticidad? ![📑](../assets/2.2_Expo-Test_Heterocedasticidad_1639184490259_0.pdf)
	  collapsed:: true
		- Test de White
		  collapsed:: true
			- En stata
				- {{embed ((c923113e-05a6-4186-8401-3015d4c07281))}}
				-
		- Test Breush y Pagan
		  collapsed:: true
			- Hipotesis Nula
			  collapsed:: true
				- $H_0$ :Varianzas de los errores constantes
			- Código Stata
			  collapsed:: true
				- {{embed ((36eea4e8-4e33-4daf-bae6-f81bb09a4813))}}
	- ¿ A que se puede deber la heterocedasticida ?
	  collapsed:: true
		- A la mala especificación del modelo
- Endogeneidad ![📑](../assets/3.REGRESORES_ESTOCÁSTICOS_Y_VARIABLES_INSTRUMENTALES_1639185978975_0.pdf)
	- ¿ Que es la endogeneidad?
	  collapsed:: true
		- La Endogeneidad es lo que se produce cuando las variables exógenas están corraladas con los términos de perturbación , con el error de la regresión.
	- ¿Por que se da esto?
	  collapsed:: true
		- Puede deberse a una relación causal inversa
		- ¿QUe es una relación causa inversa?
			- Se da cuand la varaible endogena tiene consecuencaias sobre alguna covariable
			- Cuand hay variables que se han omitido en el modelo
			- O cuando existen variables sujetas a errores de medición
	- ¿Qu genera la enodogenidad?
	  collapsed:: true
		- Genera estimaciones sesgadas e inconsistentes
	- ¿ Como corregimos la endogeneidad?
		- Test de Sobreinstrumentación
			- Test de Sargan 
			  collapsed:: true
				- Permite saber si estamos aplicando demasiados instrumentos o no
				- La $H_0$ es que existen restricciones sobre identificadas
		- Variables Instrumentales
			- Practica en stata a partir del minuto 1:15:00
			-
			  <video width="320" height="240" controls>
			    <source src="G:\Otros ordenadores\Mi Ordenador\Habilidades\Universidad\Econometria\Endogeneidad\Variables Instrumentales\Stata\Video\Stata Variables Instrumetnales.mp4" type="video/mp4">
			    Your browser does not support the video tag.
			  </video>
- Especificación del modelo
  collapsed:: true
	- ¿Cómo sabemos la correcta especificación del modelo?
	  collapsed:: true
		- Test de Ramsey
			- Donde $H_0$ El modelo esta bien especificado, $H_1$ El modelo esta mal especificado
			- En Stata
				- {{embed ((8d3feec9-0966-42ae-8d02-8186b4043d5a))}}
-