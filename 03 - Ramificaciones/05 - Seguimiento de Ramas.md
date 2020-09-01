# Seguimiento de ramas

Al activar (checkout) una rama local a partir de una rama remota, se crea automáticamente lo que podríamos denominar una “rama de seguimiento” (tracking branch). 

Las ramas de seguimiento son ramas locales que tienen una relación directa con alguna rama remota. 

Si estás en una rama de seguimiento y tecleas el comando __git pull__, Git sabe de cuál servidor recuperar (fetch) y fusionar (merge) datos.

## Preparar Ramas para seguimiento

```
$ git checkout --track [nombreRemoto]/[nombreRama]
```

Para preparar una rama local con un nombre distinto a la del remoto, puedes utilizar la primera versión con un nombre de rama local diferente:

```
$ $ git checkout -b sf [nombreRemoto]/[nombreRama]
```

Así, tu rama local sf traerá (pull) información automáticamente desde [nombreRemoto]/[nombreRama].

Si ya tienes una rama local y quieres asignarla a una rama remota que acabas de traerte, o quieres cambiar la rama a la que le haces seguimiento, puedes usar en cualquier momento las opciones __-u__ o __--set-upstream-to__ del comando __git branch__.

```
$ git branch -u [nombreRemoto]/[nombreRama]
```

Para ver las ramas de seguimiento que tienes asignadas:

```
$ git branch -vv
```