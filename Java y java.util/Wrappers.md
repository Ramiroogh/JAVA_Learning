# Wrappers

Los "wrappers" en el contexto de java.util se refieren a las **clases que envuelven tipos de datos primitivos en objetos de clase para permitir que estos tipos de datos se utilicen en contextos donde solo se permiten objetos**. Estas clases se encuentran en el paquete java.util y son parte esencial de la biblioteca estándar de Java para trabajar con tipos de datos primitivos de manera más flexible.

+ Los tipos de datos primitivos en Java (como int, char, boolean, etc.) son valores simples y no son objetos. Sin embargo, hay situaciones en las que es necesario tratar estos tipos de datos primitivos como objetos, por ejemplo, al trabajar con colecciones, al usar algunas API específicas que requieren objetos o al aprovechar características de orientación a objetos.

A continuación se presentan los wrappers más comunes que se encuentran en java.util para los tipos de datos primitivos:

+ Integer: Envuelve el tipo de dato primitivo int. Proporciona métodos para convertir entre representaciones de cadena y enteros, así como para realizar operaciones aritméticas.

+ Double: Envuelve el tipo de dato primitivo double. Al igual que Integer, proporciona métodos para conversiones y operaciones matemáticas.

+ Boolean: Envuelve el tipo de dato primitivo boolean. Permite convertir entre representaciones de cadena y valores booleanos.

+ Character: Envuelve el tipo de dato primitivo char. Facilita la conversión entre caracteres y su representación numérica.

+ Byte, Short, Long, Float: Envuelven los tipos de datos primitivos correspondientes. Ofrecen funcionalidades similares a Integer y Double.

Estos wrappers son útiles en situaciones en las que necesitas utilizar tipos primitivos en contextos que requieren objetos, como al trabajar con colecciones genéricas (List<Integer>, por ejemplo), al utilizar mapas (Map<String, Double>, por ejemplo), o cuando necesitas pasar tipos primitivos a través de interfaces y métodos que solo aceptan objetos.

En Java 5 y versiones posteriores, la autoboxing y unboxing permiten una conversión automática entre tipos primitivos y sus wrappers correspondientes, lo que simplifica el código y hace que la interacción entre tipos primitivos y sus wrappers sea más transparente.

# Ejemplo - integer
Ejemplo de cómo usar los wrappers en Java. Supongamos que tienes una lista de números enteros y deseas calcular la suma de sus valores utilizando la clase Integer como wrapper para los números enteros primitivos.
``` java
import java.util.ArrayList;
import java.util.List;

public class WrapperExample {
    public static void main(String[] args) {
        // Crear una lista de números enteros utilizando Integer como wrapper
        List<Integer> integerList = new ArrayList<>();
        integerList.add(10);
        integerList.add(20);
        integerList.add(30);

        // Calcular la suma de los números en la lista
        int sum = 0;
        for (Integer num : integerList) {
            sum += num; // La autounboxing convierte automáticamente Integer a int
        }

        System.out.println("La suma de los números es: " + sum);
    }
}
```
En este ejemplo, estamos utilizando la clase Integer como wrapper para los números enteros primitivos. Creamos una lista de números enteros utilizando List<Integer>, y luego agregamos algunos valores a la lista. Luego, iteramos a través de la lista y, debido a la autounboxing introducida en Java 5 y posteriores, podemos tratar los objetos Integer como si fueran valores enteros primitivos al sumarlos en la variable sum.

La autounboxing convierte automáticamente un objeto Integer en un valor int cuando se necesita en un contexto que espera un tipo primitivo. De manera similar, la autoboxing convierte un valor primitivo en un objeto Integer cuando se necesita en un contexto que espera un objeto.

En resumen, los wrappers como Integer permiten trabajar con tipos de datos primitivos en situaciones donde se requieren objetos, como en el contexto de colecciones genéricas.