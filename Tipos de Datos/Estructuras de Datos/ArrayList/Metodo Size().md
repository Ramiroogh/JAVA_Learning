# Size ()
El método size() en un ArrayList de Java devuelve el número de elementos presentes en la lista. Es un método que pertenece a la clase ArrayList y se utiliza para obtener la cantidad de elementos almacenados en la lista en un momento dado.

+ No cuenta los espacios vacios

Es importante tener en cuenta que el método size() devuelve un entero que representa el número de elementos en la lista en ese momento. Si se agregan o eliminan elementos de la lista, el valor devuelto por size() se actualizará en consecuencia.
``` java
ArrayList<String> miLista = new ArrayList<>();
miLista.add("Elemento 1");
miLista.add("Elemento 2");
miLista.add("Elemento 3");

int tamaño = miLista.size();
System.out.println("El tamaño de la lista es: " + tamaño);
```
## Diferencia con Length y Size()
El método length es utilizado en arrays de Java para obtener el tamaño fijo del array, es decir, el número de elementos que puede contener. Por otro lado, el método size() es utilizado en las colecciones de tipo List, como ArrayList, para obtener el número de elementos actualmente presentes en la lista.

array.length devuelve el tamaño fijo del array, que es igual a 5. Mientras tanto, lista.size() devuelve el número actual de elementos en la lista, que puede variar en función de las operaciones de agregado o eliminación de elementos realizadas en la lista.