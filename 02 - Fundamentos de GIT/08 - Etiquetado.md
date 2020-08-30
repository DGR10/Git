# Etiquetado

Listar las etiquetas disponibles en Git:

```
$ git tag
$ git tag -l 'v0*' (Listar por un patrón)
```

## Crear Etiquetas

Git utiliza dos tipos principales de etiquetas: ligeras y anotadas.

Una etiqueta ligera es muy parecido a una rama que no cambia - simplemente es un puntero a un commit específico.

Las etiquetas anotadas se guardan en la base de datos de Git como objetos enteros. Tienen un checksum; contienen el nombre del etiquetador, correo electrónico y fecha; tienen un mensaje asociado; y pueden ser firmadas y verificadas con GNU Privacy Guard (GPG). 

Normalmente se recomienda que crees etiquetas anotadas, de manera que tengas toda esta información; pero si quieres una etiqueta temporal o por alguna razón no estás interesado en esa información, entonces puedes usar las etiquetas ligeras.

## Etiquetas Anotadas

```
$ git tag -a [nombreTag] -m '[nombreMensaje]'
$ git show v1.1.0 (Se puede ver información de la etiqueta)
```

> -m especifica el mensaje de la etiqueda

## Etiquetas ligeras

Una etiqueta ligera no es más que el checksum de un commit guardado en un archivo - no incluye más información. Para crear una etiqueta ligera, no pases las opciones -a, -s ni -m.

```
$ git tag [nombreTag]
```

## Etiquetado tardío

Puedes etiquetar commits mucho tiempo después de haberlos hecho.

```
$ git tag -a [nombreTag] [checksum del commit]
```

## Compartir etiquetas

El comando git push no transfiere las etiquetas a los servidores remotos. Debes enviar las etiquetas de forma explícita al servidor luego de que las hayas creado.

```
$ git push origin [etiqueta]
$ git push --tags (Envia varias etiquetas a la vez)
```