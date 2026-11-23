# Snippety C# do Visual Studio (INF.04)

Zestaw **45 fragmentów kodu (snippetów)** do Visual Studio dla aplikacji konsolowych w C#. Zamiast pisać od zera
typowe konstrukcje (klasa z konstruktorami, wczytanie liczby, pętla po tablicy, `try/catch`, sortowanie), wpisujesz
krótki skrót, naciskasz **Tab** i Visual Studio wstawia gotowy kod. To materiał do **ćwiczeń**.

Obok jest też [ściąga z metod `string` i `char`](../csharp-sciaga-string.md).

W tym folderze jest 45 plików `.snippet` (po jednym na skrót) i ta instrukcja.

## Jak zainstalować (Visual Studio)

1. Pobierz repozytorium: zielony przycisk **Code → Download ZIP** i rozpakuj, albo sklonuj je gitem.
2. W Visual Studio: **Narzędzia → Menedżer fragmentów kodu** (`Ctrl+K`, `Ctrl+B`).
3. Wybierz język **Visual C#** i kliknij **Importuj**.
4. Przejdź do folderu `snippety`, zaznacz wszystkie pliki `.snippet` (`Ctrl+A`) i kliknij **Otwórz**.
5. Jako folder docelowy wybierz **My Code Snippets** i kliknij **Zakończ**.

**Alternatywa bez importu:** skopiuj pliki `.snippet` do folderu
`Documents\Visual Studio 18\Code Snippets\Visual C#\My Code Snippets` (numer w nazwie folderu odpowiada wersji Visual Studio)
i uruchom Visual Studio ponownie.

