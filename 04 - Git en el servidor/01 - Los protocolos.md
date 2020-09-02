# Los protocolos

Git puede usar cuatro protocolos principales para transferir datos: Local, HTTP, Secure Shell (SSH) y Git. 

## Local Protocol

El más básico es el Protocolo Local, donde el repositorio remoto es simplemente otra carpeta en el disco. 

Se utiliza habitualmente cuando todos los miembros del equipo tienen acceso a un mismo sistema de archivos.

Para añadir un repositorio local a un proyecto Git existente, puedes usar algo como:

```
$ git remote add [nombreLocal] [nombre remoto]
```

## Protocolos HTTP

El protocolo HTTP “Inteligente” funciona de forma muy similar a los protocolos SSH y Git, pero se ejecuta sobre puertos estándar HTTP/S y puede utilizar los diferentes mecanismos de autenticación
HTTP. 

Esto significa que puede resultar más fácil para los usuarios, puesto que se pueden identificar mediante __usuario y contraseña__ (usando la autenticación básica de HTTP) en lugar de usar claves SSH.

## Protocolo SSH

SSH es un protocolo muy habitual para alojar repositorios Git en hostings privados. Esto es así porque el acceso SSH viene habilitado de forma predeterminada en la mayoría de los servidores, y si no es así, es fácil habilitarlo. Además, SSH es un protocolo de red autenticado sencillo de utilizar.

Para clonar un repositorio a través de SSH, puedes indicar una URL ssh:// tal como:

```
$ git clone ssh://usuario@servidor/proyecto.git
$ git clone usuario@server/proyecto.git
```

## Protocolo GIT

El protocolo Git es un “demonio” (daemon) especial, que viene incorporado con Git. Escucha por un puerto dedicado (9418) y nos da un servicio similar al del protocolo SSH; pero sin ningún tipo de autentificación.

Para que un repositorio pueda exponerse a través del protocolo Git, tienes que crear en él un archivo __git-daemon-export-ok__; sin este archivo, el “demonio” no hará disponible el repositorio.