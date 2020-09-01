# Reorganizar el trabajo realizado

En Git tenemos dos formas de integrar cambios de una rama en otra: la fusión (merge) y la reorganización (rebase).

## Reorganización básica

En GIT puedes capturar todos los cambios confirmados en una rama y reaplicarlos sobre otra con el comando:

```
$ git rebase
```

Normalmente, la manera de sacar lo mejor de ambas es reorganizar tu trabajo local, que aún no has compartido, antes de enviarlo a algún lugar; pero nunca reorganizar nada que ya haya sido compartido.

Si hacemos hacemos commits y push y luego reorganizamos podemos romper el proyecto o perder parte del código si alguien trabaja sobre nuestro trabajo anterior.
