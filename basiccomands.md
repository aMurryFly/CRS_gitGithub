# :boom: Comando Básicos para el manejo de Git/Git-Hub :boom:

## Acerca del documento :point_up:

*Éste ha sido creado con la finalidad de plasmar los conocimientos adquiridos en el curso de manejo de Git/Git-Hub por parte del Taller de Robótica Abierta, para el buen manejo de estas dos grandes herramientas, orientada a la realizacion de proyectos multidiciplinarios, y el buen manejo de estos.*

## Lista de Comandos

* Add

Este comando agrega un archivo al repositorio y lo prepara para un commit

`$git add <nombre del archivo>`


* Commit

Crea un commit con la opción de agreagar un mensaje

`$git commit -m "Descripción del commit hecho"`

* Checkout 

Comando utilizado para cambiar de rama

`$git checkout <nombre de la rama>`

* Push

Actualiza cambios desde el repositorio local al mismo repositorio remoto

`$git push`


* Pull

Incorpora cambios de un repositorio remoto en la rama actual 

`$git pull`


* Clone 

Clona un repositorio dentro de un directorio previamente creado

`$git clone <URL del repositorio a clonar>`


* Branch 

Comando utilizado para listar, crear o eliminar ramas 

`$git branch`


* Status

Este comando nos permite ver el estado actual de nuestro repositorio, en este caso si este se encuentra actualizado con el repositorio remoto y nos indica si hay algun cambio.

`$git status`
 
* Help

Este comando nos permite listar, valga la redundancia, los comandos más usados en git, esto con el proposito de tener una herramienta por si no recordamos el comando especifico a utilizar. Tambien tiene uan pequeña descripción de para que sirve cada comando. 

`$git help`

Otra forma es pedir informacion especifica de uno de los comandos con la siguiente instrucción:

`$git help "comando_que_deseamos_conocer su información"`

* Rm

El comando rm nos permite eliminar archivos dentro de nuestro repositorio, cabe señalar que al ser un comando de git, esto evita tener posibles errores si se eliminan con los comandos de linux usuales. 

`$git rm "nombre_del_archivo_a_eliminar"`

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

`$git log`

* Show

Git show nos permite ver la información del repositorio y ademas los cambios que hay en los dos ultimos commits.


`$git rm "nombre_del_archivo"`
 
* Merge:

Este comando nos permite fusionar los cambios hechos en una rama especifica (nombre_de_la_rama) con otra rama existente, por ejemplo la rama master, para que esto sea posible debemos estar en la rama a la cual queremos hacerle los cambios. A continuación se muestra el comando que tendria que usarse.

`$git merge "nombre_de_la_rama" `

* Remote:

El comando remote nos permite actualizar un repositorio que no es de nuestra propiedad, y el cual hemos hecho un fork y posteriormente clonado de manera local. La manera de hacer esto es con el comando siguiente:

`$git remote add --track "rama_a_la_que_deseo_asociar_los_cambios" "Alias_que_queremos_asociar_el_repositorio_original" "link_con_el_que_clonamos_repositorios_en_este_caso_el_del_propietario"`

Para entenderlo mejor pondremos un ejemplo concreto, supongamos que nos interesa hacer un fork de un repositorio especifico, posteriormente al tenerlo en nuestro repositorio y hacer una copia de manera local al creador o propietario del repositorio se le ocurre subir algunos cambios, al nosotros estar interesados en tener esos cambios debemos decirle a git que se trata de un repositorio remoto, y no de un repositorio propio.

Ejemplo:

`$git remote add --track master Axel https://github.com/AxelRojas/ejercicioJueves.git`

En esta parte le estamos diciendo a git que los cambios que el propietario hizo los asocie a nuestra rama master local, posteriormete el Alias, en este caso Axel, puede ser cualquier cosa, ya sea nombre o apodo, y este nos servira más adelante para poder jalar los datos nuevos a nuestro copia local, es importante recordar este nickname para poder actualizar nuestro repositorio, y posteriormente se adjunta la liga, indicandole a git de donde esta ese repositorio original.

* Config

Configura la información del usuario para todos los repositorios locales. La herramienta config se puede utilizar de las siguientes formas:

`$ git config --global user.name "[nombre]"`

Establece el nombre que desea adjuntar a sus transacciones de confirmación (commit).

`$ git config --global user.email "[dirección de correo electrónico]"`

Establece el correo electrónico que desea adjuntar a sus transacciones de confirmación (commit).

`$ git config --global color.ui auto`

Habilita un coloreado útil para la salida de la línea de comandos. 

* Init

Inicia un nuevo repositorio mediante la línea de comandos. El uso de este comando es: 

`$ git init [nombre-de-proyecto]`

Esto crea un nuevo repositorio local con el nombre especificado

* Diff

Muestra cambios entre commits, entre commit y árbol de trabajo, etc. Funciona para diferentes opciones, desde cambios en dos archivos, árboles de trabajo hasta cambios resultantes de hacer merge. 

`$ git diff`

Muestra diferencias de archivos aún no preparadas (staged).

Por ejemplo en el curso de git-github se mostró que diff funciona para mostrar las diferencias entre dos commits realizados, utilizando los identificadores de los commits para hacer referencia a cada uno de ellos. Por ejemplo:

`$ git diff [identificador-del-commit]`

Compara y muestra las diferencias entre el último commit realizado y el commit cuyo identificador se especifica.

`$ git diff --staged`

Muestra diferencias de archivos entre la versión "staging" y la última versión del archivo.

`$ git diff [first-branch]...[second-branch]`

Muestra las diferencias de contenido entre dos ramas.

* Reset

`$ git reset [file]`

Des-efectua o demonta (unstage) el archivo, pero mantiene sus contenidos.

`$ git reset [commit]`

Deshace todos los commits después de [commit], manteniendo los cambios de forma local.

`$ git reset --hard [commit]`

Descarta todo el historial y vuelve a cambiar al commit que se especifica.

* Fetch

Cuando se utiliza git fetch, se agregan los cambios desde el repositorio remoto a la rama de trabajo local sin confirmarlos (committing). A diferencia de git pull, "fetching" permite revisar los cambios antes de confirmarlos (committing) hacia la rama local.

`$ git fetch [bookmark]`

Descarga todo el historial desde el repositorio especificado (desde el bookmark).
