# for Loop Tradicional
El bucle for es una estructura de control que permite ejecutar un bloque de código repetidamente mientras se cumple una condición. Tiene una sintaxis específica que consta de tres partes: inicialización, condición y expresión de actualización.
+ Aquí tienes un ejemplo simple para ilustrar el funcionamiento del bucle for:
``` java
public class ForLoopExample {
    public static void main(String[] args) {
        // Imprimir los números del 1 al 5 usando un bucle for
        for (int i = 1; i <= 5; i++) {
            System.out.println(i);
        }
    }
}
```
Recuerda que es fundamental asegurarte de que la condición se vuelva false en algún momento para evitar bucles infinitos. El bucle for tradicional es útil cuando necesitas un control preciso sobre el número de iteraciones y cuándo deben ocurrir.