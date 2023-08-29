# Contains()
El método contains() en un ArrayList de Java se utiliza para verificar si un elemento específico está presente en la lista. Este método devuelve un valor booleano: true si el elemento está presente en la lista y false si no lo está.

Aquí tienes un ejemplo para ilustrar cómo se utiliza el método contains():
``` java
ArrayList<String> miLista = new ArrayList<>();
miLista.add("Elemento 1");
miLista.add("Elemento 2");
miLista.add("Elemento 3");

boolean contieneElemento1 = miLista.contains("Elemento 1");
System.out.println("¿La lista contiene Elemento 1? " + contieneElemento1);

boolean contieneElemento4 = miLista.contains("Elemento 4");
System.out.println("¿La lista contiene Elemento 4? " + contieneElemento4);
```
+ En este caso, el método contains("Elemento 1") devuelve true porque el elemento "Elemento 1" está presente en la lista miLista.
+ Por otro lado, el método contains("Elemento 4") devuelve false porque el elemento "Elemento 4" no está presente en la lista.

Es importante tener en cuenta que el método contains() utiliza el método equals() para determinar la igualdad de los elementos. Por lo tanto, si estás utilizando objetos personalizados en lugar de tipos primitivos, asegúrate de sobrescribir el método equals() correctamente para obtener resultados precisos al utilizar contains().