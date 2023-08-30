# Clases Envoltorias (Wrappers) - Paquete java.lang
En Java, los tipos primitivos (como int, double, char, boolean, etc.) son valores básicos que representan datos simples, como números enteros, números de punto flotante y caracteres. Estos tipos primitivos son eficientes en términos de uso de memoria y rendimiento, pero carecen de ciertas funcionalidades que se encuentran en los objetos, como métodos y compatibilidad con algunas estructuras de datos.

+ Para superar estas limitaciones y permitir que los tipos primitivos se utilicen en contextos donde se requieren objetos, se introdujeron las clases envoltorias o wrappers en Java. *Cada tipo primitivo tiene una clase envoltoria correspondiente en el paquete java.lang*:

int tiene Integer
double tiene Double
char tiene Character
boolean tiene Boolean
Y así sucesivamente...

---
Las clases envoltorias son clases que envuelven o encapsulan un valor primitivo en un objeto. Esto permite que los tipos primitivos se utilicen en operaciones que requieren objetos, como en colecciones (por ejemplo, listas, conjuntos, mapas) o cuando se usan genéricos.

+ La relación entre los tipos primitivos y las clases envoltorias se establece mediante el mecanismo de autoboxing y unboxing. El autoboxing es la conversión automática de un tipo primitivo a su respectiva clase envoltoria, mientras que el unboxing es la conversión automática de una clase envoltoria a su tipo primitivo correspondiente.

Por ejemplo, cuando realizas operaciones como agregar un valor int a una lista, Java automáticamente realiza el autoboxing para convertir el valor int en un objeto Integer. Del mismo modo, cuando recuperas un valor Integer de la lista, se realiza un unboxing para convertirlo de nuevo a un tipo primitivo int.

En resumen, las clases envoltorias (wrappers) en Java son clases que envuelven tipos primitivos en objetos, permitiendo su uso en contextos donde se requieren objetos, como colecciones y genéricos. La relación entre tipos primitivos y clases envoltorias se maneja mediante autoboxing y unboxing, lo que facilita la manipulación de ambos tipos de datos de manera transparente.

+ Para cada primitivo hay una clase llamada Wrapper.
+ Para almacenar un primitivo en una colección, necesita crear un objeto que envuelva el valor.
+ La creación del objeto Wrapper se llama autoboxing.
+ La extracción del valor primitivo del objeto Wrapper se llama unboxing.
+ El autoboxing y unboxing ocurren automáticamente.
+ Las clases wrapper tienen varios métodos auxiliares, por ejemplo para el parsing.
+ Todas las clases wrappers que representan un valor numérico tienen la clase java.lang.Number como madre.