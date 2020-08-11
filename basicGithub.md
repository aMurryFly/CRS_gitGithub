

Proceso para actualizar nuestro repositorio remoto una vez hecho el Fork de algún otro compañero:

Una vez que tenemos la "copia" en nuestro repositorio remoto, debemos primero clonarlo a nuestro repositorio locas:

$git clone url

donde la url es de nuestro repositorio remoto

Teniendo la copia, dentro de nuetro repositorio local nos movemos a la carpeta del repositorio 

Una vez ahí, actualizamos nuestro repositorio local desde el repositorio original:

%git remote add --track master NICKNAME url

donde el NICKNAME es un identificador que puede ser cualquier nombre y la url es del repositorio remoto original

Si modificamos alguno de los acrhivos dentro de nuestro repositorio local, debemos agregarlos y comentarlos

$git add README.md
$git commit -m "Ejemplo"

Nos movemos a la rama que queremos actualizar y subimos los cambios con pull
$git pull NAME RAMA

Y actualizamos la respectiva rama en nuestro repositorio remoto

$git push origin RAMA