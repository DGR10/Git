# Obteniendo un repositorio GIT

Puedes obtener un proyecto Git de dos maneras.

- Desde un proyecto o directorio existente
- Clonando un repositorio existente en GIT desde otro servidor

# Inicializando un repositorio en un directorio existente

```
$ git init
```

Crea un subdirectorio nuevo llamado .git, el cual contiene todos los archivos necesarios del repositorio – un esqueleto de un repositorio de Git. Todavía no hay nada en tu proyecto que esté bajo seguimiento. 

# Clonando un repositorio existente

Si deseas obtener una copia de un repositorio Git existente — por ejemplo, un proyecto en el que te gustaría contribuir — el comando que necesitas es __git clone__.

```
$ git clone [url]
```

Si quieres clonar el repositorio a un directorio con otro nombre que no sea el del repositorio, puedes especificarlo con la siguiente opción de línea de comandos:

```
$ git clone [url] nombreDirectorio
```

Ese comando hace lo mismo que el anterior, pero el directorio de destino se llamará nombreDirectorio.