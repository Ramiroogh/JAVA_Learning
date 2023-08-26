# Sobrecarga de Métodos

La sobrecarga de métodos es un concepto en programación orientada a objetos que te permite definir múltiples métodos en una misma clase con el mismo nombre pero diferentes parámetros. Esto permite que un método tenga diferentes versiones según los tipos o cantidad de argumentos que se le pasen. Java es un lenguaje que permite implementar sobrecarga de métodos.

Aquí tienes un ejemplo sencillo para ilustrar la sobrecarga de métodos en Java:

``` java
public class Calculadora {

    public int sumar(int a, int b) {
        return a + b;
    }

    public double sumar(double a, double b) {
        return a + b;
    }

    public int sumar(int a, int b, int c) {
        return a + b + c;
    }

    public static void main(String[] args) {
        Calculadora calculadora = new Calculadora();

        System.out.println("Suma de enteros: " + calculadora.sumar(5, 3));
        System.out.println("Suma de decimales: " + calculadora.sumar(5.5, 3.7));
        System.out.println("Suma de tres enteros: " + calculadora.sumar(2, 4, 6));
    }
}
```
En este ejemplo, la clase Calculadora tiene tres métodos llamados sumar, pero cada uno tiene una lista diferente de parámetros. La sobrecarga de métodos permite que el compilador determine cuál versión del método debe invocar en función de los tipos y la cantidad de argumentos proporcionados.

+ Cuando se llama al método sumar con dos enteros, se invoca la versión del método que toma dos enteros como parámetros. Cuando se llama con dos números de punto flotante (decimales), se invoca la versión del método que toma dos doubles. Y cuando se llama con tres enteros, se invoca la versión del método con tres enteros como parámetros.

La sobrecarga de métodos es útil para proporcionar interfaces más intuitivas y flexibles a los usuarios de una clase, ya que pueden llamar al mismo método con diferentes tipos de datos según sea necesario.