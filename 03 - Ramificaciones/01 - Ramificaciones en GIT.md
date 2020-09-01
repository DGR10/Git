# ¿Que es un rama?

Una rama Git es simplemente un apuntador móvil apuntando a una de esas confirmaciones. La rama por defecto de Git es la rama __master__. Con la primera confirmación de cambios que realicemos (commit),
se creará esta rama principal __master__ apuntando a dicha confirmación. En cada confirmación de cambios que realicemos, la rama irá avanzando automáticamente.

## Crear una nueva Rama

```
$ git branch [nombreRama] (Crea la rama pero no salta a ella)
```

Esto creará un nuevo apuntador apuntando a la misma confirmación donde estés actualmente (último commit).

> HEAD en GIT es simplemente el apuntador a la rama local en la que tú estés en ese momento.

## Cambiar de Rama

```
$ git checkout [nombreRama]
```

Esto mueve el apuntador __HEAD__ a la rama [nombreRama] y revierte
los archivos de tu directorio de trabajo; dejándolos tal y como estaban en la última instantánea confirmada en dicha rama master.

## Fusión de Ramas

```
$ git checkout [nombreRama] (Rama sobre la que queremos fusionar)
$ git merge [nombreRama] (Rama que fusionamos)
```

Debemos estar sobre la rama que queremos que se apliquen los cambios. Un ejemplo sería que sobre la rama __master__ aplicaramos los cambios de la rama __hotfix__: _$ git merge hotfix_.

Si hay conflictos deberemos resolverlos manualmente.

```
<<<<<<< HEAD:index.html
<div id="footer">contact : email.support@github.com</div>
=======
<div id="footer">
 please contact us at support@github.com
</div>
>>>>>>> iss53:index.html

```

Donde nos dice que la versión en HEAD (la rama master, la que habías activado antes de lanzar el comando de fusión) contiene lo indicado en la parte superior del bloque (todo lo que está encima de =======) y que la versión en iss53 contiene el resto, lo indicado en la parte inferior del bloque. 

## Borrar una rama

```
$ git branch -d [nombreRama]
```