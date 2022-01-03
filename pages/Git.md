- Hacer push en un repositorio ya creado
	- ```git
	  git init
	  ```
	- ```git
	  git add .
	  ```
	- ```git
	  git commit -m 'mi primer commit'
	  ```
	- Copiamos el URL del repositorio
	- ![image.png](../assets/image_1641219709894_0.png)
	- ```git
	  git remote add origin https://github.com/aqui-tu-repo.git
	  ```
	- Ahora elegimos la branch
	- ```git
	  git push -u origin master
	  ```