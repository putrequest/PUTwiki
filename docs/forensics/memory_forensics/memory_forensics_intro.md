---
title: Memory forensics
---

Na badanym komputerze możemy znaleźć wiele śladów pozostawionych przez osobę go użytkującą, ale najpewniej najbardziej interesujące nas informacje można znaleźć wewnątrz zrzutów pamięci (eng: *memory dump*) - czyli utworzonym obrazie pamięci RAM. Zrzuty te bardzo często są bardzo obszerne i zawierają dużo informacji, których nie można łatwo wyciągnąć, np. poprzez komendę `strings`.

W tym przypadku bardzo pomocne jest narzędzie [`Volatility`](https://volatilityfoundation.org/).

## Podstawy

Baadnie pamięci wbrew pozorom nie jest takie skomplikowane - najistotniejszą kwestią jest użycie odpowiedniego zestawu narzędzi. Dobrym podejściem jest postępowanie według schematu:

1. Komendą `strings` wyszukujemy jakichś wskazówek
2. Identyfikujemy profil obrazu (jaki OS, wersja, etc.)
3. Analizujemy listę procesów i szukamy podejrzanych rekordów
4. Analizujemy historię commandline i listę plików - znowu szukamy podejrzanych rekordów

## Profilowanie obrazu

TODO: opisać profilowanie

## Analiza procesów

TODO: opisać analizę procesów + przykłady

## Dump procesów/plików

TODO: opisać dumpowanie + przykłady

## Źródła

- https://ctf101.org/forensics/what-is-memory-forensics/