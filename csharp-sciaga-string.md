# Metody `string` w C# – ściąga na INF.04

Metody, które najczęściej przydają się w konsolowych zadaniach egzaminacyjnych
(liczenie znaków, palindromy, przetwarzanie linii tekstu).

## 1. Podstawy

| Co | Przykład | Wynik |
|---|---|---|
| `Length` (właściwość) | `"ala".Length` | `3` |
| indeksator `[i]` | `"ala"[0]` | `'a'` |
| `string.IsNullOrEmpty(x)` | `string.IsNullOrEmpty("")` | `true` |
| `string.IsNullOrWhiteSpace(x)` | `string.IsNullOrWhiteSpace("  ")` | `true` |
| `ToUpper()` / `ToLower()` | `"Ala".ToUpper()` | `"ALA"` |
| `Trim()` | `"  ala ".Trim()` | `"ala"` |

## 2. Szukanie

| Metoda | Co robi |
|---|---|
| `Contains("la")` | zwraca `true` lub `false` |
| `IndexOf('l')` | indeks pierwszego wystąpienia albo `-1` |
| `LastIndexOf('a')` | indeks ostatniego wystąpienia |
| `StartsWith("A")` | czy tekst zaczyna się od podanego fragmentu |
| `EndsWith("a")` | czy tekst kończy się podanym fragmentem |

## 3. Wycinanie i zmiana

| Metoda | Przykład | Wynik |
|---|---|---|
| `Substring(start, długość)` | `"kajak".Substring(1, 2)` | `"aj"` |
| `Replace(stare, nowe)` | `"ala".Replace("a", "o")` | `"olo"` |
| `Remove(start, długość)` | `"kajak".Remove(0, 1)` | `"ajak"` |
| `Insert(pozycja, tekst)` | `"ajak".Insert(0, "k")` | `"kajak"` |
| `PadLeft(szerokość, znak)` | `"7".PadLeft(3, '0')` | `"007"` |

## 4. Dzielenie i łączenie

```csharp
string[] czesci = "a b c".Split(' ');      // { "a", "b", "c" }
string razem = string.Join(", ", czesci);  // "a, b, c"
```

## 5. Porównywanie

- `==` porównuje **zawartość** tekstów (w C# działa poprawnie).
- `string.Compare(a, b)` i `a.CompareTo(b)` zwracają liczbę ujemną, zero lub dodatnią
  (przydatne przy własnym sortowaniu).
- `a.Equals(b, StringComparison.OrdinalIgnoreCase)` ignoruje wielkość liter.

## 6. Zamiana na znaki i odwracanie

```csharp
char[] znaki = tekst.ToCharArray();
Array.Reverse(znaki);
string odwrocony = new string(znaki);

foreach (char c in tekst)
{
    // przejście po kolejnych znakach
}
```

## 7. Metody klasy `char`

| Metoda | Co robi |
|---|---|
| `char.IsDigit(c)` | czy znak jest cyfrą |
| `char.IsLetter(c)` | czy znak jest literą |
| `char.IsUpper(c)` / `char.IsLower(c)` | wielka / mała litera |
| `char.ToUpper(c)` / `char.ToLower(c)` | zmiana wielkości litery |
| `c - '0'` | zamiana znaku-cyfry na liczbę |

## 8. Wczytywanie i formatowanie

```csharp
int a = int.Parse(tekst);
bool ok = int.TryParse(tekst, out int b);

string opis = $"{a} + {b} = {a + b}";                           // interpolacja
string wynik = liczba.ToString("0.00", CultureInfo.InvariantCulture);
// CultureInfo wymaga: using System.Globalization;
```

## Najczęstsze pułapki

- **Tekst w C# jest niezmienny.** `tekst.ToUpper()` **nie zmienia** zmiennej,
  tylko zwraca nowy tekst. Trzeba zapisać wynik: `tekst = tekst.ToUpper();`.
- **Indeksy zaczynają się od 0.**
- `Substring` i `Remove` przyjmują **liczbę znaków**, a nie indeks końcowy.
- Wywołanie metody na `null` (np. `tekst.Length`) kończy się wyjątkiem.
  Najpierw sprawdź `string.IsNullOrEmpty(tekst)`.
- Przy bardzo wielu dopisywaniach w pętli lepszy jest `StringBuilder`,
  ale na egzaminie wystarczy zwykłe `+=`.
