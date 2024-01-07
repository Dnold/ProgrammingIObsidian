• Dient zur Speicherung von Wahrheitswerten (also wahr oder falsch) 
• Intern Repräsentiert durch 1 bit (0[false]; 1[true]) 

<p style="color:red">Zu beachten: Jede Zuweisung ≠ 0 wird als 1 gespeichert. Nachfolgender Code würde ausgeführt.</p>
```cpp
bool b = 256
if(b) {/* do something really cool */}
```