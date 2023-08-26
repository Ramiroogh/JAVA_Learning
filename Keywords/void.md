# Keyword Void

La palabra clave void en Java se utiliza para indicar que un método no devuelve ningún valor. Cuando un método está declarado con el tipo de retorno void, significa que el método realiza ciertas acciones o tareas, pero no produce un resultado que pueda ser utilizado más tarde en el programa. En otras palabras, un método con retorno void no devuelve ningún valor que pueda ser asignado a una variable o utilizado en una expresión.

Aquí tienes un ejemplo de un método con tipo de retorno void:
``` java
public class VoidExample {
    public static void printMessage() {
        System.out.println("¡Hola desde el método printMessage!");
    }

    public static void main(String[] args) {
        printMessage(); // Llamada al método printMessage
    }
}
```
En este ejemplo, el método printMessage está declarado con el tipo de retorno void. Dentro del método, solo hay una instrucción que imprime un mensaje en la consola. No hay un valor que se devuelva utilizando la palabra clave return.

Cuando se llama al método printMessage desde el método main, simplemente se ejecuta la acción definida en el método (imprimir un mensaje). No hay un valor que se devuelva a la línea de llamada del código.

+ La palabra clave void es útil cuando se desea que un método realice una tarea o una acción específica sin tener que preocuparse por el valor que retorna. Algunos ejemplos comunes de métodos con tipo de retorno void incluyen métodos que realizan operaciones de impresión, actualizaciones en la interfaz de usuario, cálculos internos, etc. En lugar de devolver un valor, estos métodos simplemente hacen su tarea y terminan su ejecución.

### Ejemplo con void y no void
aquí tienes un ejemplo de cómo podrías crear una clase que tenga un método void y otro método que no use void pero que almacene el valor del método que tiene void:
``` java
public class ValueMemorizer {
    private int memorizedValue;  // Variable para almacenar el valor memorizado

    // Método void que realiza una acción y no retorna valor
    public void performAction() {
        // Supongamos que realizamos algún cálculo aquí
        int result = 42;  // Valor ficticio
        memorizedValue = result;  // Almacenar el valor en la variable
        System.out.println("Acción realizada");
    }

    // Método que obtiene el valor memorizado
    public int getMemorizedValue() {
        return memorizedValue;
    }

    public static void main(String[] args) {
        ValueMemorizer memorizer = new ValueMemorizer();

        // Llamar al método void para realizar la acción y almacenar el valor
        memorizer.performAction();

        // Obtener y mostrar el valor memorizado
        int value = memorizer.getMemorizedValue();
        System.out.println("Valor memorizado: " + value);
    }
}
```
En este ejemplo, la clase ValueMemorizer tiene dos métodos. El método performAction es un método void que realiza alguna acción (en este caso, asigna un valor ficticio de 42 a la variable memorizedValue), y el método getMemorizedValue devuelve el valor almacenado en memorizedValue.

En el método main, creamos una instancia de ValueMemorizer, llamamos al método performAction para realizar la acción y almacenar el valor, y luego llamamos al método getMemorizedValue para obtener y mostrar el valor memorizado.

Es importante tener en cuenta que este ejemplo es simplificado y no refleja un uso realista de la memorización de valores. En una situación real, el método que almacena el valor podría ser más complejo, y la memorización podría requerir consideraciones adicionales, como la sincronización en entornos concurrentes.