# Array
En Java, un array es una estructura de datos que permite almacenar un conjunto de elementos del mismo tipo. Los arrays son útiles cuando necesitas manejar múltiples valores del mismo tipo y quieres acceder a ellos de manera eficiente utilizando índices.

Los arrays en Java tienen las siguientes características:

+ Tamaño Fijo: Una vez que se crea un array con un tamaño específico, ese tamaño no puede cambiar. Si necesitas un tamaño variable, podrías considerar usar una colección como ArrayList.

+ Tipo Homogéneo: Todos los elementos en un array deben ser del mismo tipo. Por ejemplo, un array de enteros solo puede contener valores enteros.

+ Índices Basados en Cero: Los índices de los elementos en un array comienzan en cero. El primer elemento tiene índice 0, el segundo tiene índice 1 y así sucesivamente.

Aquí tienes un ejemplo básico de cómo se declara y utiliza un array en Java:
``` java
public class ArrayExample {
    public static void main(String[] args) {
        // Declaración y creación de un array de enteros
        int[] numbers = new int[5];

        // Asignación de valores a los elementos del array,
        // apuntando a los indices
        numbers[0] = 10;
        numbers[1] = 20;
        numbers[2] = 30;
        numbers[3] = 40;
        numbers[4] = 50;

        // Acceso e impresión de los valores del array
        System.out.println("Elemento en el índice 0: " + numbers[0]);
        System.out.println("Elemento en el índice 3: " + numbers[3]);
    }
}
```
En este ejemplo, estamos creando un array de enteros llamado numbers con un tamaño de 5. Luego, asignamos valores a cada uno de los elementos del array utilizando los índices (0 al 4). Finalmente, accedemos a algunos elementos del array utilizando índices y los imprimimos en la consola.
#### Importante
Al array, hay que asignarle el tamaño que va a tener.

+ Es importante recordar que debes asegurarte de no acceder a un índice fuera del rango del array, ya que esto causaría una excepción en tiempo de ejecución (por ejemplo, ArrayIndexOutOfBoundsException).

### Otras Estructuras
Además de los arrays, Java ofrece una variedad de estructuras de datos más complejas y versátiles que se encuentran en el paquete java.util. Estas estructuras de datos proporcionan funcionalidades específicas y flexibilidad para abordar diferentes escenarios de programación. Algunas de las estructuras de datos más comunes en Java son:

ArrayList: Una implementación de la interfaz List que utiliza un arreglo dinámico para almacenar elementos. Proporciona un tamaño flexible y métodos para agregar, eliminar y acceder a elementos en la lista.

LinkedList: Una implementación de List basada en una lista doblemente enlazada. Es útil para inserciones y eliminaciones frecuentes, pero puede ser menos eficiente para acceso aleatorio.

HashSet: Una implementación de la interfaz Set que utiliza una tabla hash para almacenar elementos únicos. No garantiza un orden específico de los elementos.

TreeSet: Otra implementación de Set, pero esta mantiene los elementos en orden natural (ordenados).

HashMap: Una implementación de la interfaz Map que utiliza una tabla hash para almacenar pares clave-valor. Proporciona un acceso rápido a los valores utilizando las claves.

TreeMap: Similar a HashMap, pero mantiene los pares clave-valor en orden natural (ordenados por las claves).

Queue: Una interfaz que define un comportamiento de cola. LinkedList y PriorityQueue son implementaciones comunes.

Deque: Una interfaz que define una cola doble. ArrayDeque es una implementación eficiente.

Stack: Una clase que implementa una pila (LIFO). Sin embargo, se recomienda usar Deque en su lugar debido a su flexibilidad.

PriorityQueue: Una cola de prioridad basada en un montículo. Los elementos se almacenan en orden basado en su prioridad.

Estas son solo algunas de las estructuras de datos disponibles en Java. Cada estructura de datos tiene ventajas y desventajas según el escenario de uso. Al elegir una estructura de datos, es importante considerar las operaciones que realizarás con mayor frecuencia (inserciones, eliminaciones, búsquedas, etc.) y cómo se adaptan a esas necesidades.