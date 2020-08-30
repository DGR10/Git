# Deshacer cosas

En cualquier momento puede que quieras deshacer algo.  Ten cuidado, a veces no es posible recuperar algo luego que lo has deshecho. 

```
$ git commit --amend
```

## Deshacer un archivo preparado

Supongamos que has cambiado dos archivos y que quieres confirmarlos como dos cambios separados, pero accidentalmente has escrito git add * y has preparado ambos. ¿Cómo puedes sacar del área de
preparación uno de ellos?

```
$ git reset HEAD [nombreArchivo]
```

## Deshacer un archivo modificado

Para restaurar fácilmente un archivo o volver al estado en el que estaba en su última confirmación.

```
$ git checkout -- [nomreArchivo]
$ git restore [nombreArchivo]
```