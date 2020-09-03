# Flujo de Trabajo Administrador-Integración

Debido a que Git permite tener múltiples repositorios remotos, es posible tener un flujo de trabajo donde cada desarrollador tenga acceso de escritura a su propio repositorio público y acceso de
lectura a todos los demás. 

Este escenario a menudo incluye un repositorio canónico que representa
el proyecto "oficial". Para contribuir a ese proyecto, creas tu propio clon público del proyecto y haces pull con tus cambios. 

Luego, puede enviar una solicitud al administrador del proyecto principal para que agregue los cambios. Entonces, el administrador agrega el repositorio como remoto, prueba los cambios localmente, los combina en su rama y los envía al repositorio. El
proceso funciona de la siguiente manera. 

1. El administrador del proyecto hace un push al repositorio público.

2. El contribuidor clona ese repositorio y realiza los cambios.

3. El contribuidor realiza un push con su copia pública del proyecto.

4. El contribuidor envía un correo electrónico al administrador pidiendo que haga pull de los cambios.

5. El administrador agrega el repositorio del contribuidor como remoto y fusiona ambos localmente.

6. El administrador realiza un push con la fusión del código al repositorio principal.

Este es un flujo de trabajo muy común con herramientas basadas en hubs como GitHub o GitLab, donde es fácil hacer un fork de un proyecto e introducir los cambios en este fork para que todos
puedan verlos. 

Una de las principales ventajas de este enfoque es que el contribuidor puede continuar realizando cambios y el administrador principal del repositorio puede incorporar los cambios en cualquier momento. 

Los contribuidores no tienen que esperar a que el proyecto
incorpore sus cambios; cada parte puede trabajar a su propio ritmo.