# Autoboxing
El autoboxing es un mecanismo en Java que permite la *conversión automática entre tipos primitivos y sus respectivas clases envoltorias (wrapper classes) equivalentes*. Las clases envoltorias son clases que representan los tipos primitivos como objetos. Estas clases son parte del paquete java.lang y están diseñadas para permitir el uso de tipos primitivos en contextos donde se requieren objetos, como colecciones o genéricos.

Las clases envoltorias más comunes son:

+ Integer para int
+ Double para double
+ Boolean para boolean
+ Character para char

El autoboxing se realiza **automáticamente por el compilador** cuando se necesita una conversión entre un tipo primitivo y su clase envoltoria correspondiente, y viceversa. Esto simplifica el código y hace que sea más intuitivo trabajar con tipos primitivos en situaciones donde se requieren objetos. Aquí tienes un ejemplo de autoboxing:
``` java
public class AutoboxingExample {
    public static void main(String[] args) {
        int primitiveInt = 42;
        Integer boxedInt = primitiveInt; // Autoboxing

        double primitiveDouble = 3.14;
        Double boxedDouble = primitiveDouble; // Autoboxing

        System.out.println("Boxed Integer: " + boxedInt);
        System.out.println("Boxed Double: " + boxedDouble);
    }
}
```
En este ejemplo, se realiza autoboxing cuando asignamos valores de tipos primitivos (int y double) a las respectivas clases envoltorias (Integer y Double). La conversión se realiza automáticamente y simplifica la sintaxis.

Es importante tener en cuenta que, aunque el autoboxing es conveniente, puede tener un impacto en el rendimiento debido a la creación y gestión de objetos adicionales. En situaciones donde el rendimiento es crítico, es importante evaluar si el autoboxing es la mejor opción.

# Integer Deprecated
es importante estar al tanto de las actualizaciones en las bibliotecas y clases de Java. La clase Integer en efecto ha sido marcada como obsoleta (deprecated) en favor de métodos estáticos proporcionados por la clase Integer, como valueOf.

+ La razón detrás de esta recomendación es promover el uso de métodos estáticos que *ofrecen mejor rendimiento y optimización*, en comparación con el **antiguo enfoque de autoboxing**. El método valueOf permite obtener instancias reutilizadas de objetos Integer para ciertos valores dentro de un rango específico. Esto reduce la cantidad de objetos creados y ayuda a mejorar la eficiencia en memoria y rendimiento.
``` java
public class ValueOfExample {
    public static void main(String[] args) {
        int primitiveInt = 42;

        // Utilizando valueOf para obtener una instancia reutilizada de Integer
        Integer boxedInt1 = Integer.valueOf(primitiveInt);
        Integer boxedInt2 = Integer.valueOf(42); // También puedes pasar el valor directamente

        System.out.println("Boxed Integer 1: " + boxedInt1);
        System.out.println("Boxed Integer 2: " + boxedInt2);

        // Comprobando si las instancias son las mismas
        System.out.println("Misma instancia: " + (boxedInt1 == boxedInt2)); // Debería imprimir "true"
    }
}
```
En este ejemplo, valueOf se utiliza para obtener instancias de Integer reutilizadas para el valor 42. Puedes observar que las dos instancias de boxedInt1 y boxedInt2 son iguales, lo que demuestra que se trata de la misma instancia reutilizada.

En resumen, la recomendación de utilizar valueOf en lugar de autoboxing para las clases envoltorias, como Integer, se basa en la optimización de rendimiento y la gestión más eficiente de objetos. Al usar valueOf, puedes obtener beneficios en términos de uso de memoria y velocidad de ejecución.

# Unboxing
Tambien es bueno saber lo que pasa trasbambalinas cuando guardamos una referencia en una variable que acepta valores primitivos, de por si esto esta mal, pero Java lo compila igual, aqui se muestra que es lo que pasa:
``` java
int valorPrimitivo = numeroObjeto; // Esto compila, pero es una mala práctica.
int valorPrimitivo = numeroObjeto.intValue(); // Esto ocurre detras del Unboxing.
// MAS EJEMPLOS
byte byteInteger: numeroObjeto.byteValue();
double doubleInteger = numeroObjeto.doubleValue();
float floatIOnteger = numeroObjeto.floatValue();
```