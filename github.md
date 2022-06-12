# GitHub

**Terminal**  
[My_Github](https://github.com/Ceristh/markdown) 
## clonar repositorio.  
~~~
git clone https://github.com/Ceristh/markdown.git
~~~

## Primero crear repositorio en github.  
~~~
git init -b main
git add . && git commit -m "initial commit"
git remote add origin https://github.com/Ceristh/markdown.git
git push -u origin main
~~~

## Cambios en repositorio.  
~~~
git add . && git commit -m "actualización"
git push
~~~

## Diferencia entre git pull y git fetch.    

+ Repositorio remoto: sería el que se almacena en GitHub.  
+ Repositorio local: es una copia del repositorio remoto que se almacena en tu ordenador o en un servidor, por ejemplo.  
+ Espacio de trabajo: los archivos con los que trabajas directamente en Visual Studio Code, PyCharm o con cualquier editor de código.  

![git fetch y git pull](./img/git-fetch-vs-git-pull-diferencias.png "git fetch y git pull")

>git fetch es el comando que hace que tu repositorio Git local se actualice con la última información que hay en el repositorio remoto, pero no hace ninguna transferencia de archivos a tu espacio de trabajo local (el código que ves en tu editor por ejemplo). Podría decirse que sirve para comprobar si hay algún cambio y traerlo a tu repositorio local.  

>git pull es el comando que comprueba si hay cambios en el repositorio remoto y, en caso de que los haya, se trae esos archivos a tu repositorio local y actualiza tu espacio de trabajo (tu IDE, tus archivos).  