---
title: Memory forensics
---

Na badanym komputerze możemy znaleźć wiele śladów pozostawionych przez osobę go użytkującą, ale najpewniej najbardziej interesujące nas informacje można znaleźć wewnątrz zrzutów pamięci (eng: *memory dump*) - czyli utworzonym obrazie pamięci RAM. Zrzuty te bardzo często są bardzo obszerne i zawierają dużo informacji, których nie można łatwo wyciągnąć, np. poprzez komendę `strings`.

W tym przypadku bardzo pomocne jest narzędzie [`Volatility`](https://volatilityfoundation.org/).

Oryginalne pliki źródłowe znajdują się w repozytoriach prowadzonych przez `Volatility Foundation`:

- [Volatility](https://github.com/volatilityfoundation/volatility)
- [Volatility3](https://github.com/volatilityfoundation/volatility3)

!!! info "Różnice między wersjami"
    Czytając o Volatility możemy zadać sobie pytanie, dlaczego istnieją **dwie wersje programu**?

    Podział pochodzi wprost z wersji Pythona, który odpowiada za uruchamianie skryptów:

    - `Volatility` (nazywane również `Volatility2`) korzysta z Pythona w wersji 2.
    - `Volatility3` korzysta z Pythona w wersji 3.
    
!!! question "Którą wersję wybrać?"
    Najnowsza stabilna i najbardziej bogata w funkcje wersja to [Volatility 2.6](https://volatilityfoundation.org/frequently-asked-questions/) (stan na 10.03.2024). Nie jest niestety już ona dalej rozwijana, pomijając pomniejsze poprawki pluginów i bug fixów.

    Oficjalnie rozwijana wersja to *Volatility3*, będąc jednocześnie najbardziej kompatybilną z nowymi wersjami systemów i programów.

    **W SKRÓCIE**

    - Dla starszych zrzutów pamięci i dla większej dostępności pluginów - [`Volatility`](https://github.com/volatilityfoundation/volatility)
    - Dla nowszych systemów i rozwoju - [`Volatility3`](https://github.com/volatilityfoundation/volatility3)

## Podstawy

Baadnie pamięci wbrew pozorom nie jest takie skomplikowane - najistotniejszą kwestią jest użycie odpowiedniego zestawu narzędzi. Dobrym podejściem jest postępowanie według schematu:

1. Komendą `strings` wyszukujemy jakichś wskazówek
2. Identyfikujemy profil obrazu (jaki OS, wersja, etc.)
    1. W `Volatility3` identyfikacja profilu jest zbędna - można natomiast otrzymać dodatkowe informacje o oryginalnym systemie
3. Analizujemy listę procesów i szukamy podejrzanych rekordów
4. Analizujemy historię commandline i listę plików - znowu szukamy podejrzanych rekordów


## Profilowanie obrazu

Profilowanie jest prowadzone w `Volatility2`, by móc ustalić jaki był pierwotny system analizowanego obrazu pamięci.

=== "Volatility 2"
    ``` vol2
    vol.py -f "ścieżka/do/pliku" imageinfo
    ```
=== "Volatility 3"
    ``` vol3
    vol.py -f "ścieżka/do/pliku" windows.info
    ```

## Analiza procesów

TODO: opisać analizę procesów + przykłady

## Dump procesów/plików

TODO: opisać dumpowanie + przykłady

## Źródła

- https://ctf101.org/forensics/what-is-memory-forensics/