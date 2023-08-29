# Linked List - Lista anexada
La LinkedList (lista enlazada) es otra estructura de datos en Java que se utiliza para almacenar y manipular elementos de forma secuencial. A diferencia de ArrayList, LinkedList no utiliza un arreglo subyacente para almacenar los elementos, sino que **utiliza nodos enlazados**.

Linkedlist es un conjunto de objetos, es una lista pero NO ES UN ARRAY.

+ Cada nodo en una LinkedList contiene dos partes: el elemento actual y una referencia al siguiente nodo. Esto permite que los elementos estén dispersos en la memoria, en lugar de estar almacenados en ubicaciones contiguas como en el caso de ArrayList.

+ La ventaja de LinkedList sobre ArrayList es que la inserción y eliminación de elementos en el medio de la lista se pueden realizar de manera más eficiente. Esto se debe a que solo se necesitan ajustar las referencias de los nodos vecinos, en lugar de tener que mover todos los elementos contiguos como sucede con ArrayList.

Sin embargo, el acceso a un elemento en una posición específica en LinkedList puede ser más lento, ya que se requiere recorrer la lista desde el principio hasta la posición deseada.

Aquí tienes un ejemplo de cómo usar LinkedList en Java:
``` java
import java.util.LinkedList;

public class Main {
    public static void main(String[] args) {
        LinkedList<String> listaEnlazada = new LinkedList<>();

        // Agregar elementos al final de la lista
        listaEnlazada.add("Elemento 1");
        listaEnlazada.add("Elemento 2");
        listaEnlazada.add("Elemento 3");

        // Agregar elemento al inicio de la lista
        listaEnlazada.addFirst("Elemento 0");

        // Agregar elemento en una posición específica
        listaEnlazada.add(2, "Elemento 1.5");

        // Eliminar elemento de la lista
        listaEnlazada.remove("Elemento 2");

        // Recorrer la lista
        for (String elemento : listaEnlazada) {
            System.out.println(elemento);
        }
    }
}
```
En este ejemplo, se crea una LinkedList llamada listaEnlazada y se agregan varios elementos a la lista. Luego se agrega un elemento al inicio de la lista, se agrega un elemento en una posición específica y se elimina un elemento de la lista. Finalmente, se recorre la lista e imprime cada elemento.

En resumen, LinkedList es una estructura de datos enlazada que puede ser una alternativa a ArrayList en términos de rendimiento para ciertas operaciones, como la inserción y eliminación de elementos en el medio de la lista. Sin embargo, el acceso a elementos en posiciones específicas puede ser más lento. Es importante evaluar tus necesidades y los requisitos de rendimiento antes de decidir qué estructura de datos utilizar. Si tienes alguna otra pregunta, no dudes en hacerla.

+ LinkedList y ArrayList son dos implementaciones diferentes de la interfaz List. LinkedList es una lista doblemente "enlazada" y ArrayList representa un array con redimensión de tamaño dinámico.