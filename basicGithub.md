# :fire: Conceptos importantes para el manejo de GitHub :fire:

## :earth_americas: Repositorio en línea
 * Es el repositorio que está guardado en el servidor de github

## :house: Repositorio local
 * Es una copia del servidor en línea dentro de nuestro ordenador

## :satellite: Repositorio remoto 
 * Se trata del repositorio en líea de un tercero al cual hicimos un fork

## :fork_and_knife: Fork
 * Crear una copia del repositorio en línea de otro perfil en nuestro perfil de github. Desde este repositorio, podemos colaborar y sugerir cambios en el repositorio original

## :page_facing_up: Pull Request
 * Se trata de una solicitud de incluir cambios en el repositorio de un tercero realizados en un repositorio en línea surgido a partir de realizarle un fork  

# :arrows_counterclockwise: Proceso para actualizar un repositorio remoto al que se hizo Fork

:small_blue_diamond: Primero hacemos fork al repositorio remoto que necesitamos actualizar

![Fork](https://github.com/aMurryFly/CRS_gitGithub/blob/basicGitHub/gitHub_Imagenes/fork.jpg)

:small_blue_diamond: Una vez que tenemos la "copia" en nuestro repositorio remoto, debemos primero clonarlo a nuestro repositorio local

Utilizando la terminal, se hace uso del siguiente comando: `$git clone URL` , donde **URL** es la URL de nuestro repositorio remoto

![Clone](https://github.com/aMurryFly/CRS_gitGithub/blob/basicGitHub/gitHub_Imagenes/git_clone.png)  

:small_blue_diamond: Teniendo la copia, dentro de nuetro repositorio local nos movemos a la carpeta del repositorio

:small_blue_diamond: Si modificamos alguno de los acrhivos dentro de nuestro repositorio local, debemos agregarlos y comentarlos

Utilizando el siguiente comando agregamos el archivo: `$git add "ARCHIVO"`    
Donde **ARCHIVO** es el nombre del archivo modificado o creado    
  
Después de agregarlo, guardamos los cambios con el siguiente comando: `$git commit -m "COMENTARIO"`    
Donde **COMENTARIO** es un comentario respecto a los cambios guardados

![add_commit](https://github.com/aMurryFly/CRS_gitGithub/blob/basicGitHub/gitHub_Imagenes/git_add_and_commit.png)

:small_blue_diamond: Actualizamos la copia del repositorio remoto original

Utilizando el siguiente comando actualizamos la copia del repositorio original: `$git push`  

![Clone](https://github.com/aMurryFly/CRS_gitGithub/blob/basicGitHub/gitHub_Imagenes/git_push.png)
    
:small_blue_diamond: Generamos el Pull Request  

Por último, una vez actualizada nuestra copia del repositorio remoto, generamos la solicitud para actualizar el repositorio remoto original

![pull_request](https://github.com/aMurryFly/CRS_gitGithub/blob/basicGitHub/gitHub_Imagenes/Pull_request.jpg)

# :satellite: :heavy_minus_sign: :house: Proceso para actualizar nuestro repositorio local, desde un repositorio remoto

:small_blue_diamond: Primero, una vez dentro de nuestro repositorio local, nos movemos a la rama que queremos actualizar  

Utilizando el siguiente comando nos movemos a la rama de interés: `$git checkout RAMA`  
Donde **RAMA** es el nombre de la rama a actualizar  

![checkout](https://github.com/aMurryFly/CRS_gitGithub/blob/basicGitHub/gitHub_Imagenes/git_checkout.png)  

:small_blue_diamond: Agregamos la dirección del repositorio remoto original  

Utilizando el siguiente comando: `%git remote add --track master NICKNAME URL`  
Donde **NICKNAME** es un identificador que puede ser cualquier nombre y **URL** es la URL del repositorio remoto original

:small_blue_diamond: Actualizamos el repositorio local  

Utilizando el siguiente comando actualizamos nuestro repositorio local con los ultimos cambios del repositorio remoto original:

`pull $git pull NICKNAME RAMA`  
Donde **RAMA** es el nombre de la rama a actualizar
