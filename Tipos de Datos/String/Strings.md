Las clases de String son inmutables, para volverlos mutables se deben recurrir a metodos como string builder.

Esta clase tiene muchos metodos como toUpperCase, toLowerCase, etc.

String nombre = "Alura";

nombre = nombre.toUpperCase();

StringBuilder es una clase común. Observe que usamos new para crear el objeto. Además, como el objeto es mutable, usamos la misma referencia, sin nuevas asignaciones.

La interfaz CharSequence
Ahora lo bueno es que la clase StringBuilder también implementa la interfaz CharSequence:
public class StringBuilder implements CharSequence {
CharSequence cs = new StringBuilder("También es una secuencia de caracteres");

Esto significa que algunos métodos de la clase String saben cómo trabajar con StringBuilder, por ejemplo:
String nombre = "ALURA";
CharSequence cs = new StringBuilder("al");

nombre = nombre.replace("AL", cs);

System.out.println(nombre);

Viceversa, la clase StringBuilder tiene métodos que reciben el tipo CharSequence. De esa forma podemos trabajar de forma compatible con ambas clases, basándonos en una interfaz común.