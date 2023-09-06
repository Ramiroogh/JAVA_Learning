Primero que nada, se debe crear un paquete con una clase para empezar a trabajar de forma ordenada.
Luego intentaremos mapear, para que Hibernate pueda reconocer la clase como un modelo de entidad, se debe configurar ciertas cosas en la clase como:

+ Usar @Entity
en el IDE, al pasar el mouse, podremos usar dos maneras, esto al seleccionar click en una de estas, automaticamente nos importara un paquete como por ejemplo:
import javax.persistence.Entity;

+ Usar @Table
El nombre de la clase debe ser igual al de la tabla, en caso contrario de que no sea asi, hay que implementar lo siguiente:
Para que la clase, corresponda con el modelo de la base de datos que tenemos, tenemos que usarlo y importarlo automaticamente
@Table(name="productos")

# Llave Primaria
Para representarlo en nuestro modelo, debemos usar @Id, y tambien podemos usar @GeneratedValue(strategy=GenerationType.IDENTITY)
+ Siempre asegurarse de importar cada implementacion, al pasar el mouse con ayuda del IDE.