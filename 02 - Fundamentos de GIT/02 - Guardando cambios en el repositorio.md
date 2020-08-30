# Guardando cambios en el Repositorio

Ya tienes un repositorio Git y un checkout o copia de trabajo de los archivos de dicho proyecto. El siguiente paso es realizar algunos cambios y confirmar instantáneas de esos cambios en el repositorio cada vez que el proyecto alcance un estado que quieras conservar.

Cada archivo de tu repositorio puede tener dos estados:

- Rastreado -> Aquellos que estaban en la última instantánea del proyecto, pueden ser archivos sin modificar, modificados o preparados.
- Sin rastrear -> Son el resto de archivos, todos los que son nuevos para tu repositorio.

## Revisando el Estado de tus Archivos

La herramienta principal para determinar qué archivos están en qué estado es el comando:

```
$ git status
``` 

## Rastreando Archivos Nuevos y Modificados

Para comenzar a rastrear un archivo debes usar el comando:

```
$ git add nombreArchivo
```

El comando __git add__ puede recibir tanto la ruta de un archivo como de un directorio (Se añaden todos los archivos dentro de él).

Es más útil que lo veas como un comando para “añadir este contenido a la próxima confirmación” más que para “añadir este archivo al proyecto".

Si modificamos un archivo y lo pasamos al estado __preparado__ y lo volvemos a abrir y a modificar, veremos que si hacemos un git status nos aparecen dos archivos, uno en __preparado__ y el otro en __no preparado__. Esto ocurre por que GIT prepara un archivo de acuerdo al estado que tenía cuando ejecutas el comando git add.

Si confirmas ahora, se confirmará la versión de que tenías la última vez que ejecutaste git add y no la versión que ves ahora en tu directorio de trabajo al ejecutar git status. 

Si modificas un archivo luego de ejecutar git add, deberás ejecutar git add de nuevo para preparar la última versión del archivo

## Estado abreviado

GIT ofrece una opción para obtener un estado abreviado, de manera que puedas ver tus cambios de una forma más compacta. 

```
$ git status -s
```