# Alias de Git

Git no deduce automáticamente tu comando si lo tecleas parcialmente. Si no quieres teclear el nombre completo de cada comando de Git, puedes establecer fácilmente un alias para cada comando mediante git config.

```
$ git config --global alias.co checkout
$ git config --global alias.st status
$ git config --global alias.br branch
$ git config --global alias.l git log --oneline --graph --decorate --all
```