# Lambda Expression ->

Una expresión lambda en Java es una forma concisa de representar una función anónima, es decir, una función sin un nombre explícito. Las expresiones lambda introducidas en Java 8 permiten escribir código más limpio y más legible al eliminar la necesidad de crear clases internas o implementaciones de interfaces funcionales para definir comportamientos cortos y específicos.

Las expresiones lambda se basan en interfaces funcionales, que son interfaces que tienen un único método abstracto. Las expresiones lambda se pueden usar para proporcionar una implementación para ese único método abstracto de la interfaz funcional. Esto hace que el código sea más compacto y más fácil de entender.

### return y llaves {}
Si el codigo que contiene una lambda expression, y abre llaves, es necesario declarar un return.
``` java
lista.sort((Cuenta o1, Cuenta o2)-> {
    return Integer.compare(o1.getNumero(), o2.getNumero());
});
```
+ Esto porque con las llaves, esta dentro de un contexto de las llaves.
<br>
Ahora veamos como queda si quitamos las llaves de contexto:

``` java
lista.sort((Cuenta o1, Cuenta o2) -> 
    Integer.compare(o1.getNumero(), o2.getNumero())
);
```
+ Se retorna Implicitamente.

### Ejemplo
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

### Ejemplo 2
¿Y si fuera lambda?
Consulte el código heredado escrito a continuación con una versión de Java anterior a 1.8. Tenga en cuenta que este código todavía usa aún una clase anónima en el método sort:

``` java
List<String> nombres = new ArrayList<>();
nombres.add("Super Mario");
nombres.add("Yoshi"); 
nombres.add("Donkey Kong"); 

Collections.sort(nombres, new Comparator<String>() {

    @Override
    public int compare(String s1, String s2) {
        return s1.length() - s2.length();
    }
});

System.out.println(nombres);
```
+ ¿Cómo sería la implementación de la llamada al método sort con lambda? Verifique las implementaciones correctas:

1.
``` java
nombres.sort((s1, s2) ->  {return s1.length() - s2.length();} );
```
También puede utilizar el método sort de la lista. También tenga en cuenta que el return es opcional (siempre que también saquemos el {}):
``` java
nombres.sort((s1, s2) ->  s1.length() - s2.length());
```
2.

``` java
Collections.sort(nombres, (s1, s2) ->  s1.length() - s2.length());
```
¡Fíjate que no es necesaria ningún return! Mucho más sencillo y conciso.

### Ejemplo 3
Foreach con lambda
Vea el código usando un for "tradicional" para:
``` java
List<String> nombres = new ArrayList<>();
nombres.add("Super Mario");
nombres.add("Yoshi"); 
nombres.add("Donkey Kong"); 

for(int i = 0; i < nombres.size(); i++) {
    System.out.println(nombres.get(i));
}
```
Te gustaron las lambdas y te gustaría usarlas en el momento del bucle. ¿Qué alternativa usa correctamente la expresión lambda para iterar los elementos de la lista?
``` java
nombres.forEach((nombre) -> System.out.println(nombre));
```
Correcto. El lenguaje ha evolucionado mucho como muestra este ejercicio. En las primeras versiones, era muy burocrático recorrer las listas.
+ Con lambdas, el bucle (for) se ha convertido en una simple llamada a un método. ¡Muy bueno!