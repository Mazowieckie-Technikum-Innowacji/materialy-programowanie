# Lista kontrolna: część praktyczna INF.04 (aplikacja konsolowa, mobilna, dokumentacja)

Lista do **samodzielnego sprawdzenia** przed oddaniem pracy z części praktycznej egzaminu INF.04
(projektowanie, programowanie i testowanie aplikacji). Oparta na typowej budowie arkusza: aplikacja konsolowa,
aplikacja mobilna i dokumentacja.

> **Ważne:** to ściąga pomocnicza napisana własnymi słowami, a nie arkusz egzaminacyjny. Każdy arkusz ma własne
> polecenie i własne wymagania (nazwy folderów, nazwy klas, wygląd programu). **Zawsze czytaj treść swojego arkusza**
> i rób to, co w nim napisano. Gdy lista jest sprzeczna z arkuszem, wygrywa arkusz.

## 0. Zanim zaczniesz (czas na zapoznanie się z zadaniem)

- [ ] Przeczytaj całe zadanie do końca (części I, II i III), zanim napiszesz pierwszą linię kodu.
- [ ] Zaznacz w arkuszu **nazwy**, które musisz zachować: nazwy klas, pól, metod, folderów, plików, napisów na ekranie.
- [ ] Sprawdź, **jakim numerem się podpisujesz** (numer zdającego, PESEL lub inny): będzie potrzebny w nazwie folderu i w dokumentacji.
- [ ] Zapisz sobie, jakie **dokładnie teksty** program ma wyświetlać (łącznie ze znakami, wielkością liter i spacjami).
- [ ] Zaplanuj czas (przykładowo: część I ok. 1/3, część II ok. 1/3, dokumentacja i zrzuty ekranu ok. 1/3 czasu, z zapasem
      na sprawdzenie). Nie utknij na jednej części.

## 1. Struktura folderów

- [ ] Utwórz **folder główny** nazwany tak, jak każe arkusz (zwykle numerem zdającego).
- [ ] W nim podfoldery o **dokładnie takich nazwach**, jak w arkuszu (zwykle: `konsolowa`, `mobilna`, `dokumentacja`).
- [ ] W każdym podfolderze **tylko to, co arkusz wymienia** (np. archiwum projektu, pliki z kodem, plik wykonywalny).
- [ ] Po zakończeniu pracy sprawdź w Eksploratorze, że pliki są w **właściwych** folderach.

## 2. Aplikacja konsolowa

