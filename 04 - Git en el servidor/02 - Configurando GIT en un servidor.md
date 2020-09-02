# Configurando Git en un servidor

Para configurar por primera vez un servidor de Git, hay que exportar un repositorio existente en un nuevo repositorio vacío - un repositorio que no contiene un directorio de trabajo. Esto es generalmente fácil de hacer. 

Para clonar el repositorio con el fin de crear un nuevo repositorio vacío, se ejecuta el comando clone con la opción __--bare__.

```
$ git clone --bare [nombreProyecto] [proyecto].git
```

## Colocando un Repositorio vacío en un Servidor

Ahora que tienes una copia vacía de tú repositorio, todo lo que necesitas hacer es ponerlo en un servidor y establecer sus protocolos. Digamos que has configurado un servidor llamado git.example.com que tiene acceso a SSH, y quieres almacenar todos tus repositorios Git bajo el directorio / opt` / git`. Suponiendo que existe / opt / git en ese servidor, puedes configurar tu nuevo repositorio copiando tu repositorio vacío a:

```
$ scp -r my_project.git user@git.example.com:/opt/git
```

Git automáticamente agrega permisos de grupo para la escritura en un repositorio apropiadamente si se ejecuta el comando git init con la opción __--shared__.

```
$ git init --bare --shared
```

## Generando tu clave pública SSH

Tal y como se ha comentado, muchos servidores Git utilizan la autentificación a través de claves públicas SSH. 

Para ello, cada usuario del sistema ha de generarse una, si es que ya no la tiene. El proceso para hacerlo es similar en casi cualquier sistema operativo. 

Ante todo, asegúrate que no tengas ya una clave. Por defecto, las claves de cualquier usuario SSH se guardan en la carpeta __~/.ssh__ de dicho usuario.

## Configurando el servidor

Vamos a avanzar en los ajustes de los accesos SSH en el lado del servidor. 

Comienzas creando un usuario git y una carpeta .ssh para él.

```
$ sudo adduser git
$ su git
$ mkdir .ssh && chmod 700 .ssh
$ touch .ssh/authorized_keys && chmod 600 .ssh/authorized_keys
```

A continuación se añaden las claves públicas de los desarrolladores al archivo __authorized_keys__ del usuario __git__.

Tras añadir todas las claves se prepara un repositorio básico vacio para ellos:

```
$ git init --bare
```

> Cabe indicar que alguien tendrá que iniciar sesión en la máquina y crear un repositorio básico, cada vez que se desee añadir un nuevo proyecto. 

## El demonio GIT

Ahora vamos a configurar un “demonio” sirviendo repositorios mediante el protocolo “Git”. Es la forma más común para dar acceso anónimo, pero rápido, a los repositorios. 

El protocolo Git es relativamente fácil de configurar. 

```
$ git daemon --reuseaddr --base-path=/opt/git/ /opt/git/
```

El parámetro --reuseaddr permite al servidor reiniciarse sin esperar a que se liberen viejas conexiones; el parámetro --base-path permite a los usuarios clonar proyectos sin necesidad de indicar su camino completo; y el camino indicado al final del comando mostrará al “demonio” Git, dónde buscar los repositorios a exportar. 

Si tienes un cortafuegos activo, necesitarás abrir el puerto 9418 para la máquina donde estás configurando el “demonio” Git.