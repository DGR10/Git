# Reescribiendo la historia

Muchas veces, al trabajar con Git, vas a querer confirmar tu historia por alguna razón. Una de las grandes cualidades de Git es que te permite tomar decisiones en el último momento.

Puede decidir qué archivos entran en juego antes de comprometerse con el área de ensayo, puedes decidir que no querías estar trabajando en algo todavía con el comando de alijos, y puedes reescribir confirmaciones que ya hayan pasado haciendo parecer que fueron hechas de diferente manera.

## Cambiando última confirmación

Cambiar la última confirmación es probablemente lo más común que le harás a tu historia.

Si solamente quieres cambiar la confirmación del mensaje final, es muy sencillo:

```
$ git commit --amend
```