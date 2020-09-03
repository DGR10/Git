# Flujo de Trabajo Dictador-Tenientes

Esta es una variante de un flujo de trabajo de múltiples repositorios. Generalmente es utilizado por grandes proyectos con cientos de colaboradores.

Un ejemplo famoso es el kernel de Linux. Varios administradores de integración están a cargo de ciertas partes del repositorio. 

Se les llaman “tenientes”. Todos los tenientes tienen un gerente de integración conocido como el “dictador benévolo”. 

El repositorio del dictador benevolente sirve como el repositorio de referencia del cual todos los colaboradores necesitan realizar pull.

1. Los desarrolladores trabajan en su propia rama especifica y fusionan su código en la rama master, la cual, es una copia de la rama del dictador.

2. Los tenientes fusionan el código de las ramas master de los desarrolladores en sus ramas master de tenientes.

3. El dictador fusiona la rama master de los tenientes a su rama master de dictador.

4. El dictador hace push del contenido de su rama master al repositorio para que otros fusionen los cambios a sus ramas.
