# :boom: Comando Básicos para el manejo de Git/Git-Hub :boom:

## Acerca del documento :pint_up:

*Éste ha sido creado con la finalidad de plasmar los conocimientos adquiridos en el curso de manejo de Git/Git-Hub por parte del Taller de Robótica Abierta, para el buen manejo de estas dos grandes herramientas, orientada a la realizacion de proyectos multidiciplinarios, y el buen manejo de estos.*

**Lista de Comandos**

* Status

Este comando nos permite ver el estado actual de nuestro repositorio, en este caso si este se encuentra actualizado con el repositorio remoto y nos indica si hay algun cambio.

$git status
 
* Help

Este comando nos permite listar, valga la redundancia, los comandos más usados en git, esto con el proposito de tener una herramienta por si no recordamos el comando especifico a utilizar. Tambien tiene uan pequeña descripción de para que sirve cada comando. 

$git help

Otra forma es pedir informacion especifica de uno de los comandos con la siguiente instrucción:

$git help "comando_que_deseamos_conocer su información"

* Rm

El comando rm nos permite eliminar archivos dentro de nuestro repositorio, cabe señalar que al ser un comando de git, esto evita tener posibles errores si se eliminan con los comandos de linux usuales. 

$git rm "nombre_del_archivo_a_eliminar"

* Mv

Este comando es usado para mover o renombrar un archivo o un directorio especifico, para esto hay dos formas:

 Move or rename a file, directory or symlink.

          $git mv  "source" "destination"
          $git mv  "source" ... "destination directory"

       In the first form, it renames "source", which must exist and be either
       a file, symlink or directory, to "destination". In the second form, the
       last argument has to be an existing directory; the given sources will
       be moved into this directory.

       The index is updated after successful completion, but the change must
       still be committed.

* Log

El comando log nos permite ver los identificadores de los cambios hechos, esto, ya que es necesario cuando deseamos observar por terminal el cambio que existe en la version actual del repositorio, con una version especifica, dada por este identificador.

$git log

* Show

Git show nos permite ver la información del repositorio y ademas los cambios que hay en los dos ultimos commits.


$git rm "nombre_del_archivo"
 
* Merge:

Este comando nos permite fusionar los cambios hechos en una rama especifica (nombre_de_la_rama) con otra rama existente, por ejemplo la rama master, para que esto sea posible debemos estar en la rama a la cual queremos hacerle los cambios. A continuación se muestra el comando que tendria que usarse.

$git merge "nombre_de_la_rama" 

* Remote:

El comando remote nos permite actualizar un repositorio que no es de nuestra propiedad, y el cual hemos hecho un fork y posteriormente clonado de manera local. La manera de hacer esto es con el comando siguiente:

$git remote add --track "rama_a_la_que_deseo_asociar_los_cambios" "Alias_que_queremos_asociar_el_repositorio_original" "link_con_el_que_clonamos_repositorios_en_este_caso_el_del_propietario"

Para entenderlo mejor pondremos un ejemplo concreto, supongamos que nos interesa hacer un fork de un repositorio especifico, posteriormente al tenerlo en nuestro repositorio y hacer una copia de manera local al creador o propietario del repositorio se le ocurre subir algunos cambios, al nosotros estar interesados en tener esos cambios debemos decirle a git que se trata de un repositorio remoto, y no de un repositorio propio.

Ejemplo:

$git remote add --track master Axel https://github.com/AxelRojas/ejercicioJueves.git

En esta parte le estamos diciendo a git que los cambios que el propietario hizo los asocie a nuestra rama master local, posteriormete el Alias, en este caso Axel, puede ser cualquier cosa, ya sea nombre o apodo, y este nos servira más adelante para poder jalar los datos nuevos a nuestro copia local, es importante recordar este nickname para poder actualizar nuestro repositorio, y posteriormente se adjunta la liga, indicandole a git de donde esta ese repositorio original.


