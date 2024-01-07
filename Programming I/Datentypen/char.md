char ist ein Datentyp, um Zeichen darzustellen.  Zeichen sind jedoch ebenfalls Zahlen!

ASCII definiert 256 unterschiedliche Zeichen, welche durch 1 Byte repräsentiert werden.

• Datentyp zum speichern von (genau einem) Zeichen. 
• wird zur Speicherung ein Byte verwendet. 
• Das Zeichen, das representiert wird hängt von der Kodierung ab.
• C (C++) verwendet standardmäßig ASCII (ISO 8859-1) Anmerkung: Es existieren UNICODE Datentypen z.B. wchar_t (verwendet mehrere Byte)

<div style="background-color:orange; padding:0.5em;border-radius:20px">
<h5 style=color:black>Hinweis:</h5><p style="color:black"><br> Kleine Zahlen sollten dennoch eher mit dem Datentyp short gespeichert werden, aufgrund der Ausgabefunktion.</p></div>

### C++ Syntax
Einzelnes char
```cpp
char character = 'a';
```
