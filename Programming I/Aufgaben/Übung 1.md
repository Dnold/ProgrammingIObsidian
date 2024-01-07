Analysieren Sie im Hinblick auf das EVA-Prinzip die Tätigkeiten, die ein Mensch bzw. ein Computer durchführen muss, um die Hypotenuse c eines rechtwinkligen Dreiecks aus den beiden anderen Seitenlängen a und b zu berechnen. 
a) Welche Eingaben sind nötig? 
b) Welche Verarbeitungsschritte? 
c) Wie sollte die Ausgabe gestaltet werden?




a)
Die Eingaben währen die beiden Werte a und b als die Katheten des Dreiecks.

b)
Um c zu ermitteln müssen die eingegebenen Werte "a" und "b" zuerst quadriert werden, denn 
c² = a² + b²
in C++ würde das so aussehen:
```cpp
float Hypotenuse(float a, float b){
float aSquared = a * a;
float bSquared = b * b;
}
```
Nun muss man `aSquared` und `bSquared` noch zusammen addieren:

```cpp
float Hypotenuse(float a, float b){
float aSquared = a * a;
float bSquared = b * b;

float cSquared = aSquared + bSquared;

}
```
Am Ende zieht man die Wurzel aus `cSquared`
```cpp
float Hypotenuse(float a, float b){
float aSquared = a * a;
float bSquared = b * b;

float cSquared = aSquared + bSquared;
return Sqrt(cSquared);
}
```

c.) Während die Eingabe aus zwei Zahlenwerten besteht, braucht die Ausgabe nur einen Zahlenwert
da man nur ein Skalar benötigt um eine Länge darzustellen.