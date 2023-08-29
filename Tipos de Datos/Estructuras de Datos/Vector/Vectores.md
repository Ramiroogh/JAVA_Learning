# Vectores - Estructura de Datos
Un vector en programación es una estructura de datos que permite almacenar y acceder a elementos de forma secuencial. En Java, un vector se implementa utilizando la clase "Vector" o la interfaz "List".

+ Vector implementa la interfaz List.
+ Un vector también usa un array, por debajo similar a un ArrayList.
+ Un vector puede contener elementos de cualquier tipo, como enteros, cadenas de texto, objetos personalizados, etc. Los elementos se almacenan en posiciones consecutivas y se accede a ellos utilizando un índice numérico.

Aquí tienes un ejemplo de cómo utilizar un vector en Java:
``` java
import java.util.Vector;

public class Main {
    public static void main(String[] args) {
        Vector<String> vector = new Vector<>();

        // Agregar elementos al vector
        vector.add("Elemento 1");
        vector.add("Elemento 2");
        vector.add("Elemento 3");

        // Acceder a un elemento en una posición específica
        String elemento = vector.get(1);
        System.out.println("Elemento en la posición 1: " + elemento);

        // Modificar un elemento en una posición específica
        vector.set(0, "Nuevo elemento");

        // Eliminar un elemento del vector
        vector.remove(2);

        // Recorrer el vector
        for (String elemento : vector) {
            System.out.println(elemento);
        }
    }
}
```
+ En este ejemplo, se crea un vector llamado "vector" que almacena elementos de tipo String. Se agregan varios elementos al vector, se accede y se modifica un elemento en una posición específica, se elimina un elemento del vector y finalmente se recorre el vector e imprime cada elemento.

Los vectores son útiles cuando se necesita acceder a elementos de forma rápida utilizando un índice. Sin embargo, si se requieren operaciones frecuentes de **inserción o eliminación en el medio de la estructura, puede ser más eficiente utilizar otras estructuras de datos como ArrayList o LinkedList**.

# Thread-safe
Thread-safe (seguro en hilos) es un término utilizado en programación para describir una operación o estructura de datos que puede ser utilizada de manera simultánea por múltiples hilos de ejecución sin generar resultados incorrectos o inconsistencias.

+ En el contexto de los vectores en Java, se asocia el término "thread-safe" debido a que la clase Vector de Java proporciona garantías de seguridad en entornos de concurrencia. Esto significa que los vectores se pueden utilizar de manera segura en hilos concurrentes sin preocuparse por problemas de sincronización.

Cuando varios hilos acceden a un vector sin tomar precauciones adicionales, pueden ocurrir problemas como condiciones de carrera, lecturas o escrituras inconsistentes y resultados impredecibles. Sin embargo, la clase Vector en Java implementa mecanismos internos para garantizar que las operaciones se realicen de manera segura en entornos de concurrencia.

La clase Vector logra esto sincronizando automáticamente todas las operaciones para evitar conflictos entre hilos. Esto significa que solo un hilo puede acceder al vector a la vez, evitando problemas de sincronización. Sin embargo, esta sincronización puede tener un impacto en el rendimiento, por lo que en situaciones donde no se requiere sincronización, se recomienda utilizar otras estructuras de datos como ArrayList.
