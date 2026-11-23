# Git i GitHub: podstawy w pigułce

Dla początkujących: jak pobrać projekt, zapisać zmiany i wysłać je na GitHub.

## Pojęcia

| Pojęcie | Co to jest |
|---|---|
| **repozytorium** | folder projektu razem z historią zmian |
| **commit** | „zdjęcie" projektu w danym momencie, z krótkim opisem |
| **push** | wysłanie commitów z komputera na GitHub |
| **pull** | pobranie nowych commitów z GitHuba |
| **klon** | kopia repozytorium z GitHuba na Twoim komputerze |

## Pierwsze kroki

```
git clone https://github.com/<organizacja>/<repozytorium>.git
cd <repozytorium>
```

Po zmianach w plikach:

```
git status                      # co się zmieniło
git add .                       # dodaj zmiany do commitu
git commit -m "krótki opis"     # zapisz zmiany
git push                        # wyślij na GitHub
```

Zanim zaczniesz kolejną pracę, pobierz nowości:

```
git pull
```

## Typowe problemy

- **„Please tell me who you are"**: Git nie zna Twojego imienia i e-maila. Ustaw je raz:
  `git config --global user.name "Imię Nazwisko"` i `git config --global user.email "adres@przyklad.pl"`.
- **`git push` jest odrzucony** („rejected", „fetch first"): na GitHubie są zmiany, których nie masz u siebie.
  Wykonaj `git pull`, a potem `git push` jeszcze raz.
- **Konflikt przy `git pull`**: ten sam fragment pliku zmieniono w dwóch miejscach. Otwórz plik, wybierz właściwą
  wersję (usuń znaczniki `<<<<<<<`, `=======`, `>>>>>>>`), potem `git add .` i `git commit`.
- **Zapomniałem dodać plik do commitu**: `git add <plik>` i `git commit --amend --no-edit`, dopóki nie zrobiłeś `git push`.
- **Nie widzę repozytorium (strona 404)**: zaloguj się na właściwe konto GitHub. Repozytoria prywatne są niewidoczne
  dla osób bez dostępu.

## Czego nie wrzucać do repozytorium

- haseł, kluczy i tokenów,
- folderów generowanych przy budowaniu (np. `bin/`, `obj/`, `node_modules/`). Dodaj je do pliku `.gitignore`.

## Dalej

- [Dokumentacja Git](https://git-scm.com/doc)
- [Wprowadzenie do GitHuba](https://docs.github.com/pl/get-started)
