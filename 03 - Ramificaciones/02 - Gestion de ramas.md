# Gestión de Ramas

Mostrar lista de ramas en el proyecto:

```
$ git branch
```

> El caracter * nos muestra en que rama estamos

 Para ver la última confirmación de cambios en cada rama, puedes usar el comando:
 
 ```
 $ git branch -v
 ```

 Para mostrar el estado de las ramas fusionadas o no fusionandas:

 ```
 $ git branch --merge (Las ramas que no llevan delante el * ya han sido mergeadas y podemos borrarlas)
 $ git branch --no-merge
 ```

 Si tratamos de borrar una rama que contiene trabajos sin fusionar nos dará error:

 ```
 $ git branch -d [nombreRama]
 $ git branch -D [nombreRama] (Si queremos borrarla de todas formas)
 ```