### Klasa i jej elementy
- [ ] Język programowania jest taki, jaki wolno użyć na stanowisku (sprawdź w arkuszu).
- [ ] Nazwa klasy i elementów jest **znacząca** (polska albo angielska, ale spójna w całym programie).
- [ ] Pola mają **wymagane typy** (napisowy, liczbowy, logiczny, data) i wymagany **poziom dostępu** (np. ogólnodostępne).
- [ ] Konstruktory mają **wymaganą liczbę i kolejność argumentów** i robią dokładnie to, co opisano
      (przypisują wartości, ustawiają datę na „teraz" itd.).
- [ ] Metoda ma wymagany **typ zwracany** i **argumenty** (np. bezargumentowa, bez zwracania wartości).

### Program główny
- [ ] Tworzy **obiekty w opisany sposób** (każdym wymaganym konstruktorem).
- [ ] Dane, które mają być wpisane **na stałe**, są wpisane w kodzie, a pobierane z klawiatury: naprawdę czytane z klawiatury.
- [ ] Wywołuje metodę/metody wypisujące i **wynik wygląda tak, jak na ilustracji** w arkuszu (te same linie, ten sam układ).
- [ ] Komunikaty dla użytkownika są **zrozumiałe** (np. „Podaj tytuł: ", a nie „wpisz").

### Jakość kodu
- [ ] Kod jest **sformatowany**: wcięcia, puste linie między metodami, jedna instrukcja w linii.
- [ ] Brak zbędnego, zakomentowanego kodu i „śmieciowych" zmiennych.
- [ ] Program **kompiluje się bez błędów** i **uruchamia** się.
- [ ] Przetestowałeś go **kilka razy** (np. z pustym tekstem, długim tekstem, nietypowymi znakami).

## 3. Aplikacja mobilna

- [ ] Używasz **środowiska i emulatora dostępnych na stanowisku**.
- [ ] Układ (layout) ma **wymagany typ rozkładu** i **kolory**: sprawdź dokładnie kody lub nazwy kolorów z arkusza.
- [ ] Wszystkie wymagane **elementy interfejsu** są obecne w kolejności z arkusza (napisy, lista, pola tekstowe, przycisk).
- [ ] Teksty napisów, przycisków i podpowiedzi są **dokładnie takie**, jak w poleceniu.
- [ ] **Stan początkowy** zgadza się z opisem (np. jedna notatka na liście).
- [ ] Po naciśnięciu przycisku robi się **dokładnie to, co opisano** (nowy element, dodanie do kolekcji, odświeżenie widoku listy).
- [ ] Lista **odświeża się** po dodaniu elementu (kolekcja odpowiedniego typu albo powiadomienie adaptera).
- [ ] Przycisk działa też, gdy pola są **puste** lub zawierają dziwne znaki (nic się nie wysypuje).
- [ ] Aplikacja **kompiluje się i uruchamia na emulatorze**. Jeśli nie da się uruchomić, masz zrzut z listą błędów
      (zgodnie z poleceniem w arkuszu).

## 4. Dokumentacja

### Komentarz dokumentujący metodę
- [ ] Jest **jeden** nagłówek dokumentacji metody w kodzie aplikacji konsolowej (nad nazwą metody lub pod nią).
- [ ] Zawiera **wszystkie pola ze wzoru** w arkuszu, w tej kolejności (np. nazwa, opis, parametry, zwracany typ, autor).
- [ ] Zamiast `<…>` wpisałeś **swoje opisy**. W polu „autor" jest **wymagany numer**.
- [ ] Jeśli metoda nie ma parametrów lub nic nie zwraca, wpisałeś **„brak"**.
- [ ] Komentarz jest zapisany **poprawną składnią komentarza** w Twoim języku (`//` albo `/* … */`).

### Zrzuty ekranu
- [ ] Zrzut obejmuje **cały ekran** razem z **paskiem zadań** (nie samo okno programu).
- [ ] Widać **uruchomiony program** (okno z wynikiem) **i** otwarte środowisko programistyczne z projektem lub okno terminala z kompilacją.
- [ ] Jeśli program się nie kompiluje: zrzut z **oknem błędów** i otwartym środowiskiem.
- [ ] Masz **tyle zrzutów, ile interakcji** wykonuje program (np. start i po dodaniu elementu).
- [ ] Pliki mają **nazwy ze wzoru z arkusza** (np. `konsola1`, `konsola2`, `mobilna1`…).

### Plik z opisem narzędzi
- [ ] Plik tekstowy ma **nazwę z arkusza** (np. `egzamin`).
- [ ] W środku: **system operacyjny**, **środowiska programistyczne**, **emulator**, **języki programowania**.
- [ ] Plik leży w folderze **dokumentacja**.

## 5. Przed oddaniem

- [ ] Sprawdziłeś **wszystkie** punkty polecenia, nie tylko te, które są łatwe.
- [ ] Przejrzałeś **wynik programu** porównując go z ilustracją w arkuszu, znak po znaku.
- [ ] Przygotowałeś **archiwa projektów** i skopiowałeś **pliki z kodem** (tylko te modyfikowane, jeśli tak mówi arkusz).
- [ ] Otworzyłeś **folder z wynikami** i potwierdziłeś, że nic nie brakuje (kod, archiwa, zrzuty, plik z narzędziami).
- [ ] **Nie zmieniłeś już niczego** po zrobieniu zrzutów ekranu (żeby zrzuty zgadzały się z oddanym kodem).
- [ ] Jeśli arkusz wymaga **nagrania na nośnik** lub opisania go numerem, zrobiłeś to zgodnie z poleceniem i sprawdziłeś nagranie.

## Najczęstsze błędy na egzaminie

| Błąd | Jak go uniknąć |
|---|---|
| Inna nazwa klasy, pola lub folderu niż w arkuszu | przepisz nazwy z arkusza i porównaj na końcu |
| Pola lub metoda nie są ogólnodostępne (`public`) | zaznacz w arkuszu poziom dostępu i sprawdź w kodzie |
| Konstruktory mają argumenty w złej kolejności | czytaj kolejność argumentów z arkusza słowo po słowie |
| Napis na ekranie różni się o jedną literę lub spację | skopiuj tekst z arkusza i porównaj z wynikiem programu |
| Brak numeru zdającego w dokumentacji | wpisz go od razu przy tworzeniu komentarza |
| Zrzut ekranu tylko z oknem programu | zrób zrzut **całego ekranu** z paskiem zadań |
| Zapomniany plik z opisem narzędzi | dodaj go do listy zadań na początku egzaminu |
| Brak czasu na część III | zostaw na nią zapas, bo dokumentacja jest oceniana osobno |

## Zasady korzystania z materiałów na egzaminie

Co wolno mieć i używać podczas egzaminu, określa komisja i instrukcja w arkuszu. Ta lista służy do **ćwiczeń** i do
sprawdzania własnych prac przed egzaminem.
