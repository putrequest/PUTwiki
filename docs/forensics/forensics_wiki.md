![Forensics_wiki_header](https://gist.github.com/assets/64504618/2439fd43-b385-4a06-95f2-e7526c1e7947)

# ProTipy
1. Zawsze warto sprawdzać otrzymane pliki komendą `file <filename>`! Jeśli zawartość pliku widnieje jako "`data`" to należy użyć innych narzędzi do wyciągnięcia naszych cennych informacji;
2. Sprawdzaj metadane EXIF przy użyciu komendy `exiftool <filename>`;
3. Używaj `strings` dla dodatkowych podpowiedzi;
4. Do filecarvingu/wyciągania plików z plików można użyć:
   1. `binwalk <filename>` - samo polecenie tylko wyświetla możliwą zawartość pliku na podstawie znalezionych [`magic numbers`](#magic-numbers);
   2. `foremost <filename>` - znajduje i ekstraktuje pliki do folderu `output` w tej samej lokalizacji;
   3. `steghide`
   4. `zsteg`
5. Jeśli plik ma rozszerzenie `.img` oznacza to, że jest to zrzut obrazu całego dysku - plik zawiera w sobie bootloader i tabelę partycji & należy znaleźć odpowiedni [`offset`](#offset) partycji, żeby móc ją zamontować i przeglądać dane w niej zawarte. Do tego zadania najłatwiej jest użyć narzędzia `fdisk`.
   1. Wpisując `fdisk -l <path/to/image>` otrzymujemy informacje o dumpie przechowywanym w pliku
   ![Linux101 Managing_drive_mount_drive](https://gist.github.com/assets/64504618/6c827fa5-0611-4d51-9ca9-dfd893e37732)
   2. Przykładowo możemy odczytać block-size i start-block interesującej nas partycji.
   3. Można też w łatwy sposób odczytać offset konkretnej partycji.
      1. Np. *offset* dla partycji pierwszej (będącej też partycją bootowania btw.) wyliczamy poprzez pomnożenie bajtów na sektor/blok z offsetem sektora/bloku (kolumna **Start**):
         ```
         512 * 2048 = 1048576
         ```
      2. Dla partycji trzeciej (będącej jednocześnie największą - więc też pewnie zawierającą najwięcej interesujących danych):
         ```
         512 * 731136 = 374341632
         ```
    4. Z tymi informacjami możemy przejść do montowania obrazu za pomocą komendy `mount`:
       ```
       mount -o loop,offset=374341632 <file> <mount_location>
       ```
       !! Lokalizacja montowania musi być wcześniej stworzona (*mkdir*...)
       
       !! polecenie *mount* należy uruchamiać z prawami **admina**
       1. Na szczęście nie trzeba samemu wyliczać potrzebnego *offsetu*, część offsetową komendy można zapisać jako `offset=$((512*731136))` (shell sam sobie wyliczy wartość i przekaże do komendy)

# Ciekawe stronki
* https://gchq.github.io/CyberChef/ - Cyberchef
* https://www.dcode.fr/xor-cipher - Przetwarzanie XOR tekstu
* https://www.base64decode.org - Base64 decoder

# Programy

## Lista skryptów i komend
Lista mniejszych programów i skryptów (wraz z najczęściej używanymi flagami/argumentami)

1. `file <filename>` - określa rodzaj pliku
2. `exiftool <filename>` - wyświetla metadane EXIF
3. `strings` - wyszukuje tekst w pliku i wylistowuje wszystkie rekordy w kolejnych wierszach
4. `foremost <filename>` - filecarving/wyciąganie plików z plików
5. `fdisk` - obsługa dyskowej tablicy partycji
6. `mount` - montowanie obrazów

## **Cyberchef** - wielozadaniowe narzędzie internetowe
* Za pomocą cyberchefa mamy możliwość przetworzenia danych na wszelkie sposoby, a jednocześnie możemy tworzyć "przepisy", czyli sekwencje przetwarzające po kolei konkretne dane wejściowe.

## **Volatility** - analiza zrzutów pamięci 
* aktualnie bardziej zaawansowana wersja istnieje na Pythona 2 - i ma bardzo dużo poradników!
* Na Pythonie 3 wersja jest ciągle w fazie rozwojowej - dużo funkcji nie działa...

### Volatility - użycie

## **Autopsy** - analiza obrazów dysków

## [**Process Monitor**](https://learn.microsoft.com/en-us/sysinternals/downloads/procmon)
Narzędzie do monitorowania i analizy aktywnych procesów w systemie. Przedstawia w czasie rzeczywistym informacje o systemie plików, rejestrze i aktywnych procesach.

## [**ProcDump**](https://learn.microsoft.com/en-us/sysinternals/downloads/procdump)
Narzędzie do tworzenia dumpów pamięci i nie tylko.

## **G'MIC** - program do obróbki obrazów
* przydatny np. przy XORowaniu obrazów
  * `gmic <img_1> <img_2> -blend xor -o <result_img>`

# Słowniczek
#### **magic numbers**
- początkowe bajty pliku jednoznacznie identyfikujące konkretny typ, [przykładowa lista](https://www.garykessler.net/library/file_sigs.html), [druga lista](https://asecuritysite.com/forensics/magic); 

#### **offset** 
- pozycja danego pola, nagłówka lub innych danych w pliku lub pamięci operacyjnej względem wybranego punktu odniesienia[[1]](https://pl.wikipedia.org/wiki/Offset_(informatyka));

---

## Autor

- [mattix1710](https://gist.github.com/mattix1710)

## Źródła

- [CTF Playbook](https://fareedfauzi.gitbook.io/ctf-playbook/digital-forensics)