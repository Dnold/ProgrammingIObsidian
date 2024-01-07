### Datentyp "int" in C++

Der Datentyp "int" in C++ repräsentiert ganze Zahlen (Integer) und ist ein essenzieller Bestandteil der Programmierung. Im Vergleich zu anderen Datentypen wie "char" handelt es sich bei "int" um eine Darstellung von numerischen Werten, nicht von Zeichen.
#### Charakteristika des Datentyps "int":

- **Speichergröße:** Der Datentyp "int" verwendet normalerweise 4 Bytes (32 Bit) zur Speicherung von ganzen Zahlen.
    
- **Darstellung von Zahlen:** Im Gegensatz zum "char"-Datentyp, der Zeichen repräsentiert, kann "int" eine breite Palette von ganzen Zahlen darstellen, von negativen zu positiven Werten.
    
- **Verwendung von ASCII:** Anders als bei "char" spielt der ASCII-Code hier keine direkte Rolle, da "int" für numerische Werte steht.
    
#### C++ Syntax zur Deklaration eines "int":
```cpp
int number = 42;
```
#### Hinweis zur Verwendung:

Es ist wichtig zu beachten, dass der Datentyp "int" für ganze Zahlen verwendet wird, während "char" für die Darstellung von Zeichen genutzt wird. Der richtige Einsatz hängt von der Art der Daten ab, die gespeichert und verarbeitet werden sollen.

<div style="background-color:orange; padding:0.5em;border-radius:20px"> <h5 style="color:black">Hinweis:</h5> <p style="color:black"><br> Kleine Zahlen sollten dennoch eher mit dem Datentyp "short" gespeichert werden, besonders wenn es um die Ausgabe geht, aufgrund der Ausgabefunktion.</p></div>