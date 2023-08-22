# Modificador de Acceso

Un modificador de acceso en Java es una palabra clave que se utiliza para controlar la visibilidad y el alcance de las clases, métodos, variables y otros elementos en un programa. Estos modificadores definen quién puede acceder a un elemento particular y desde dónde.

Existen cuatro tipos principales de modificadores de acceso en Java:

+ Public: Cuando un miembro se declara como público, es accesible desde cualquier parte del código, incluso desde otras clases y paquetes.
``` java
public class MiClase {
    public int miVariablePublica = 10;

    public void miMetodoPublico() {
        // Código del método
    }
}
```
+ Protected: Los miembros protegidos son accesibles desde la misma clase, las clases del mismo paquete y las subclases (incluso si están en paquetes diferentes).
Protected me da visibilidad a nivel de paquete y a nivel de Herencia.
``` java
class MiClase {
    protected int miVariableProtegida = 20;

    protected void miMetodoProtegido() {
        // Código del método
    }
}
```
+ Default (o Package-private): Si no se especifica ningún modificador de acceso, el miembro tiene acceso "por defecto" dentro del mismo paquete, pero no es accesible desde paquetes externos.
``` java
class MiClase {
    int miVariableDefault = 30;

    void miMetodoDefault() {
        // Código del método
    }
}
```
+ Private: Los miembros privados son accesibles solo desde la misma clase. No se pueden acceder desde clases externas, ni siquiera desde subclases.
``` java
class MiClase {
    private int miVariablePrivada = 40;

    private void miMetodoPrivado() {
        // Código del método
    }
}
```
Ejemplo de uso:
``` java
public class Principal {
    public static void main(String[] args) {
        MiClase miObjeto = new MiClase();
        System.out.println(miObjeto.miVariablePublica);

        // No se puede acceder a miVariableProtegida, miVariableDefault o miVariablePrivada desde aquí
    }
}
```
### Encapsulación
Los modificadores de acceso en Java están estrechamente relacionados con el concepto de encapsulación. La encapsulación es uno de los principios fundamentales de la programación orientada a objetos y se refiere a la idea de ocultar los detalles internos de una clase y proporcionar una interfaz controlada para interactuar con ella.

Los modificadores de acceso desempeñan un papel importante en la implementación de la encapsulación al permitirte controlar qué partes de una clase son accesibles desde otras clases.

Recuerda que el uso adecuado de modificadores de acceso es fundamental para mantener una estructura de código segura y coherente. Cada modificador tiene su propio propósito y contribuye a la encapsulación y modularidad del código.