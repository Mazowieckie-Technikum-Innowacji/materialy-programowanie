# Classroom 50: przewodnik dla uczniów

Jak przyjąć zadanie, pracować nad nim, wysłać je i zobaczyć wynik. W Mazowieckim Technikum Innowacji zadania z
programowania rozdajemy przez **Classroom 50** i **GitHub**. Ocenianie robi się **automatycznie**: po każdym wysłaniu pracy
testy na GitHubie sprawdzają Twój kod i pokazują wynik.

## 1. Jak to działa w skrócie

1. Nauczyciel wysyła Ci **link do zadania**.
2. Klikasz link i **przyjmujesz zadanie**. GitHub tworzy Twoje **własne repozytorium** z plikami startowymi.
3. **Pobierasz** je na komputer, rozwiązujesz zadanie i **wysyłasz** (push) na GitHub.
4. Po każdym wysłaniu **testy uruchamiają się same** i dają Ci wynik w punktach.
5. Poprawiasz kod i wysyłasz ponownie, aż wynik Cię zadowoli (do terminu).

## 2. Zanim zaczniesz

- Potrzebujesz **konta GitHub dodanego do organizacji szkoły** (Mazowieckie-Technikum-Innowacji).
  Gdy nauczyciel Cię doda, dostaniesz **zaproszenie** e-mailem i na GitHubie. **Zaakceptuj je** (przycisk w mailu lub na
  stronie https://github.com/Mazowieckie-Technikum-Innowacji).
- Zainstaluj **Git** albo **GitHub Desktop** oraz edytor kodu, np. Visual Studio. Instrukcje:
  [GitHub Desktop](github-desktop.md) i [jak zacząć z C#](https://github.com/Mazowieckie-Technikum-Innowacji/csharp-jak-zaczac).
- Logując się do GitHuba, **używaj tego samego konta**, na które dostałeś zaproszenie.

## 3. Przyjmij zadanie

1. Kliknij **link do zadania** od nauczyciela. Otworzy się strona Classroom 50.
2. Zaloguj się przez GitHub (jeśli trzeba) i sprawdź, że widzisz **swoje imię i login** („Signed in as …").
3. Zobaczysz nazwę zadania, **termin oddania** i nazwę repozytorium, które powstanie, np.
   `4tpb-ad-csharp-klasa-notatka-twojlogin`.
4. Kliknij **Accept assignment** i poczekaj chwilę. Powstanie **Twoje repozytorium** (prywatne). Widzisz je tylko Ty
   i nauczyciele.
5. W repozytorium zobaczysz też otwartego **pull requesta „Feedback"**. To miejsce, w którym zbierają się komentarze
   i wynik oceniania.

> **Ważne:** pracujesz w **swoim** repozytorium (w nazwie jest Twój login), a **nie** w „szablonie" zadania. W szablonie nie
> masz uprawnień do zapisu, a próba wysłania tam zmian kończy się komunikatem o braku dostępu i propozycją „fork".

## 4. Pobierz repozytorium na komputer

- **GitHub Desktop:** na stronie swojego repozytorium kliknij **Code → Open with GitHub Desktop** i **Clone**.
- **Terminal:** `git clone https://github.com/Mazowieckie-Technikum-Innowacji/<nazwa-twojego-repozytorium>.git`
  (adres skopiujesz przyciskiem **Code**).

Wejdź do folderu i **przeczytaj plik `README.md`**: opisuje zadanie, wymagania i punktację.

## 5. Rozwiązuj zadanie

- Edytuj **tylko pliki wskazane w README** (np. `Notatka.cs`, `Program.cs`).
- **Nie zmieniaj** plików z testami (np. folderu `Notatki.Tests`), pliku `.classroom50.yaml` ani folderu `.github`:
  to one uruchamiają ocenianie. Ich zmiana może je zepsuć albo będzie uznana za próbę oszustwa.
- Uruchamiaj i testuj kod u siebie na bieżąco (w README są polecenia, np. `dotnet test`), zanim wyślesz go na GitHub.

## 6. Wyślij pracę (to jest „oddanie")

W repozytorium z zadaniem **każdy push na gałąź `main` jest oddaniem pracy** i uruchamia ocenianie.

- **GitHub Desktop:** **Commit to main**, potem **Push origin**.
- **Terminal:**

  ```
  git add .
  git commit -m "opis zmiany"
  git push
  ```

Możesz wysyłać **wiele razy**. Liczy się (zwykle) ostatnia wersja przed terminem, o czym decyduje nauczyciel.

## 7. Zobacz wynik

Po około **1-2 minutach** od wysłania:

- Na stronie repozytorium przy ostatnim commicie zobaczysz **znaczek**: zielony (wszystko zaliczone) lub czerwony (są błędy).
  Po najechaniu zobaczysz opis, np. **„classroom50 autograde: 65/100 (4/7 tests passed)"**.
- W zakładce **Actions** znajdziesz uruchomienie o nazwie **Autograde**. Po wejściu w nie zobaczysz, **które testy się
  nie udały i dlaczego**.
- W pull requeście **Feedback** zbierają się wyniki i komentarze nauczyciela.

Jeśli test się nie powiódł, przeczytaj jego komunikat. Zwykle mówi, czego brakuje albo co jest nie tak (np. „metoda powinna
wypisać 5 linii"). Popraw kod, wyślij ponownie i sprawdź wynik jeszcze raz.

## 8. Terminy

- **Termin oddania** widzisz na stronie przyjmowania zadania i w opisie zadania w Classroom 50.
- Prace wysłane po terminie mogą być oznaczone jako **spóźnione**. Co się wtedy dzieje z oceną, decyduje nauczyciel.
- Nie zostawiaj wysyłania na ostatnią minutę: ocenianie trwa chwilę i czasem wymaga poprawek.

## 9. Typowe problemy

| Objaw | Co zrobić |
|---|---|
| Strona **404** albo „nie masz dostępu" | zalogowałeś się na **inne konto GitHub** niż to, które dostało zaproszenie, albo nie zaakceptowałeś zaproszenia do organizacji |
| Classroom 50 nie pokazuje Twojego zadania | sprawdź, czy jesteś zalogowany na właściwe konto i czy nauczyciel dodał Cię do klasy |
| Komunikat o braku dostępu i propozycja „fork" przy `git push` | pracujesz w **szablonie** zamiast w swoim repozytorium (z loginem w nazwie). Sklonuj właściwe repozytorium |
| `git push` jest odrzucony („rejected") | na GitHubie są zmiany, których nie masz u siebie: wykonaj `git pull`, potem `git push` |
| Wynik 0/100 mimo działającego programu | sprawdź w zakładce **Actions**, czy któryś krok nie wywrócił się na starcie (np. błąd kompilacji) i czy nie zmieniłeś plików testów |
| Wysłałeś pracę, a wyniku nie ma | poczekaj 2-3 minuty i odśwież stronę. Jeśli nadal nic, sprawdź zakładkę **Actions** |
| Nie wiesz, co jest wymagane | wróć do `README.md` w repozytorium. Jeśli nadal niejasne, zapytaj nauczyciela |

## 10. Zasady

- Pracujesz **samodzielnie**, chyba że zadanie mówi inaczej.
- Nie udostępniaj swojego repozytorium innym i nie kopiuj cudzych rozwiązań.
- **Nie wrzucaj do repozytorium haseł ani tokenów.**
- Nie usuwaj i nie zmieniaj plików uruchamiających ocenianie (`.classroom50.yaml`, `.github/`).

## 11. Gdzie szukać pomocy

- Najpierw **README zadania** i komunikaty testów w zakładce Actions.
- Potem [słowniczek](slowniczek.md), [Git w pigułce](git-podstawy.md) i [GitHub Desktop](github-desktop.md).
- Jeśli nadal utknąłeś, **zapytaj nauczyciela** i pokaż mu komunikat błędu (zrzut ekranu).
