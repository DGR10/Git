## Nota 02.1: Añadiendo SOLO los archivos que nos interesan

git add index.html --> Añade un archivo

git add *.png --> Añade todos los archivos con X extensión

git add css/ --> Añade todos los archivos dentro de X carpeta

git reset *.xml --> Para excluir todos los archivos del stage con una extensión

## Nota 02.2 Mirando el LOG

git log --> Nos muestra todos los commits realizados

git log --oneline --> Nos muestra todos los commits en una linea

git log --oneline --decorate --all --graph --> Nos muestra mejor el git status, nos permite diferenciar ramas

git status -s -->  Mostrar solo los archivos que se han modificado y estan en el stage

git status -s -b --> Saber en que rama estamos trabajando manteniendo el -s

## Nota 02.3: Creando alias

git config --global alias.lg "log --oneline --decorate --all --graph" --> .lg es como se va a llamar el comando a ejecutar todo lo demás. Por ejemplo: git lg