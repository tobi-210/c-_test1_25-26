# c-_test1_25-26


using System.Runtime.CompilerServices;

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


    public class Program // Bauplan für Objekte. Beschreibt welche Datein ein Objekt hat und welche Funktionen es besitzt. Beim Test public setzen.
    {
        static void Main(string[] argv) // wieder public verwenden. Main groß schreiben. Main ist static weil das Programm starten soll bevor ein objekt existiert
        {

            //--------------------------------------------------
            //Class Auto

            Console.WriteLine("\nClass Auto");
            Console.WriteLine("--------------------------------------------------");

            Auto meinAuto = new Auto(); // Erstellung des Objekts
            meinAuto.Farbe = "Rot";

            Console.WriteLine("Die Farbe des Autos ist: " + meinAuto.Farbe);

            Auto meinAuto2 = new Auto();

            meinAuto2.Fahren();

            Console.WriteLine("--------------------------------------------------");

            //--------------------------------------------------


            //--------------------------------------------------
            //Class Mathe

            Console.WriteLine("\nStatische Class Mathe");
            Console.WriteLine("--------------------------------------------------");

            Mathe.TellPi(); // Elemente gehören dann zu der Klasse, in dem Fall also Mathe

            int a = 1;
            int b = 2;

            Console.WriteLine(a + " + " + b + " ergibt " + Mathe.Addiere(a, b));

            Console.WriteLine("--------------------------------------------------");

            //--------------------------------------------------





        }

    }

}


// Sonstige Theorie:

// Constructor: eine spezielle Methode einer Klasse, die automatisch ausgeführt wird, wenn ein Objekt erzeugt wird.
// Aufgaben des Constructors: Objekt initialisieren (muss public sein, um es zu verwenden)

// Private Methoden

// können nicht von alleine gesetzt werden:

// ----------------------------------------------------------

//  public class Auto
// {
//
//public string marke;
//    private int geschwindigkeit;  // Feld (privat)
//
//    public void SetzeGeschwindigkeit(int wert)
//    {
//        geschwindigkeit = wert;
//    }
// }
//
// ----------------------------------------------------------

// Getter und Setter
// gleich wie normale Methoden, aber kann auf private Felder zugreifen

// In der Class:

// ----------------------------------------------------------
//
//private uint age;
// private string name;
//
// public void set_age(uint new_age)
// {
//   age = new_age;
// }
//
// public int get_age() 
// {
// return age;
// }
//
// oder mit this.age = age; beide dienen dazu um Namenskonflikte zu vermeiden
//
// ----------------------------------------------------------

// Standartwerte
//
//  | Datentyp                          | Default-Wert                               | Beispielcode                      |
//  | --------------------------------- | ------------------------------------------ | --------------------------------- |
//  | `int`                             | `0`                                        | `int x; // x == 0`                |
//  | `float`                           | `0.0f`                                     | `float f; // f == 0.0f`           |
//  | `double`                          | `0.0d`                                     | `double d; // d == 0.0`           |
//  | `decimal`                         | `0.0m`                                     | `decimal m; // m == 0.0m`         |
//  | `bool`                            | `false`                                    | `bool b; // b == false`           |
//  | `char`                            | `'\0'` (Null-Zeichen)                      | `char c; // c == '\0'`            |
//  | `string`                          | `null`                                     | `string s; // s == null`          |
//  | **Referenztypen (z. B. Klassen)** | `null`                                     | `MyClass obj; // obj == null`     |
//  | **Structs (Werttypen)**           | Alle Felder auf ihre Default-Werte gesetzt | `MyStruct s = default(MyStruct);` |
//  | `DateTime`                        | `01.01.0001 00:00:00`                      | `DateTime dt = default;`          |
//  | `object`                          | `null`                                     | `object o; // o == null`          |







