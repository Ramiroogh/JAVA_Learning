# Implements Keyword

Las interfaces funcionales salieron apartir de java 8, es decir java 1.8
<br>
La palabra clave implements en Java se utiliza para indicar que una clase está implementando una o varias interfaces.
+ Una interfaz es un conjunto de métodos abstractos (métodos sin implementación) que una clase concreta debe proporcionar. Al usar la palabra clave implements, estás *comprometiendo a la clase a proporcionar implementaciones concretas para los métodos definidos en la interfaz*.

Sintaxis:
La sintaxis básica de implements es la siguiente:
``` java
class MiClase implements Interfaz1, Interfaz2, ... {
    // Código de la clase
}
```
Donde MiClase es el nombre de la clase que implementa las interfaces Interfaz1, Interfaz2, etc.

### Interfaces:
Una interfaz es un tipo de contrato que define una serie de métodos que deben ser implementados por cualquier clase que implemente la interfaz. Las interfaces pueden también contener constantes (variables declaradas como static final) y métodos default (métodos con implementación) desde Java 8 en adelante.

En el mundo de Java, existen dos interfaces para definir los criterios para ordenar los elementos de una lista, estos son:
+ java.lang.Comparable
+ java.util.Comparator

### Implementación de Métodos:
Cuando una clase implementa una interfaz, debe proporcionar implementaciones concretas para todos los métodos definidos en la interfaz. Estas implementaciones deben seguir la firma (nombre, parámetros y tipo de retorno) especificada por la interfaz.

# Relación entre Clases e Interfaces:

Una clase puede implementar múltiples interfaces. Esto permite que una clase adquiera las características y funcionalidades definidas en varias interfaces diferentes.
La implementación de interfaces permite la **herencia múltiple**, que es una característica que Java no admite para las clases (una clase solo puede heredar de una clase base).

+ Una clase que implementa una interfaz debe proporcionar implementaciones para todos los métodos abstractos en esas interfaces, a menos que la clase sea abstracta también.

Ejemplo:
Aquí tienes un ejemplo simple que ilustra cómo usar la palabra clave implements:
``` java
interface Animal {
    void hacerSonido();
}

class Perro implements Animal {
    @Override
    public void hacerSonido() {
        System.out.println("Guau guau");
    }
}
```
+ La palabra clave implements es fundamental para establecer relaciones entre clases e interfaces en Java. Al implementar interfaces, puedes crear clases que cumplan ciertos contratos específicos y definir comportamientos compartidos por varias clases diferentes.