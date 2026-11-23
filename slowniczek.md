# Słowniczek programisty (C#)

Najważniejsze pojęcia z lekcji programowania, wyjaśnione krótko i z przykładem w C#.
Hasła są pogrupowane tematycznie. Polskie nazwy podajemy razem z angielskimi, bo w dokumentacji i w Visual Studio
spotkasz oba warianty.

## Spis

- [Podstawy](#podstawy)
- [Klasy i obiekty](#klasy-i-obiekty)
- [Sterowanie programem](#sterowanie-programem)
- [Tablice i kolekcje](#tablice-i-kolekcje)
- [Tekst i dane](#tekst-i-dane)
- [Błędy i wyjątki](#błędy-i-wyjątki)
- [Narzędzia](#narzędzia)
- [Git i GitHub](#git-i-github)

## Podstawy

| Pojęcie | Wyjaśnienie |
|---|---|
| **program** | ciąg instrukcji, które komputer wykonuje po kolei |
| **kod źródłowy** (*source code*) | tekst programu napisany przez programistę, zapisany w plikach (w C#: `.cs`) |
| **kompilacja** (*compile*) | zamiana kodu źródłowego na program, który komputer potrafi uruchomić |
| **zmienna** (*variable*) | nazwane miejsce w pamięci na wartość, np. `int wiek = 17;` |
| **stała** (*constant*) | wartość, której nie można zmienić po ustawieniu, np. `const double Pi = 3.14;` |
| **typ** (*type*) | rodzaj danych w zmiennej: `int` (liczba całkowita), `double` (liczba rzeczywista), `bool` (prawda/fałsz), `char` (znak), `string` (tekst) |
| **instrukcja** (*statement*) | pojedynczy krok programu, zwykle kończony średnikiem |
| **wyrażenie** (*expression*) | coś, co ma wartość, np. `2 + 3` albo `wiek > 18` |
| **operator** | symbol działania: `+`, `-`, `*`, `/`, `%` (reszta z dzielenia), `==` (równe), `&&` (i), `||` (lub) |
| **przypisanie** (*assignment*) | zapisanie wartości do zmiennej: `x = 5;` (znak `=` to przypisanie, a `==` to porównanie) |
| **komentarz** (*comment*) | tekst dla ludzi, pomijany przez kompilator: `// do końca linii` albo `/* kilka linii */` |
| **konsola** (*console*) | okno tekstowe, w którym program wypisuje wyniki i czyta dane z klawiatury |
| **argument i parametr** | parametr to nazwa w definicji metody, argument to wartość podana przy jej wywołaniu |

## Klasy i obiekty

| Pojęcie | Wyjaśnienie |
|---|---|
| **klasa** (*class*) | wzór (przepis) na obiekty: opisuje, jakie mają pola i co potrafią robić |
| **obiekt** (*object*) | konkretny egzemplarz klasy, utworzony słowem `new`, np. `var n = new Notatka("Zakupy");` |
| **pole** (*field*) | zmienna należąca do obiektu, przechowuje jego dane |
| **właściwość** (*property*) | „inteligentne pole" z odczytem i zapisem: `public string Tytul { get; set; }` |
| **metoda** (*method*) | funkcja należąca do klasy: to, co obiekt potrafi zrobić |
| **konstruktor** (*constructor*) | specjalna metoda wywoływana przy tworzeniu obiektu, ma nazwę klasy i nie zwraca wartości |
| **przeciążanie** (*overloading*) | kilka metod lub konstruktorów o tej samej nazwie, ale różnych argumentach |
| **modyfikator dostępu** (*access modifier*) | mówi, kto widzi element: `public` (wszyscy), `private` (tylko ta klasa), `protected` (klasa i klasy pochodne) |
| **`this`** | odwołanie do bieżącego obiektu, np. `this.tytul = tytul;` |
| **`static`** | element należący do klasy, a nie do konkretnego obiektu (np. `Console.WriteLine`) |
| **dziedziczenie** (*inheritance*) | klasa pochodna przejmuje pola i metody klasy bazowej: `class Pies : Zwierze` |
| **klasa abstrakcyjna** (*abstract class*) | klasa, z której nie tworzy się obiektów, tylko dziedziczy; może mieć metody bez treści |
| **interfejs** (*interface*) | lista metod, które klasa musi zaimplementować (obietnica „umiem to robić") |
| **polimorfizm** (*polymorphism*) | ta sama metoda działa inaczej w różnych klasach pochodnych |
| **hermetyzacja** (*encapsulation*) | ukrywanie szczegółów w klasie i dawanie dostępu przez metody lub właściwości |
| **`override`** | nadpisanie metody klasy bazowej, np. `public override string ToString()` |

## Sterowanie programem

| Pojęcie | Wyjaśnienie |
|---|---|
| **warunek** (*if / else*) | wybór, co wykonać, zależnie od tego, czy coś jest prawdą |
| **pętla** (*loop*) | powtarzanie fragmentu kodu |
| **`for`** | pętla z licznikiem, gdy wiadomo, ile razy powtórzyć |
| **`while`** | pętla wykonywana, dopóki warunek jest prawdziwy |
| **`foreach`** | pętla po wszystkich elementach kolekcji lub tekstu |
| **`switch`** | wybór jednego z wielu wariantów |
| **metoda `Main`** | punkt wejścia: od niej zaczyna się wykonywanie programu |
| **rekurencja** (*recursion*) | metoda, która wywołuje samą siebie (np. silnia) |
| **algorytm** (*algorithm*) | przepis na rozwiązanie zadania, opisany krok po kroku |

## Tablice i kolekcje

| Pojęcie | Wyjaśnienie |
|---|---|
| **tablica** (*array*) | stała liczba elementów tego samego typu, numerowanych od zera: `int[] t = new int[5];` |
| **indeks** (*index*) | numer elementu; pierwszy element ma indeks `0`, ostatni `Length - 1` |
| **lista** (*`List<T>`*) | kolekcja o zmiennej długości: można dodawać i usuwać elementy |
| **kolekcja** (*collection*) | wspólna nazwa dla struktur przechowujących wiele elementów |
| **sortowanie** (*sorting*) | ustawianie elementów w kolejności (np. bąbelkowe, `Array.Sort`) |
| **`ObservableCollection<T>`** | kolekcja, która powiadamia widok (np. listę na ekranie) o zmianach |

## Tekst i dane

| Pojęcie | Wyjaśnienie |
|---|---|
| **`string`** | tekst, ciąg znaków; w C# jest niezmienny (każda zmiana tworzy nowy tekst) |
| **konwersja** (*parsing*) | zamiana tekstu na liczbę: `int.Parse("5")` albo `int.TryParse(tekst, out int x)` |
| **interpolacja** (*string interpolation*) | wstawianie wartości do tekstu: `$"Wiek: {wiek}"` |
| **kodowanie** (*encoding*) | sposób zapisu znaków w bajtach (np. UTF-8); od niego zależy, czy widać polskie znaki |
| **`DateTime`** | typ przechowujący datę i czas; `DateTime.Now` to bieżąca chwila |
| **plik tekstowy** | zwykły plik z tekstem; w C# czytasz go `File.ReadAllLines`, zapisujesz `File.WriteAllLines` |

## Błędy i wyjątki

| Pojęcie | Wyjaśnienie |
|---|---|
| **błąd kompilacji** (*compile error*) | program nie da się zbudować; kompilator wskazuje plik i linię |
| **ostrzeżenie** (*warning*) | program się zbuduje, ale kompilator zwraca uwagę na coś podejrzanego |
| **błąd wykonania** (*runtime error*) | program wystartował, ale w trakcie działania coś poszło nie tak |
| **błąd logiczny** (*logic error*) | program działa, lecz daje zły wynik, bo źle zaplanowaliśmy algorytm |
| **wyjątek** (*exception*) | sygnał o błędzie w trakcie działania, np. `FormatException` czy `DivideByZeroException` |
| **`try / catch`** | blok kodu, w którym przechwytujemy wyjątek, żeby program się nie zatrzymał |
| **`throw`** | zgłoszenie własnego wyjątku, np. `throw new ArgumentException("Zły argument");` |
| **`null`** | „brak wartości": odwołanie do metody na `null` kończy się wyjątkiem |
| **debugowanie** (*debugging*) | szukanie błędów przez zatrzymywanie programu i podglądanie zmiennych |
| **punkt przerwania** (*breakpoint*) | miejsce w kodzie, w którym debugger zatrzymuje program |

## Narzędzia

| Pojęcie | Wyjaśnienie |
|---|---|
| **IDE** | środowisko programistyczne: edytor, kompilator i debugger w jednym (np. Visual Studio) |
| **.NET SDK** | zestaw narzędzi do budowania i uruchamiania programów w C# (`dotnet`) |
| **projekt** (*project*) | zbiór plików, z których powstaje jeden program (plik `.csproj`) |
| **rozwiązanie** (*solution*) | zbiór projektów, plik `.sln` |
| **snippet** (fragment kodu) | skrót, który po wciśnięciu Tab wstawia gotowy kod |
| **dokumentacja** (*documentation*) | opis tego, co robi kod: komentarze i pliki README |
| **test automatyczny** (*unit test*) | program sprawdzający, czy inny fragment kodu działa poprawnie |

## Git i GitHub

| Pojęcie | Wyjaśnienie |
|---|---|
| **repozytorium** (*repository*) | folder projektu razem z historią zmian |
| **commit** | zapisany stan projektu z krótkim opisem |
| **push / pull** | wysłanie zmian na GitHub / pobranie zmian z GitHuba |
| **klon** (*clone*) | kopia repozytorium z GitHuba na Twoim komputerze |
| **gałąź** (*branch*) | równoległa linia zmian w repozytorium (domyślna to `main`) |
| **pull request** | prośba o włączenie zmian z jednej gałęzi do innej, z możliwością komentowania |
| **`.gitignore`** | lista plików i folderów, których Git ma nie zapisywać (np. `bin/`, `obj/`) |
| **fork** | własna kopia cudzego repozytorium na GitHubie |

Więcej: [przewodnik dla początkujących](https://github.com/Mazowieckie-Technikum-Innowacji/csharp-jak-zaczac),
[Git w pigułce](git-podstawy.md), [ściąga `string` i `char`](csharp-sciaga-string.md).
