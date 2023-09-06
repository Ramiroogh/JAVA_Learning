Nos permite crear de forma automatica las tablas columnas y elementos existentes en la base de datos, y enfocarnos unicamente en jpa y hibernate.

Este archivo contendra las diferentes unidades de persistencia y las propiedades para la base de datos.

Para crear este archivo de configuracion, primero se debe respetar un orden jerarquico de Carpetas para que la Aplicación funcione:

+ proyecto/src/main/resources
+ En la carpeta de nuestro proyecto, ir a main y en la Carpeta Resources, crear una carpeta llamada META-INF.
<br>
+ Luego en esa misma carpeta, crear un archivo con extension XML, y de nombre colocar 'persistence'.
+ persistence.xml

## Tag <persistence-unit>
Sirve para Agrupar las configuraciones de una unidad de persistencia, que representa una base de datos utilizada por la aplicación.