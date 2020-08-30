# Acerca del Control de Versiones

Un control de versiones es un sistema que registra los cambios realizados en un archivo o conjunto de archivos a lo largo del tiempo, de modo que puedas recuperar versiones específicas más adelante.

Si eres diseñador gráfico o de web y quieres mantener cada versión de una imagen o diseño (es algo que sin duda vas a querer), usar un sistema de control de versiones (VCS por sus siglas en inglés) es una decisión muy acertada. 

Dicho sistema te permite regresar a versiones anteriores de tus archivos, regresar a una versión anterior del proyecto completo, comparar cambios a lo largo del tiempo, ver quién modificó por última vez algo que pueda estar causando problemas, ver quién introdujo un problema y cuándo, y mucho más. Usar un VCS también significa generalmente que si arruinas o pierdes archivos, será posible recuperarlos fácilmente.

Hay tres tipos de VCS:

- Sistemas de Control de Versiones Locales -> Contenían una simple base de datos, en la que se llevaba el registro de todos los cambios realizados a los archivos.

- Sistemas de Control de Versiones Centralizado -> Tienen un servidor que contiene todos los archivos versionados y varios clientes que descargan los archivos desde ese lugar central. Si el servidor se cae, se pierden los archivos.

- Sistemas de Control de Versiones Distribuidos -> Los clientes no solo descargan la última copia instantánea de los archivos, sino que se replica completamente el repositorio. Si falla el servidor, cualquiera de los repositorios clientes puede ser copiado a un nuevo servidor. 