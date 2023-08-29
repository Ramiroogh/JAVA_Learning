# superclase Collections
en Java es una clase de utilidad que proporciona métodos estáticos para trabajar con colecciones, como listas, conjuntos y mapas. Esta clase se encuentra en el paquete java.util.

+ La interfaz java.util.Collection que es la interfaz de todas las colecciones.
+ Las listas son secuencias que aceptan elementos duplicados.
+ Los conjuntos (java.util.Set) también son colecciones, pero no aceptan duplicados ni listas.

Collections proporciona una serie de métodos útiles para realizar operaciones comunes en colecciones, como ordenar, buscar, filtrar y transformar elementos. Al ser una clase de utilidad, no se puede crear una instancia de Collections, ya que todos sus métodos son estáticos y se pueden invocar directamente en la clase.

Algunos de los métodos más comunes proporcionados por Collections incluyen:

+ sort(): se utiliza para ordenar una lista en orden ascendente. Puede aceptar una lista de cualquier tipo que implemente la interfaz Comparable, o puede proporcionar un comparador personalizado.
+ binarySearch(): se utiliza para buscar un elemento en una lista ordenada utilizando el algoritmo de búsqueda binaria. La lista debe estar ordenada previamente.
+ reverse(): se utiliza para invertir el orden de los elementos en una lista.
+ shuffle(): se utiliza para mezclar aleatoriamente los elementos en una lista.
+ max(): se utiliza para encontrar el elemento máximo en una colección.
+ min(): se utiliza para encontrar el elemento mínimo en una colección.
unmodifiableList(), unmodifiableSet(), unmodifiableMap(): se utilizan para crear versiones inmutables de una lista, conjunto o mapa, respectivamente.

## Ejemplo
Aquí tienes un ejemplo sencillo en Java que utiliza la clase Collections y el método sort() para ordenar una lista de números enteros:
``` java
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;

public class EjemploCollections {
    public static void main(String[] args) {
        // Crear una lista de números enteros desordenados
        List<Integer> numeros = new ArrayList<>();
        numeros.add(5);
        numeros.add(2);
        numeros.add(8);
        numeros.add(1);
        numeros.add(4);

        // Ordenar la lista de números utilizando el método sort() de Collections
        Collections.sort(numeros);

        // Imprimir la lista ordenada
        System.out.println("Lista ordenada: " + numeros);
    }
}
```
En este ejemplo, creamos una lista de números enteros desordenados utilizando la clase ArrayList. Luego, utilizamos el método sort() de la clase Collections para ordenar la lista en orden ascendente. Finalmente, imprimimos la lista ordenada.

El resultado de este código será:
``` java
Lista ordenada: [1, 2, 4, 5, 8]
```
Este es solo un ejemplo básico para ilustrar el uso del método sort() de Collections. La clase Collections proporciona muchos otros métodos útiles para trabajar con colecciones en Java.
