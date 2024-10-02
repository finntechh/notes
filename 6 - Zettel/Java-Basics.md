
### Primitive Datentypen

integer --> int, long, byte, short  
floating point --> float, double  
character --> char  
logical --> boolean

Die Abstufungen der integer werden genutzt um Speicher zu sparen, da
sie von long --> byte immer kleiner werden und so weniger Ressourcen benötigen.

|   Type  | Size (bits) | Minimum |     Maximum    |            Example            |
|:-------:|:-----------:|:-------:|:--------------:|:-----------------------------:|
| byte    | 8           | -27     | 27– 1          | byte b = 100;                 |
| short   | 16          | -215    | 215– 1         | short s = 30_000;             |
| int     | 32          | -231    | 231– 1         | int i = 100_000_000;          |
| long    | 64          | -263    | 263– 1         | long l = 100_000_000_000_000; |
| float   | 32          | -2-149  | (2-2-23)·2127  | float f = 1.456f;             |
| double  | 64          | -2-1074 | (2-2-52)·21023 | double f = 1.456789012345678; |
| char    | 16          | 0       | 216– 1         | char c = ‘c’;                 |
| boolean | 1           | –       | –              | boolean b = true;             |  
***
***int***  
+ Standardwert ohne Zuweisung ist 0.
+ Wird die Variable in einer Methode definiert muss ihr ein Wert zugewiesen werden bevor sie benutzt werden kann.
+ Nachkommastellen werden abgeschnitten-

***
***float***
+ Standardwert ohne Zuweisung ist 0.0
+ Nach 6 Nachkommastellen wird es ungenau --> "Big Decimal".
+ mit *f* designation kann die float definiert werden. (vgl. bei double mit D)

```Java
float dezimal = 3.41f;
```
double ist doppelt so groß wie float und nutzt 64 statt 32 bits als Speicher.
***
***char***
+ Steht für die Unicode der character. 
```Java
char c = 'a';
char c = 61; //61 in der Unicode Tabelle ist das Äquivalent zu klein a. 
```
#### Overflow

Trifft ein wenn die maximale Grenze des Typs überschritten wird 
und gibt infinity $\infty$.  

#### Underflow

Das Gegenteil zum Overflow trifft auf wenn die unterste Grenze
(Im negativen Bereich) unterschritten wird.  
In diesem Fall wird 0.0 ausgegeben.

### Objekt/Refernz - Typen

Zeigen auf Werte oder Objekte oder dem Wert *null*.
Ein *String*s ist beispielsweise ein Referenztyp.


### Variable deklarieren

Typ + Name der Variable (Identifier) + Semicolon

```Java
int a;
```  
Variable deklarieren mit Zuweisung:
Typ + Name + Zuweisungsoperator "=" + Semicolon

```Java
int a = 10;
String name = "Tobi";
```
Der Unterschied zwischen *char* und *String* ist die Anzahl der quotes "a" ist ein *String*
während 'a' ein *char* darstellt.

### Identifier  

Ein identifier ist ein Name für dessen Erstellung folgende Regeln gelten:
1. Startet mir einem Buchstabe, underscore oder dollar Zeichen
2. Darf kein Schlüsselwort sein.
3. Darf nicht *true*, *false*, oder *null* sein.  

### Arrays

Schema:
***typ[] identifier = new typ[länge];***
  
Um auf ein Wert im Array zuzugreifen wird der Name des Arrays und
der Index einer Variablen zugewiesen.

```Java
int[] numbers = new int[100];

numbers[0] = 1;

int firstElement = numbers[0];
```
Array Index startet bei 0 (vgl. Python & co.)  
Die Länge eines Array kann mit *numbers.length* abgerufen werden.

```Java
int lengthOfNumbersArray = numbers.length;
```

### Java Keywords (Schlüsselwörter)

Haben eine besondere Bedeutng und können nicht als Identifier benutzt werden. (vgl. Python (for, break, etc.))

```Java
public
static
class
main
new
instanceof
```  

### Operatoren in Java

Zuweisungsoperator =

#### Arithmetische Operatoren

(+) --> Addition und String Konkatenierung  
(-) --> Subtraktion  
(*) --> Multiplikation  
(/) --> Division
(%) --> Modulus (Rest einer Division)

#### Logische Operatoren

(&&) --> AND  
(||) --> OR  
(!) --> NOT  

#### Vergleichsoperatoren

(<) --> Kleiner als  
(>) --> Größer als  
(<=) --> Kleiner als oder gleich  
(>=) --> Größer als oder gleich  
(==) --> Gleich  
(!=) --> Nicht gleich zu

### Programmstruktur in Java

Das Grundelement ist die *Class*, welche mehrere *properties*, 
*methods* und andere *inner classes* enthalten kann.  
Damit seine Klasse ausführbar ist muss sie die *main* Methode besitzen.

```Java
public class SimpleAddition {

    public static void main(String[] args) {
        int a = 10;
        int b = 5;
        double c = a + b;
        System.out.println( a + " + " + b + " = " + c);
    }
}
```
Als Codeblock bezeichnet man den Code zwischen den geschweiften Klammern einer Klasse.

### Compiling und Ausführung

Java Runtime Environment JRE muss installiert sein.  

```Java
javac Programm.java
```
Erstellt eine *.class* Datei welche dann mit dem *java* Befehl
ausgeführt werden kann.

```Java
java Programm
```