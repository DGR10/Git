# Guardado y Limpieza

Muchas veces, cuando has estado trabajando en una parte de tu proyecto, las cosas se encuentran desordenadas y quieres cambiar de ramas por un momento para trabajar en algo más. 

El problema es que no quieres hacer un “commit” de un trabajo que va por la mitad, así puedes volver a ese punto más tarde. 

La respuesta a ese problema es el comando __git stash__.

```
$ git stash (Hace un guardado rápido)
$ git stash list (Muestra la lista de stash guardados)
$ git stash apply (Aplica el último stash guardado)
$ git stash drop (Elimina el último stash guardado)
$ git stash pop (Aplica y elimina el último stash guardado)
$ git stash -s (Guarda en el stash lo que no está en el stage)
```