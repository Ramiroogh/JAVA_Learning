Quiere ayudar a Pedro, que está trabajando con Java pero nunca aprendió los genéricos. Él te mostró el siguiente código:
``` java
List referencias = new ArrayList(); //AQUÍ
referencias.add(Double.valueOf(30.9));
referencias.add(Integer.valueOf(10));
referencias.add(Float.valueOf(13.4f));COPIA EL CÓDIGO
```
¿Con qué código puedes reemplazar la línea con el comentario //AQUÍ para usar generics?
``` java
List<Object> referencias = new ArrayList<>();
```
+ Correcto, todas las referencias también son Objetos.
``` java
List<Number> referencias = new ArrayList<>();
```
+ Correcto, todos los elementos de esa lista son números.