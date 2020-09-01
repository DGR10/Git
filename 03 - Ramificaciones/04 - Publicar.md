# Publicar

Cuando quieres compartir una rama con el resto del mundo, debes llevarla (push) a un remoto donde tengas permisos de escritura. 

```
$ git push [nombreRemoto] [nombreRama]
$ git push [nombreRemoto] [nombreRamaLocal:nombreRamaRemoto]
```

Es importante destacar que cuando recuperas (fetch) nuevas ramas remotas, no obtienes automáticamente una copia local editable de las mismas. 

Para integrar (merge) esto en tu rama de trabajo actual, puedes usar el comando:

```
$ git merge [nombreRemoto]/[nombreRama] 
$ git checkout -b [nombreNuevaRama] [nombreRemoto]/[nombreRamaRemota]
```