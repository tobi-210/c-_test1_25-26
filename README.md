Alles klar! Hier ist dein **komplettes README.md** als ein zusammenhängendes Dokument, bereit zum Einfügen in GitHub:

````markdown
# c-_test1_25-26

Dieses Projekt enthält Beispiele für Klassen, Objekte, statische Klassen, Konstruktoren, Getter/Setter und die Standardwerte von Datentypen in C#.

---

## Auto-Klasse Beispiel

```csharp
using System;

namespace OOP // dazu da Namenskonflikte zu vermeiden. Name gleich wie der Folder.
{
    class Auto // Klasse ohne static, ein Objekt muss erstellt werden
    {
        public string Farbe = "Blau";

        public void Fahren()
        {
            Console.WriteLine("Das Auto fährt!");
        }
    }
}
````

---

## Mathe-Klasse Beispiel (statisch)

```csharp
namespace OOP
{
    class Mathe
    {
        public static double pi = 3.14159265359;

        public static void TellPi()
        {
            Console.WriteLine("Pi ist: " + pi);
        }

        public static int Addiere(int a, int b)
        {
            return a + b;
        }
    }
}
```

---

## Main-Programm

```csharp
namespace OOP
{
    public class Program
    {
        static void Main(string[] argv)
        {
            //--------------------------------------------------
            // Class Auto
            Console.WriteLine("\nClass Auto");
            Console.WriteLine("--------------------------------------------------");

            Auto meinAuto = new Auto(); // Erstellung des Objekts
            meinAuto.Farbe = "Rot";

            Console.WriteLine("Die Farbe des Autos ist: " + meinAuto.Farbe);

            Auto meinAuto2 = new Auto();
            meinAuto2.Fahren();

            Console.WriteLine("--------------------------------------------------");

            //--------------------------------------------------
            // Class Mathe
            Console.WriteLine("\nStatische Class Mathe");
            Console.WriteLine("--------------------------------------------------");

            Mathe.TellPi(); // Elemente gehören dann zu der Klasse, in dem Fall also Mathe

            int a = 1;
            int b = 2;

            Console.WriteLine(a + " + " + b + " ergibt " + Mathe.Addiere(a, b));

            Console.WriteLine("--------------------------------------------------");
        }
    }
}
```

---

## Theorie: Konstruktoren, private Methoden, Getter/Setter

### Konstruktoren

Eine spezielle Methode einer Klasse, die automatisch ausgeführt wird, wenn ein Objekt erzeugt wird.
Aufgaben des Constructors: Objekt initialisieren (muss `public` sein, um es zu verwenden).

### Private Methoden

Können nicht direkt von außen gesetzt werden:

```csharp
public class Auto
{
    public string marke;
    private int geschwindigkeit;  // Feld (privat)

    public void SetzeGeschwindigkeit(int wert)
    {
        geschwindigkeit = wert;
    }
}
```

### Getter und Setter

Zugriff auf private Felder über Methoden:

```csharp
private uint age;
private string name;

public void set_age(uint new_age)
{
    age = new_age;
}

public int get_age() 
{
    return age;
}
```

Oder mit `this` um Namenskonflikte zu vermeiden:

```csharp
public void set_age(uint age)
{
    this.age = age;
}
```

---

## Standardwerte von Datentypen

| Datentyp                          | Default-Wert                               | Beispielcode                      |
| --------------------------------- | ------------------------------------------ | --------------------------------- |
| `int`                             | `0`                                        | `int x; // x == 0`                |
| `float`                           | `0.0f`                                     | `float f; // f == 0.0f`           |
| `double`                          | `0.0d`                                     | `double d; // d == 0.0`           |
| `decimal`                         | `0.0m`                                     | `decimal m; // m == 0.0m`         |
| `bool`                            | `false`                                    | `bool b; // b == false`           |
| `char`                            | `'\0'` (Null-Zeichen)                      | `char c; // c == '\0'`            |
| `string`                          | `null`                                     | `string s; // s == null`          |
| **Referenztypen (z. B. Klassen)** | `null`                                     | `MyClass obj; // obj == null`     |
| **Structs (Werttypen)**           | Alle Felder auf ihre Default-Werte gesetzt | `MyStruct s = default(MyStruct);` |
| `DateTime`                        | `01.01.0001 00:00:00`                      | `DateTime dt = default;`          |
| `object`                          | `null`                                     | `object o; // o == null`          |

```

---

Wenn du willst, kann ich auch noch ein **Inhaltsverzeichnis** und **kurze Erklärung zu den Klassen** direkt im README einbauen, damit es richtig professionell aussieht.  

Willst du, dass ich das mache?
```
