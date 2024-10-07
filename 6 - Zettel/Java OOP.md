#Note
2024-10-07
Tags: [[Java]] [[Programmierung]] [[OOP]]

### Klassen, Objekte und Methoden

Eine Klasse wird durch ihr Member aufgebaut. Hinter dem Begriff "Member"
verstecken sich die wesentlichen Bestandteile einer Klasse. 

+ Variablen (auch Attribute genannt)
+ Konstruktoren
+ Methoden  

Attribute enthalten Informationen über des Zustands der Objekte, die sie beschreiben.
Methoden enthalten den Code einer Klasse und beschreiben somit ihr Verhalten.
Sie können den Zustand und die Werte von Attributen verändern. Konstruktoren sind 
spezielle Methoden, welche zur Objekterzeugung aufgerufen werden.

```Java
[Modifizierer] class Klassenname [extends Basisklasse] [implements Interface-Liste] {

//Attribute
private int zahl;
private String name;

//Konstruktoren
public Klassenname() {
    this.zahl = 100;
    this.name = "Tom";
    };

//Methoden
public void printHelloWorld() {
    System.out.println("Hello World!");
    };

public static void main(String[] args) {
    Klassenname meineNeueKlasse = new Klassenname();
    meineNeueKlasse.printHelloWorld();
    };
}
```  
Es ist darauf zu achten, dass pro Datei nur eine Klasse den Modifizierer
*public* besitzt. Am Besten ist es, wenn man pro Datei nur eine Klassen verwendet. Der Dateiname
muss der Name der Klasse entsprechen.

### Objekterzeugung mit *new*

---
## Info

[[Baeldung]]