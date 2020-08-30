# Trabajar con Remotos

Para poder colaborar en cualquier proyecto Git, necesitas saber cómo gestionar repositorios remotos. Los repositorios remotos son versiones de tu proyecto que están hospedadas en Internet o en cualquier otra red. 

Puedes tener varios de ellos, y en cada uno tendrás generalmente permisos de solo lectura o de lectura y escritura. Colaborar con otras personas implica gestionar estos repositorios remotos enviando y trayendo datos de ellos cada vez que necesites compartir tu trabajo. Gestionar repositorios remotos incluye saber cómo añadir un repositorio remoto, eliminar los remotos que ya no son válidos,gestionar varias ramas remotas, definir si deben rastrearse o no y más.

## Ver tus Remotos

```
$ git remote
$ git remote -v (Muestra las url que git asocia al nombre)
```

## Añadir Repositorios Remotos

```
git remote add [nombre] [url]
```

Con este comando se puede utilizar el nombre dado en vez de la url.

## Traer y Combinar Remotos

```
$ git fetch [nombre-remoto]
```

El comando irá al proyecto remoto y se traerá todos los datos que aun no tienes de dicho remoto. Luego de hacer esto, tendrás referencias a todas las ramas del remoto, las cuales puedes combinar e inspeccionar cuando quieras.

Es importante destacar que el comando git fetch solo trae datos a tu repositorio local - ni lo combina automáticamente con tu trabajo ni modifica el trabajo que llevas hecho. La combinación con tu trabajo debes hacerla manualmente cuando estés listo.

> La diferencia con git pull es que git pull trae y combina automaticamente los cambios mientras que git fetch solo los trae y se combina manualmente.

## Enviar a tus Remotos

```
$ git push [nombre-remoto] [nombre-rama]
```

## Inspeccionar un remoto

Si quieres ver más información acerca de un remoto en particular, puedes ejecutar el comando:

```
$ git remote show
$ git remote show [nombre-remoto] (Muestra la información del remoto y la información del rastreo de ramas)
```

## Eliminar y Renombrar Remotos

Comando para eliminar:

```
$ git remote rm [nombreRemoto]
```

Comando para renombrar:

```
$ git remote rename [nombreActual] [nuevoNombre]
```