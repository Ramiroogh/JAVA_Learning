# Clases Anonimas
Las clases anónimas en Java son una característica que permite crear una clase sin nombre (anónima) que implementa una interfaz o extiende una clase abstracta de forma directa en el lugar donde se necesita. Son útiles cuando solo necesitas una implementación de una interfaz o una extensión de una clase abstracta en un lugar específico del código y *no quieres definir una clase separada para ello*.

Por dentro, las clases anónimas se compilan en una clase interna anónima que se genera automáticamente con un nombre complicado y se utiliza para proporcionar la implementación. Esta clase interna anónima tiene acceso a las variables locales y parámetros final del método donde se crea, lo que permite capturar valores de manera efectiva en el contexto de la clase anónima.

+ Esta clase anonima, se crea cuando el programa es compilado, y puede verse dentro de la carpeta bin, en los archivos de tu programa, dentro de la clase que estas usando esa logica de clase anonima, y debajo una copia exacta de tu clase, pero con un signo dolar $

### Ejemplo
Supongamos que estamos desarrollando una aplicación de manejo de eventos de botones en una interfaz gráfica de usuario (GUI) utilizando la biblioteca Swing. Aquí tienes un ejemplo de cómo podrías usar una clase anónima para manejar eventos de un botón:
``` java
import javax.swing.*;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class EjemploClaseAnonimaGUI {
    public static void main(String[] args) {
        JFrame frame = new JFrame("Ejemplo de Clase Anónima");
        JButton button = new JButton("Haz clic");

        // Usamos una clase anónima para manejar el evento de clic del botón
        button.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                JOptionPane.showMessageDialog(null, "¡Has hecho clic en el botón!");
            }
        });

        // Configuramos la ventana
        frame.setLayout(new FlowLayout());
        frame.add(button);
        frame.setSize(300, 100);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setVisible(true);
    }
}
```
En este ejemplo, estamos creando una ventana Swing con un botón. Para manejar el evento de clic del botón, utilizamos una clase anónima que implementa la interfaz ActionListener. Dentro del método actionPerformed, mostramos un cuadro de diálogo emergente cuando se hace clic en el botón.

Este es un caso típico en el que las clases anónimas son útiles en la programación de interfaces de usuario, ya que nos permiten definir y manejar eventos en el lugar donde se necesitan sin tener que crear clases separadas para cada tipo de evento.

+ Veamos otro ejemplo sencillo:
``` java
Comparator<String> comp = new Comparator<String>() {

  @Override
  public int compare(String s1, String s2) {
    return s1.compareTo(s2);
  }
};
```
En este ejemplo, se genera una clase anónima y se crea un objeto de tipo Comparador.