# Fontanería y porcelana

Los archivos HEAD e index (todavía por ser creado), y las carpetas objects y refs. Estos elementos forman el núcleo de Git. 

La carpeta objects guarda el contenido de tu base de datos, la carpeta refs guarda los apuntadores a las confirmaciones de cambios (commits), el archivo HEAD apunta a la rama que tengas activa (checked out) en este momento, y el archivo index es donde Git almacena la información sobre tu área de preparación (staging área).

## Los objetos

Git es un sistema de archivo orientado a contenidos. Estupendo. Y eso, ¿qué significa? 

Pues significa que el núcleo Git es un simple almacén de claves y valores. Cuando insertas cualquier tipo de contenido, él te devuelve una clave que puedes utilizar para recuperar de nuevo dicho contenido en cualquier momento. Para verlo en acción, puedes utilizar el comando de fontanería hash-object.

Este comando coge ciertos datos, los guarda en la carpeta .git. y te devuelve la clave bajo la cual se han guardado. 

## Referencias

Puedes utilizar algo así como git log 1a410e para echar un vistazo a lo largo de toda tu historia, recorriéndola y encontrando todos tus objetos. 

Pero para ello has necesitado recordar que la última confirmación de cambios es 1a410e. Necesitarías un archivo donde almacenar los valores de las sumas de comprobación SHA-1, junto con sus respectivos nombres simples que puedas utilizar como enlaces en lugar de la propia suma de comprobación.

En Git, esto es lo que se conoce como "referencias" o "refs"; en la carpeta .git/refs puedes encontrar esos archivos con valores SHA-1 y nombres . 

## La cabeza (HEAD)

El archivo HEAD es una referencia simbólica a la rama donde te encuentras en cada momento. 

Por referencia simbólica nos referimos a que, a diferencia de una referencia normal, esta contiene un enlace a otra referencia en lugar de un valor SHA-1. 

## Etiquetas

El objeto tipo etiqueta es muy parecido al tipo confirmación de cambios, --contiene un marcador, una fecha, un mensaje y un enlace--. Su principal diferencia reside en que generalmente apunta a una confirmación de cambios (commit) en lugar de a un árbol (tree). Es como una referencia a una rama, pero permaneciendo siempre inmóvil, --apuntando siempre a la misma confirmación de cambios--, dando un nombre mas amigable a esta.