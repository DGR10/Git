# Cambios

## Ver Cambios preparados  y no preparados

Si el comando git status es muy impreciso para ti - quieres ver exactamente que ha cambiado, no solo cuáles archivos lo han hecho - puedes usar el comando __git diff__.

Se utiliza para responder estas 2 preguntas:

- ¿Qué has cambiado pero aun no has preparado?
- ¿Qué has preparado y está listo para confirmar? 

__git diff__ muestra las lineas exactas que fueron añadidas y eliminadas.

__git diff --cached_ sirve para ver que has preparado hasta ahora (--staged y --cached son sinónimos)

## Confirmar tus cambios

Ahora que tu área de preparación está como quieres, puedes confirmar tus cambios. Recuerda que cualquier cosa que no esté preparada - cualquier archivo que hayas creado o modificado y que no hayas agregado con git add desde su edición - no será confirmado.

```
$ git commit
$ git commit -v (Muestra más información en el editor)
$ git commit -m "Comentario" (Forma corta de hacer una confirmación desde consola sin tener que abrir el editor)
```

## Saltarse el area de preparación

```
$ git commit -a -m "añadir archivos"
```

En este caso no es necesario utilizar el comando git add antes de confirmar los cambios.

## Eliminar archivos

Para eliminar archivos de Git, debes eliminarlos de tus archivos rastreados (o mejor dicho, eliminarlos del área de preparación) y luego confirmar. 

Para ello existe el comando __git rm__, que además elimina el archivo de tu directorio de trabajo de manera que no aparezca la próxima vez
como un archivo no rastreado.

```
$ git rm [nombreArchivo]
$ git rm -f [nombreArchivo] (Lo elimina incluso de preparado)
$ git rm --cached [nombreArchivo] (Lo saca de preparado y lo deja en no preparado)
```

Con la próxima confirmación, el archivo habrá desaparecido y no volverá a ser rastreado. Si modificaste el archivo y ya lo habías añadido al índice, tendrás que forzar su eliminación con la opción -f. Esta propiedad existe por seguridad, para prevenir que elimines accidentalmente datos que aun no han sido guardados como una instantánea y que por lo tanto no podrás recuperar luego con Git.

## Renombrando archivos

```
$ git mv [nombreArchivo] [nuevoNombreArchivo]
```