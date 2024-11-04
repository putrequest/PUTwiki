# PUTwiki
---

## HOW TO

### Edycja lokalna

1. Sklonuj repozytorium, np. przy pomocy HTTPS URL / GitHub Desktop
2. Zainstaluj Pythona
   1. Python w wersji min. `3.12.1`
   2. Stwórz wirtualne środowisko - nie jest to potrzebne, ale **rekomendowane**
      1. `python -m venv <virtual_environment_name>
   3. Zainstaluj MkDocs Material i dodatkowe potrzebne biblioteki [patrz: [Używane biblioteki](#używane-biblioteki)]
      1. `pip install <nazwa_bilbioteki>` LUB
      2. `pip install -r wiki-req.txt`
   4. Uruchom projekt/stronkę komendą:
      1. `mkdocs serve`

#### Używane biblioteki

| Nazwa                       | Wersja | Źródło                                                              |
| --------------------------- | ------ | ------------------------------------------------------------------- |
| MkDocs Material             | 9.5.43 | https://pypi.org/project/mkdocs-material/                           |
| Git Revision Date Localized | 1.3.0  | https://pypi.org/project/mkdocs-git-revision-date-localized-plugin/ |
| Git Committers              | 2.4.1  | https://pypi.org/project/mkdocs-git-committers-plugin-2/            |


### Deployment na stronę

1. Po edycji/utworzeniu pliku wystarczy go zapisać i stworzyć nowego commita
   1. :warning: UWAGA: dobrą praktyką jest tworzenie zmian na nowych gałęziach (branch), nie powinno się robić zmian na gałęzi `main` przed zweryfikowaniem poprawności działania kodu!
2. GH Pages utworzy instancję ze zaktualizowanymi danymi na gałęzi main po kilku minutach od nadesłania commita.


## Edycja dokumentu

| Plik          | Opis                                                                                                                         |
| -------------:| ---------------------------------------------------------------------------------------------------------------------------- |
| `mkdocs.yml`  | główny plik konfiguracyjny, zawierający wszystkie potrzebne ustawienia potrzebne do poprawnego uruchomienia instancji strony |
| `docs`        | lokalizacja zawierająca wszystkie pliki składające się na wiki                                                               |
| `docs/assets` | podfolder zawierający wszystkie *assety* używane na wiki                                                                     |
| `docs/style`  | podfolder zawierający wszystkie pliki CSS używane na wiki                                                                    |


## Pomocne źródła

| Opis        | Link                                                   |
|--------------------|--------------------------------------------------------|
| **_REFERENCES_**   | https://squidfunk.github.io/mkdocs-material/reference/ |
| source project     | https://squidfunk.github.io/mkdocs-material/           |
| plugins            | https://squidfunk.github.io/mkdocs-material/plugins/   |
| documentation      | https://www.mkdocs.org/                                |
| catalog of plugins | https://github.com/mkdocs/catalog                      |
