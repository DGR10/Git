# Configurando GIT por primera vez

Lo primero que deberás hacer cuando instales Git es establecer tu nombre de usuario y dirección de correo electrónico. 

```
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```

Para comprobar la configuración:

```
$ git config --list
$ git config <key> (user.name | user.email)
```

Para obtener ayuda:

```
$ git help <verb> (config)
$ git <verb> --help
```

Estos comandos son muy útiles porque puedes acceder a ellos desde cualquier sitio, incluso sin conexión. Si las páginas del manual y este libro no son suficientes y necesitas que te ayude una persona, puedes probar en los canales #git o #github del servidor de IRC Freenode (irc.freenode.net). Estos canales están llenos de cientos de personas que conocen muy bien Git y suelen estar dispuestos a ayudar.