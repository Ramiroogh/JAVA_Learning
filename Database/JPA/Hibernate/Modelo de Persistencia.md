# Persistencia
Cuando un modelo de datos contiene una lógica de persistencia, quiere decir que guardara o registrará datos en la tabla en la que este apuntando, en la base de datos.

Luego de haber creado el archivo persistence.xml, crearemos la primera entidad dentro del package <<com.latam.alura.tienda.modelo>> con el nombre <<Producto>>

``` java
@Entity
@Table(name="productos")
public class Producto{
    @Id
    @GeneratedValue(strategy=GenerationType.IDENTITY)
    private Long id;

    private String nombre;
    private String descripcion;
    private BigDecimal precio;

    public Long getId() {    return id;}

    public void setId(Long id) {    this.id = id;}

    public String getNombre() {    return nombre;}

    public void setNombre(String nombre) {this.nombre = nombre;}

    public String getDescripcion() {return descripcion;}

    public void setDescripcion(String descripcion) {
        this.descripcion = descripcion;
}

    public BigDecimal getPrecio() {return precio;}

    public void setPrecio(BigDecimal precio) {this.precio = precio;}
}
```
Y por último vamos a crear una clase main donde vamos a instanciar el modelo <<Producto>> y el <<EntityManager> que nos va a permitir comunicarnos con la base de datos.
``` java
public class RegistroDeProducto {

    public static void main(String[] args) {

        Produto celular = new Produto();
            celular.setNombre("Xiaomi Redmi");
            celular.setDescripcion("Producto usado");
            celular.setPrecio(new BigDecimal("800"));

            EntityManagerFactory factory = Persistence.
            createEntityManagerFactory("tienda");

            EntityManager em = factory.createEntityManager();
            em.getTransaction().begin();
            em.persist(celular);
            em.getTransaction().commit();
            em.close();
    }
}
```