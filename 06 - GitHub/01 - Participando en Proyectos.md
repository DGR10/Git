# Participando en proyectos

## Bifurcación (fork) de proyectos

Si quieres participar en un proyecto existente, en el que no tengas permisos de escritura, puedes bifurcarlo (hacer un “fork”). 

De esta forma, los proyectos no necesitan añadir colaboradores con acceso de escritura (push). 

La gente puede bifurcar un proyecto, enviar sus propios cambios a su copia y luego remitir esos cambios al repositorio original para su aprobación; creando lo que se llama un Pull Request, que veremos más adelante. 

Esto permite abrir una discusión para la revisión del código, donde propietario y participante pueden comunicarse acerca de los cambios y, en última instancia, el propietario original puede aceptarlos e integrarlos en el proyecto original cuando lo considere adecuado.

## El flujo de trabajo

El funcionamiento habitual es el siguiente:

1. Se crea una rama a partir de master.

2. Se realizan algunos commits hacia esa rama.

3. Se envía esa rama hacia tu copia (fork) del proyecto.

4. Abres un Pull Request en GitHub.

5. Se participa en la discusión asociada y, opcionalmente, se realizan nuevos commits.

6. El propietario del proyecto original cierra el Pull Request, bien fusionando la rama con tus cambios o bien rechazándolos.

Veamos un ejemplo:

```
$ git clone https://github.com/tonychacon/blink
$ git checkout -b slow-blink (Una vez estamos en la rama hacemos cambios)
$ git diff --word-diff
$ git commit -a -m 'three seconds is better'
$ git push origin slow-blink
```

Después en GitHub debemos ir a nuestra rama y solicitar pull request.

