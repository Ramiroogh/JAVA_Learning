# Orden Natural
el término "orden natural" se refiere al ordenamiento predeterminado de objetos basado en su implementación de la interfaz Comparable. Cada clase que implementa la interfaz Comparable define cómo se comparan sus instancias y, por lo tanto, cómo deben ser ordenadas naturalmente.

La interfaz Comparable tiene un único método llamado compareTo, que se utiliza para comparar dos objetos. El método compareTo devuelve un número negativo si el objeto actual es menor que el objeto con el que se compara, cero si son iguales y un número positivo si el objeto actual es mayor.

``` java
Collections.sort(lista); // No sabe como ordenar, el parametro lo acepta, pero no compila el metodo sort
Collections.sort(lista, new OrdenadorPorNombreTitular()); // Si Compila
```
+ Orden natural es el atributo por defecto por el que vas a ordenar un arreglo o una lista.
El ejemplo anterior es una forma antigua de ordenar, ahora se puede usar la interfaz Comparable, apartir de java 8 en adelante.