> Fragmenty są zapisywane **osobno dla każdego konta Windows**. Jeśli ćwiczysz na kilku kontach (np. na koncie
> „Egzamin" na pracowni), zainstaluj je na każdym z nich.

## Jak używać

1. W edytorze kodu C# wpisz **skrót** (np. `klasa`).
2. Naciśnij **Tab** (dwa razy, jeśli podpowiedź IntelliSense jest otwarta). Pojawi się gotowy kod.
3. Kolejne naciśnięcia **Tab** przenoszą Cię między **polami do uzupełnienia** (podświetlone na kolorowo): nazwa klasy,
   typ, nazwa zmiennej itd. Wpisujesz swoje wartości.
4. **Enter** kończy edycję fragmentu.

### Przykład: skrót `klasa`

Wpisujesz `klasa`, Tab, Tab i dostajesz:

```csharp
public class Klasa
{
    private int pole;

    public Klasa()
    {
        pole = 0;
    }

    public Klasa(int pole)
    {
        this.pole = pole;
    }

    public override string ToString()
    {
        return $"{pole}";
    }
}
```

Nazwa klasy, typ pola, nazwa pola i wartość domyślna to pola do zmiany (Tab przechodzi między nimi, a zmiana nazwy
klasy zmienia ją od razu we wszystkich konstruktorach).

## Spis skrótów

### Metody i klasy
| Skrót | Co wstawia |
|---|---|
| `metv` | statyczna metoda bez zwracania wartości (`void`) |
| `metr` | statyczna metoda zwracająca wartość (`return`) |
| `klasa` | klasa z polem, konstruktorem domyślnym, konstruktorem z parametrem i `ToString` |
| `kons` | konstruktor z parametrem (przypisuje parametr do pola) |
| `konk` | konstruktor kopiujący |
| `statprop` | właściwość statyczna (licznik instancji, `private set`) |
| `tostr` | nadpisanie metody `ToString` |
| `dziedz` | klasa pochodna z wywołaniem konstruktora bazowego |
| `abskl` | klasa abstrakcyjna z metodą abstrakcyjną |
| `intf` | deklaracja interfejsu |
| `klstat` | klasa statyczna (narzędziowa) z metodą |

### Wczytywanie danych i wyjątki
| Skrót | Co wstawia |
|---|---|
| `rdint` | wczytanie liczby całkowitej (`int.Parse(Console.ReadLine())`) |
| `rdtry` | wczytanie liczby z walidacją (`TryParse` w pętli, aż do poprawnej) |
| `rdstr` | wczytanie tekstu do zmiennej `string` |
| `rddbl` | wczytanie liczby rzeczywistej (akceptuje kropkę i przecinek) |
| `trc` | `try / catch` z obsługą `FormatException` i `ArgumentException` |
| `thr` | `throw new ArgumentException` |
| `thrr` | `throw new ArgumentOutOfRangeException` |
| `rnd` | losowa liczba z zakresu min–max (włącznie) |

### Losowanie, tablice, listy
| Skrót | Co wstawia |
|---|---|
| `tabl` | tablica `int[]` wypełniona liczbami losowymi |
| `tabw` | pętla `for` wypisująca indeks i wartość |
| `tabs` | suma (`long`) i średnia (`double`) tablicy |
| `tabm` | minimum i maksimum tablicy |
| `tabszuk` | szukanie w tablicy (indeks pierwszego wystąpienia, `-1` gdy brak) |
| `lst` | lista `List<T>`: utworzenie i dodanie elementu |
| `sortb` | sortowanie bąbelkowe (metoda sortująca `int[]`) |

### Algorytmy i tekst
| Skrót | Co wstawia |
|---|---|
| `nwd` | NWD (algorytm Euklidesa) |
| `pierw` | test liczby pierwszej |
| `pal` | sprawdzenie palindromu w `string` |
| `samog` | zliczanie samogłosek (z polskimi znakami) |
| `fmt2` | format z 2 miejscami po przecinku (`ToString` z kropką jako separatorem) |
| `silnia` | silnia w pętli (`long`) |
| `fib` | n-ty wyraz ciągu Fibonacciego (pętla) |

### Tekst (stringi)
| Skrót | Co wstawia |
|---|---|
| `strrev` | odwrócenie tekstu (`ToCharArray`, `Array.Reverse`) |
| `strfor` | pętla `foreach (char c in tekst)` po znakach |
| `strcnt` | zliczanie wystąpień wybranego znaku w tekście |
| `strkl` | zliczanie liter, cyfr, wielkich i małych liter (`char.IsLetter`, `IsDigit`…) |
| `strwords` | podział na słowa (`Split` z `RemoveEmptyEntries`), ich liczba i wypisanie |
| `strjoin` | podział tekstu po separatorze i połączenie z innym (`Split` + `string.Join`) |
| `strcmp` | porównanie bez rozróżniania wielkości liter (`Equals(..., OrdinalIgnoreCase)`) |
| `strcap` | pierwsza litera każdego słowa wielka, reszta mała |
| `strcez` | szyfr Cezara (przesunięcie liter a–z i A–Z o `k`) |
| `strcyf` | suma cyfr znajdujących się w tekście (`c - '0'`) |

Pozostałe metody `string` i `char` znajdziesz w [ściądze](../csharp-sciaga-string.md).

### Pliki
| Skrót | Co wstawia |
|---|---|
| `filer` | wczytanie linii z pliku (`File.ReadAllLines` i `foreach`) |
| `filew` | zapis linii do pliku (`File.WriteAllLines`) |

## Uwagi

- Znak `$` w kodzie (interpolacja `$"..."`) jest w plikach `.snippet` zapisany jako `$$`. Visual Studio zamienia to z
  powrotem na `$`, więc nic nie musisz poprawiać.
- Fragmenty to **punkt wyjścia**: sprawdź, czy wstawiony kod pasuje do polecenia, i dostosuj nazwy do zadania. Na
  egzaminie liczy się to, że rozumiesz kod, który oddajesz.
- Zasady korzystania z narzędzi i własnych materiałów na egzaminie zawodowym określa komisja, nie to repozytorium.
