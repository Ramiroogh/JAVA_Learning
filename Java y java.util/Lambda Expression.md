# Lambda Expression

Una expresión lambda en Java es una forma concisa de representar una función anónima, es decir, una función sin un nombre explícito. Las expresiones lambda introducidas en Java 8 permiten escribir código más limpio y más legible al eliminar la necesidad de crear clases internas o implementaciones de interfaces funcionales para definir comportamientos cortos y específicos.

Las expresiones lambda se basan en interfaces funcionales, que son interfaces que tienen un único método abstracto. Las expresiones lambda se pueden usar para proporcionar una implementación para ese único método abstracto de la interfaz funcional. Esto hace que el código sea más compacto y más fácil de entender.

Aquí hay un ejemplo de cómo se ve una expresión lambda en Java, junto con su uso en un contexto práctico:
``` java
import java.util.ArrayList;
import java.util.List;

public class LambdaExample {
    public static void main(String[] args) {
        List<String> names = new ArrayList<>();
        names.add("Juan");
        names.add("María");
        names.add("Carlos");
        names.add("Ana");

        // Utilizando una expresión lambda para ordenar la lista de nombres alfabéticamente
        names.sort((name1, name2) -> name1.compareTo(name2));

        // Imprimir la lista de nombres ordenada
        names.forEach(name -> System.out.println(name));
    }
}
```
En este ejemplo, estamos utilizando una expresión lambda para ordenar una lista de nombres alfabéticamente. La interfaz funcional involucrada aquí es Comparator, que tiene el método abstracto compare. La expresión lambda (name1, name2) -> name1.compareTo(name2) se ajusta a la firma del método compare, por lo que podemos usarla para proporcionar una implementación concisa de la comparación.

El método sort de la lista acepta un comparador, y en lugar de crear una clase anónima que implemente la interfaz Comparator, simplemente proporcionamos la expresión lambda como una forma más compacta y legible de definir la lógica de comparación.

Luego, utilizamos otra expresión lambda en el método forEach para imprimir cada nombre en la lista.

Las expresiones lambda en Java facilitan la escritura de código más claro y conciso, especialmente en situaciones donde solo se necesita una implementación simple y corta de una interfaz funcional.