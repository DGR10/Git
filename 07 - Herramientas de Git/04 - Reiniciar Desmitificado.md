# Reiniciar Desmitificado

HEAD es el puntero a la referencia de bifurcación actual, que es, a su vez, un puntero al último commit realizado en esa rama. 

Eso significa que HEAD será el padre del próximo commit que se cree. En general, es más simple pensar en HEAD como la instantánea de tu último commit.

El índice es tu siguiente commit propuesto. También nos hemos estado refiriendo a este concepto como el “Área de Preparación” de Git ya que esto es lo que Git ve cuando ejecutas git commit.

## Reset

El comando reset tiene más sentido cuando se ve en este contexto.

```
$ git reset [commit]
```

Lo primero que reset hará es mover a lo que HEAD apunta.

```
$ git reset --soft HEAD~ (Deshace el último commit )
```

Lo siguiente que reset hará es actualizar el Índice con los contenidos de cualquier instantánea que
HEAD señale ahora.

## Checkout

```
$ git checkout [branch] (Actualiza la información para que se vea como está en la rama)
```

A diferencia de Reset está en el directorio-de-trabajo seguro; Verificará para asegurarse de que no está volando los archivos que tienen cambios en ellos. 
La segunda diferencia importante es cómo actualiza HEAD. Donde reset moverá la rama a la que HEAD apunta, checkout moverá HEAD para señalar otra rama.