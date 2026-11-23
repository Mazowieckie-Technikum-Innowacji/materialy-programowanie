# GitHub Desktop: Git bez wpisywania poleceń

**GitHub Desktop** to darmowy program z okienkami, który robi to samo co polecenia `git clone`, `git add`, `git commit`,
`git push` i `git pull`, ale klikaniem. Dobry na początek, zanim nauczysz się terminala. Działa na Windows i macOS.

> Opis oparty na typowym wyglądzie programu (interfejs jest po angielsku). Nazwy przycisków mogą się nieco różnić
> w nowszych wersjach.

## 1. Instalacja i logowanie

1. Pobierz program ze strony **https://desktop.github.com** i zainstaluj go (domyślne ustawienia).
2. Uruchom i wybierz **Sign in to GitHub.com**. Otworzy się przeglądarka: zaloguj się na **swoje konto GitHub**
   (u nas: konto dodane do organizacji szkoły) i potwierdź.
3. W kroku „Configure Git" wpisz swoje **imię i nazwisko** oraz **adres e-mail**: będą widoczne przy Twoich commitach.
   Jeśli nie chcesz podawać prawdziwego adresu, użyj adresu `noreply` z ustawień konta GitHub.

## 2. Pobierz zadanie na swój komputer (klonowanie)

1. Przyjmij zadanie w Classroom 50 (link od nauczyciela). Powstanie Twoje repozytorium.
2. Na stronie repozytorium na GitHubie kliknij zielony przycisk **Code** i wybierz **Open with GitHub Desktop**.
   (Albo w programie: **File → Clone repository…**, zakładka **GitHub.com**, wybierz repozytorium z listy.)
3. Wybierz folder na dysku (**Local path**) i kliknij **Clone**.

Repozytorium jest teraz na Twoim komputerze. Folder otworzysz przyciskiem **Show in Explorer**, a projekt w edytorze
przyciskiem **Open in Visual Studio** (jeśli program ma go ustawionego jako edytor w **File → Options → Integrations**).

## 3. Zmieniasz pliki i zapisujesz (commit)

1. Edytuj pliki w Visual Studio (albo innym edytorze) i zapisz je (`Ctrl+S`).
2. W GitHub Desktop w lewym panelu, na zakładce **Changes**, zobaczysz listę zmienionych plików. Po kliknięciu pliku widać,
   co dokładnie się zmieniło (zielone linie to dodane, czerwone to usunięte).
3. W polu **Summary** (na dole po lewej) wpisz **krótki opis zmiany**, np. „Dodano klasę Notatka".
4. Kliknij **Commit to main**. Zmiana jest zapisana na Twoim komputerze (to jeszcze nie jest wysłane na GitHub).

## 4. Wyślij na GitHub (push)

Kliknij **Push origin** na górnym pasku. Po chwili Twoja praca jest na GitHubie. W repozytorium zadania uruchomi się
automatycznie ocenianie: wynik zobaczysz w zakładce **Actions** na GitHubie i w „Feedback".

## 5. Pobierz zmiany z GitHuba (pull)

Gdy pracujesz na dwóch komputerach albo nauczyciel coś zmienił w Twoim repozytorium, **zanim zaczniesz pracę** kliknij
**Fetch origin** (sprawdza, czy są nowe zmiany), a jeśli program pokaże **Pull origin**, kliknij go.

## 6. Typowe problemy

| Objaw | Co zrobić |
|---|---|
| **Push origin** jest wyszarzony albo program prosi o **Pull origin** | najpierw kliknij **Pull origin**, potem **Push origin** |
| Pojawia się okno **Resolve conflicts** | ten sam fragment pliku zmieniono w dwóch miejscach: otwórz plik, wybierz właściwą wersję (usuń znaczniki `<<<<<<<`, `=======`, `>>>>>>>`), zapisz i dokończ commit |
| W **Changes** są setki plików (`bin`, `obj`…) | brakuje pliku `.gitignore`. Dodaj go: w terminalu `dotnet new gitignore` albo skopiuj z szablonu zadania |
| Nie widzisz swojego repozytorium na liście klonowania | sprawdź, czy jesteś zalogowany na właściwe konto (**File → Options → Accounts**) i czy przyjąłeś zadanie |
| Chcesz cofnąć zmiany w pliku, których jeszcze nie zapisałeś w commicie | kliknij plik prawym przyciskiem → **Discard changes** (uwaga: tego nie da się cofnąć) |
| Zrobiłeś commit, ale chcesz poprawić jego opis | do czasu push: **Repository → Amend last commit** (dostępne w nowszych wersjach) |

## 7. Przydatne rzeczy

- Zakładka **History** pokazuje wszystkie wcześniejsze commity i zmiany w każdym z nich.
- Menu **Branch** pozwala tworzyć gałęzie (domyślna to `main`). Przy zadaniach z Classroom 50 zwykle pracujesz na `main`.
- Przycisk **Fetch origin** / **Pull origin** / **Push origin** to jeden przycisk, który zmienia nazwę zależnie od stanu.

## 8. Co dalej

- [Git w pigułce](git-podstawy.md): te same czynności w terminalu i typowe błędy.
- [Jak zacząć z C#](https://github.com/Mazowieckie-Technikum-Innowacji/csharp-jak-zaczac): instalacja Visual Studio i pierwszy program.
- [Słowniczek](slowniczek.md): pojęcia (commit, push, pull, gałąź, klon).
