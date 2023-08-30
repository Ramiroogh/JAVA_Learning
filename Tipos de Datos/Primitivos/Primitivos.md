# Lista de Valores Primitivos
Acompañado de su superclase y tamaños de bytes.

### char
``` java
Character cRef = new Character('A');
```
Lo interesante es que el char es casi un tipo numérico. Tiene dos bytes, al igual que el tipo short, pero no usa el primer bit para almacenar el signo. En otras palabras, el char solo almacena números positivos. Esto significa que el char puede almacenar valores entre 0 y 65536 (2 ^ 16).