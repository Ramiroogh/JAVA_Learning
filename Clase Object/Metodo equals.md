# equals()
El método equals, junto con los métodos toString y hashCode, es uno de los métodos fundamentales de la clase Object.

La firma correcta para este metodo es:
``` java
public boolean equals(Object ref)
```
+ es público, devuelve boolean y recibe un Objeto.

### Definición
El método equals() de la clase Object en Java se utiliza para verificar la igualdad entre dos objetos. Este método compara el contenido de los objetos en lugar de simplemente comparar las referencias de memoria.

Por defecto, el método equals() en la clase Object realiza una comparación de igualdad por referencia, es decir, dos objetos son considerados iguales solo si son exactamente la misma instancia en memoria. Sin embargo, la mayoría de las clases en Java sobrescriben este método para proporcionar su propia lógica de igualdad.

Por ejemplo, supongamos que tienes una clase Persona con atributos como nombre y edad. Para realizar una comparación basada en el contenido de los objetos Persona, deberías sobrescribir el método equals() en la clase Persona. Aquí hay un ejemplo:
``` java
public class Persona {
    private String nombre;
    private int edad;

    // Constructor y otros métodos de la clase

    @Override
    public boolean equals(Object obj) {
        if (this == obj) {
            return true;
        }

        if (obj == null || getClass() != obj.getClass()) {
            return false;
        }

        Persona persona = (Persona) obj;
        return edad == persona.edad && Objects.equals(nombre, persona.nombre);
    }
}
```
En este ejemplo, se utiliza el método equals() para comparar el contenido de dos objetos Persona basándose en el nombre y la edad. Si el nombre y la edad son iguales en ambos objetos, se consideran iguales.

+ Es importante tener en cuenta que al sobrescribir el método equals(), también es recomendable sobrescribir el método hashCode() para mantener la consistencia entre ambos. Esto es necesario para que los objetos puedan funcionar correctamente en colecciones basadas en hash, como HashSet y HashMap.