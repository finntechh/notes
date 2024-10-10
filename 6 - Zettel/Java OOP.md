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
*public* besitzt. Am besten ist es, wenn man pro Datei nur eine Klasse verwendet. Der Dateiname
muss der Name der Klasse entsprechen.

#### Objekterzeugung mit *new*

Mit dem *new* Operator lässt sich ein neues Objekt einer Klasse erzeugen.
Dieser Prozess wird Instanziierung genannt und die Objekte werden folglich auch als Instanzen
der Klasse bezeichnet.

#### Identität


### Konkrete Klassen, interfaces und abstrakte Klassen

#### Konkrete Klasse
In konkreten Klassen sind alle Methoden implementiert und von der Klasse kann mit dem *new*
Operator eine neue Instanz erstellt werden.

Aufbau einer konkreten Klasse:
```Java
public class Auto() {
    public String bremsen() {
        return "Auto bremst";
    }
    
    public String hupen() {
        return "Auto hupt";
    }
    
}

Auto neuesAuto = new Auto();
```

Interfaces und abstrakte Klassen können in konkrete Klassen eingebaut werden.
```Java
public class SchönesAuto extend Fahrzeug implements Fahrbar {
    public String hupen() {
        return "Auto hupt";
    }
}
```

#### Interfaces

Können als Vorlagen von Klassen verwendet werden und enthalten uninplementierte Methoden. 
```Java
interface Fahrbar {
    void bremsen();
    void hupen();
}
```

#### Abstrakte Klassen

Eine abstrakte Klasse kann unimplementierte und implementierte Methoden enthalten.
```Java
public abstract class Fahrzeug {
    public abstract String hupen();
    
    public String fahren() {
        return "Auto Fährt";
    }
}
```

### Access Modifiers

Access Modifier regeln in Java die Zugriffsrechte auf Methoden, Variablen, Konstruktoren oder Klassen.  
Eine Top-Level Klasse kann nur default oder public als Access Modifier besitzen. 
Auf dem Member-Level, also in einer Top-Level Klasse können alle verwendet werden.

#### Vergleich der Modifier Public, Protected, Default, und Private

| Modifier  | Class | Package | Subclass | World |
|:---------:|:-----:|:-------:|:--------:|:-----:|
|  public   |   Y   |    Y    |    Y     |   Y   |
| protected |   Y   |    Y    |    Y     |   N   |
|  default  |   Y   |    Y    |    N     |   N   |
|  private  |   Y   |    N    |    N     |   N   |

Der default access modifier wird auch gesetzt, wenn kein access modifier definiert wird.  
Default und package-private meinen das Gleiche.

### Standard Reihenfolge der Modifikatoren

Annotation --> Access Modifier --> andere Keywords  

|  **Allgemein**  |   **Klassen**   |  **Methoden**   |
|:---------------:|:---------------:|:---------------:|
|   Annotation    |   Annotation    |   Annotation    |
| Access Modifier | Access Modifier | Access Modifier |
|    abstract     |    abstract     |    abstract     |
|     static      |     static      |     static      |
|      final      |      final      |      final      |
|    transient    |    strictfp     |  synchronized   |
|    volatile     |                 |     native      |
|                 |                 |    strictfp     |


---
## Info

[[Baeldung]]