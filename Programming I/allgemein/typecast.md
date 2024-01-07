Als **Typumwandlung** ([englisch](https://de.wikipedia.org/wiki/Englische_Sprache "Englische Sprache") _type conversion_ oder _type casting_, kurz _cast_) wird in der [Informatik](https://de.wikipedia.org/wiki/Informatik "Informatik") die Umwandlung eines [Datums](https://de.wikipedia.org/wiki/Daten "Daten") von einem [Datentyp](https://de.wikipedia.org/wiki/Datentyp "Datentyp") in einen anderen bezeichnet. Dadurch werden [Typverletzungen](https://de.wikipedia.org/wiki/Typverletzung "Typverletzung") vermieden, die durch mangelnde [Zuweisungskompatibilität](https://de.wikipedia.org/wiki/Zuweisungskompatibilit%C3%A4t "Zuweisungskompatibilität") entstehen.

Hierbei unterscheidet man zwischen

1. expliziter und impliziter Typumwandlung;
2. werterhaltender und verlustbehafteter Typumwandlung;
3. benutzerdefinierter und vordefinierter (“built-in”) Typumwandlung.

Bei der expliziten Typumwandlung wird die Typumwandlung im [Programmcode](https://de.wikipedia.org/wiki/Programmcode "Programmcode") ausdrücklich hingeschrieben. Je nach [Typisierung](https://de.wikipedia.org/wiki/Typisierung_(Informatik) "Typisierung (Informatik)") der verwendeten [Programmiersprache](https://de.wikipedia.org/wiki/Programmiersprache "Programmiersprache") kann das Fehlen der expliziten Angabe der Typumwandlung einen [Laufzeit](https://de.wikipedia.org/wiki/Laufzeit_(Informatik) "Laufzeit (Informatik)")- oder [Compilezeit](https://de.wikipedia.org/wiki/Compilezeit "Compilezeit")-Fehler zur Folge haben. Im Unterschied dazu erscheinen implizite Typumwandlungen nicht im [Quelltext](https://de.wikipedia.org/wiki/Quelltext "Quelltext"). Sie erfolgen entweder nach Vorschriften, die durch die Programmiersprache vorgegeben sind, oder gemäß einem vom [Programmierer](https://de.wikipedia.org/wiki/Programmierer "Programmierer") an einer anderen Stelle im Quelltext festgelegten Verfahren.

Eine Typumwandlung ist werterhaltend, wenn alle im Ausgangstyp darstellbaren Werte auch im Zieltyp darstellbar sind, so dass sich der Wert, also das umgewandelte Datum, auf keinen Fall ändert. Anderenfalls nennt man sie verlustbehaftet. Implizite Typumwandlungen können eine Fehlerquelle sein, indem versehentlich eine verlustbehaftete Umwandlung verursacht wird. Deshalb erlauben viele Programmiersprachen eine implizite Typumwandlung nur dann, wenn sie werterhaltend ist.

```cpp
Geraet* geraet = new Computer;

Bildschirm* bildschirm = static_cast<Bildschirm*>(geraet);  // Kompiliert nur, wenn entweder Geraet or Bildschirm von der anderen oder derselben Klasse abgeleitet ist
bildschirm = dynamic_cast<Bildschirm*>(geraet);  // Wenn (geraet is Bildschirm), dann bildschirm = (Bildschirm*) geraet, sonst bildschirm = nullptr

Bildschirm& bildschirmR = static_cast<Bildschirm&>(*geraet);  // Wie oben, aber eine Exception wird geworfen, wenn ein nullptr zurückgegeben wird

geraet = nullptr;
bildschirm = dynamic_cast<Bildschirm*>(geraet);  // bildschirm == nullptr

delete geraet;  // gibt die Ressourcen frei
```