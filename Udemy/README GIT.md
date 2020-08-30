# Nota 01 Inicio

git init --> Inizializamos el repositorio

git status --> Vemos el estado de los archivos del proyecto

git add . | nombreArchivo --> Tomamos "foto" del estado del proyecto

git checkout -- . --> Volvemos a la versión más reciente de la que hicimos captura

# Nota 02.1 Añadiendo SOLO los archivos que nos interesan

git add index.html --> Añade un archivo

git add *.png --> Añade todos los archivos con X extensión

git add css/ --> Añade todos los archivos dentro de X carpeta

git reset *.xml --> Para excluir todos los archivos del stage con una extensión

# Nota 02.2 Mirando el LOG

git log --> Nos muestra todos los commits realizados

git log --oneline --> Nos muestra todos los commits en una linea

git log --oneline --decorate --all --graph --> Nos muestra mejor el git status, nos permite diferenciar ramas

git status -s -->  Mostrar solo los archivos que se han modificado y estan en el stage

git status -s -b --> Saber en que rama estamos trabajando manteniendo el -s

# Nota 02.3 Creando alias

git config --global alias.lg "log --oneline --decorate --all --graph" --> .lg es como se va a llamar el comando a ejecutar todo lo demás. Por ejemplo: git lg

# Nota 03.1 Diferenciando archivos

git diff --> Muestra las lineas que han cambiado entre el commit y lo que hemos modificado

git diff --staged --> Muestra las lineas que han cambiado pero mirando los archivos que hay en el staged

# Nota 03.2 Actualizar mensaje del commit y revertir commits

git commit --amend -m "Actualizamos el readme"

# Nota 03.3 Modificar ultimo commit echo

git reset --soft HEAD^

HEAD apunta al ultimo commit realizado

# Nota 04 Viajes en el tiempo

git reset --mixed 49b34a1 --> Movernos a un punto en concreto

git reset --hard 49b34a1 --> Nos mueve a ese commit y elimina lo que agregamos después, también puede llevarnos a uno que hayamos eliminado.

git reflog --> Nos muestra la historia de los cambios que fuimos haciendo

git mv destruir-mundo.txt salvar-mundo.txt

git rm salvar-mundo.txt --> Elimina el archivo

# Archivo .gitignore 

En este fichero introducimos los archivos o carpetas que no queremos que se suban a git. Por ejemplo: *.log

# Nota 05 Tarea

# Nota 06.1 RAMAS

Es una linea de tiempo de commits diferente de la principal (master)

Merge --> Unir una rama a otra, para unir dos ramas, tenemos que estar en la rama que queremos que se fusione.

Tipos:

    - Fast-forward
    - Uniones automáticas
    - Manual

git branch rama-villanos --> Creamos una rama

git checkout -b rama-villanos --> Creamos la rama y nos movemos a ella

git checkout rama-villanos --> Nos movemos a la rama con ese nombre

git diff rama-villanos master --> Nos muestra las diferencias entre estas dos ramas

git merge rama-villanos --> Esto nos mezcla las dos ramas con fast-forward

git merge rama-villanos --> Nos mezla las ramas con Union automática

git branch -d rama-villanos --> Eliminar rama

# Nota 06.2 TAGS

Son una referencia a un commit específico

git tag superRelease --> Creamos un tag

git tag --> Muestra nuestros tags

git tad -d superRelease --> Borra el tag introducido

git tag -a v1.0.0 -m "Versión 1.0.0" --> Nos crea el tag en el lugar donde estamos

git tag -a v0.1.0 345d7de -m "Versión 0.1.0" --> Nos crea el tag en el commit señalado

git show v1.0.0 --> Nos muestra la información del tag

# Nota 07: STASH

Es como una caja o un contenedor en el cual nosotros podemos poner todos los cambios temporales y después recuperarlos.

git stash --> Esto salva el estado actual de la rama

git stash save "Mensaje" --> Guardamos el stash con un mensaje

git stash pop --> Recuperamos los cambios del stash y la borramos

git stash apply --> Recuperamos la ultima entrada del stash

git stash apply stash@{1} --> De la lista de stash decimos que queremos la posicion 1

git stash list --> Nos muestra todos los cambios temporales

git show stash --> Nos muestra más información

git stash drop --> Se elimina el ultimo cambio en el stash

git stash drop stash@{2}  --> Se elimina el stash seleccionado

git stash clear --> Borra todas las entradas en el stash

# Nota 08: REBASE

git rebase --> Crea un area temporal en el cual se mueven los dos commits de la rama y luego va a mover el puntero de la rama misiones hacia el ultimo commit de la rama master y por ultimo va a regresar los dos commits que están en el area temporal.

git rebase master --> master será la rama que quiero que haga los commits

git rebase -i HEAD~4 --> Esto nos permite mezclar los ultimos 4 commits en un commit, en el editor cambiar pick por p o por s (Mezclar)

git rebase -i HEAD~1 --> En el editor cambiar pick por r (Renombrar) o podemos usar e (Editar/Separar)

git checkout -- nombre del archivo --> Nos vuelve a poner el archivo como estaba originalmente

git rebase --continue


