# patron Iterator
Ahora sabes que hay muchas colecciones. Solo en este entrenamiento vimos ArrayList, LinkedList y Vector. Si aún ve el curso dedicado a las colecciones, aprenderá las interfaces para cola (Queue), conjunto (Set) y mapa (Map) cada una con varias implementaciones.

Aquí viene una pregunta: ¿Cómo puedo acceder (iterar) a todas estas implementaciones de manera uniforme sin conocer los detalles de cada implementación? La respuesta está en el "cuadro de patrón de diseño" y se llama Iterador.

+ Un Iterador es un objeto que tiene al menos dos métodos: hasNext() y next(). Es decir, puede usarlo para preguntar si hay un próximo elemento y pedir el próximo elemento. La buena noticia es que funciona con **TODAS** las implementaciones y esa es la gran ventaja.

Vea el código para usar el Iterador de una lista:
``` java
List<String> nombres = new ArrayList<>();
nombres.add("Super Mario");
nombres.add("Yoshi"); 
nombres.add("Donkey Kong"); 

Iterator<String> it = nombres.iterator();

while(it.hasNext()) {
  System.out.println(it.next());
}
```
Si comprende este código, ya ha aprendido a iterar con colas, conjuntos o mapas. Vea el uso de Iterator a través de un conjunto:

``` java
Set<String> nombres = new HashSet<>();
nombres.add("Super Mario");
nombres.add("Yoshi"); 
nombres.add("Donkey Kong"); 

Iterator<String> it = nombres.iterator();

while(it.hasNext()) {
  System.out.println(it.next());
}
```

## Definición
El patrón de diseño Iterator es un patrón de comportamiento que se utiliza comúnmente en la programación orientada a objetos para proporcionar una forma uniforme de acceder a los elementos de una colección de objetos sin exponer los detalles internos de la estructura de la colección. Este patrón *promueve la separación de la lógica de acceso a los elementos de la lógica de la estructura de datos subyacente*, lo que hace que el código sea más flexible y fácil de mantener.

El patrón Iterator consta de los siguientes componentes clave:

+ Iterador (Iterator): Define una interfaz que declara métodos para acceder a los elementos de la colección. Los métodos típicos incluyen next() para obtener el siguiente elemento y hasNext() para verificar si hay más elementos disponibles.

+ Colección (Aggregate): Define una interfaz que declara un método para crear un objeto iterador. Esta interfaz puede representar una colección de elementos, como una lista, un conjunto o un array.

+ Colección Concreta (ConcreteAggregate): Implementa la interfaz de la colección y proporciona la implementación concreta de la creación de un objeto iterador.

+ Iterador Concreto (ConcreteIterator): Implementa la interfaz del iterador y realiza el seguimiento de la posición actual dentro de la colección. Proporciona implementaciones específicas para los métodos next() y hasNext().

El uso del patrón Iterator permite que el código cliente recorra una colección de elementos sin preocuparse por cómo se almacenan o gestionan internamente esos elementos. Esto hace que el código sea más independiente de la estructura de datos subyacente y más fácil de mantener, ya que los cambios en la estructura de la colección no afectarán al código que utiliza el iterador.

Aquí hay un ejemplo simple de cómo se podría implementar el patrón Iterator en Java:
``` java
import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;

// Paso 1: Definir la interfaz Iterator
interface MiIterador<T> {
    boolean hasNext();
    T next();
}

// Paso 2: Definir la interfaz Colección
interface Coleccion<T> {
    MiIterador<T> crearIterador();
}

// Paso 3: Implementar las clases concretas
class MiLista<T> implements Coleccion<T> {
    private List<T> elementos = new ArrayList<>();

    public void agregarElemento(T elemento) {
        elementos.add(elemento);
    }

    public MiIterador<T> crearIterador() {
        return new ListaIterador();
    }

    private class ListaIterador implements MiIterador<T> {
        private int indice = 0;

        public boolean hasNext() {
            return indice < elementos.size();
        }

        public T next() {
            if (hasNext()) {
                return elementos.get(indice++);
            }
            throw new UnsupportedOperationException("No hay más elementos.");
        }
    }
}

public class EjemploIterator {
    public static void main(String[] args) {
        MiLista<String> miLista = new MiLista<>();
        miLista.agregarElemento("Uno");
        miLista.agregarElemento("Dos");
        miLista.agregarElemento("Tres");

        MiIterador<String> iterador = miLista.crearIterador();
        while (iterador.hasNext()) {
            System.out.println(iterador.next());
        }
    }
}
```
En este ejemplo, hemos creado una clase MiLista que implementa la interfaz Coleccion y proporciona un iterador interno ListaIterador. El código cliente puede recorrer los elementos de la lista utilizando este iterador sin necesidad de conocer la estructura interna de la lista. Esto ejemplifica cómo el patrón Iterator facilita el acceso a los elementos de una colección de manera uniforme.