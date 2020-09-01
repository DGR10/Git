# Traer y Fusionar

A pesar de que el comando git fetch trae todos los cambios que no tienes del servidor, este no modifica tu directorio de trabajo. 

Simplemente obtendrá los datos y dejará que tú mismo los fusiones. Sin embargo, existe un comando llamado git pull, el cuál básicamente hace git fetch seguido por git merge en la mayoría de los casos. 

Si tienes una rama de seguimiento configurada como vimos en la última sección, bien sea asignándola explícitamente o creándola mediante los comandos clone o checkout, git pull identificará a qué servidor y rama remota sigue tu rama actual, traerá los datos de dicho servidor e intentará fusionar dicha rama remota.