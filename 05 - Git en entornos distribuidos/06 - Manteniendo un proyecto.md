# Manteniendo un proyecto

Además de saber cómo contribuir de manera efectiva a un proyecto, probablemente necesitarás saber cómo mantenerlo. 

Esto puede comprender desde aceptar y aplicar parches generados vía format-patch enviados por e-mail, hasta integrar cambios en ramas remotas para repositorios quehas añadido como remotos a tu proyecto. 

## Trabajando en ramas puntuales

Cuando estás pensando en integrar nuevo trabajo, generalmente es una buena idea probarlo en una rama puntual (topic branch) - una rama temporal específicamente creada para probar ese nuevo trabajo. 

De esta forma, es fácil ajustar un parche individualmente y abandonarlo si no funciona hasta que tengas tiempo de retomarlo. 

## Aplicando parches recibidos por email

Si recibes por e-mail un parche que necesitas integrar en tu proyecto, deberías aplicarlo en tu rama puntual para evaluarlo. 

Hay dos formas de aplicar un parche enviado por e-mail: con __git apply__ o __git am__.

### Aplicando con apply

Si recibiste el parche de alguien que lo generó con git diff o con el comando Unix diff, puedes aplicarlo con el comando git apply.

```
$ git apply [ruta_del_parche]
$ git apply --check [ruta_del_parche] (Para comprobar si un parche se aplica de forma limpia antes de aplicarlo)
```

Esto modifica los archivos de tu directorio de trabajo.

> La diferencia entre apply y patch es que apply sigue un modelo que aplica todo o no aplica nada.

### Aplicando con am

Si el colaborador es usuario de Git y conoce lo suficiente como para usar el comando format-patch para generar el parche, entonces tu trabajo es más sencillo, puesto que el parche ya contiene información del autor y un mensaje de commit. 

Si puedes, anima a tus colaboradores a usar formatpatch en lugar de diff para generar parches. Sólo deberías usar git apply para parches antiguos y cosas similares.

Técnicamente, git am se construyó para leer de un archivo mbox (buzón de correo). Es un formato de texto plano simple para almacenar uno o más mensajes de correo en un archivo de texto. 

```
$ git am [ruta_del_parche]
```

Puedes ver que aplicó el parche limpiamente y creó automáticamente un nuevo commit.

## Recuperando ramas remotas

Si recibes una contribución de un usuario de Git que configuró su propio repositorio, realizó cambios en él y envió la URL del repositorio junto con el nombre de la rama remota donde están los cambios, puedes añadirlo como una rama remota y hacer integraciones (merges) de forma local.

## Etiquetando tus versiones

Cuando decides lanzar una versión, probablemente quieras etiquetarla para poder generarla más adelante en cualquier momento. 