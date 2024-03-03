## Programy

Przydatne programy do łamania haseł oraz tworzenia słowników.

1. `hashcat -a <attack> -m <hash_mode> <hash> <dictionary | mask>` - do łamania haseł korzystając ze słownika lub generując wszystkie możliwe kombinacje podanej maski.
2. `john [OPTIONS] [PASSWORD-FILES]` - do łamania haseł podobnie jak _hashcat_.
3. `<file_type>2john <filename>` - set narzędzi do wyciągania haszy z plików. Wyciągnięty format można wstawić równiesz do _hashcat_. np `rar2john`, `zip2john`, `pdf2john`.
4. `aircrack-ng <pcap-file-with-handshake>` - do łamania haseł wifi. Konieczne jest złapanie handshake lub PKMIC data.
5. `airolib-ng <databse> <operation> [options]` - prekomputacja PMKs (Pairwise Master Keys) do wykorzystania w krakowaniu kluczy WPA/WPA2.
6. `hcxtools` - suite narzędzi do wyciągania haszy lub kluczy z plików pcap. Następnie można takie hasze wstawić do _hashcat_
    - `hcxpcapngtool <options> *.*` - convert pcapng, pcap and cap files to hash formats that hashcat and JtR use
    - `hcxhashtool <options>` - konerwsja pomiędzy formatami oraz wyciąganie haszy PKMID/EAPOL lub ESSID.
7. `crunch <min> <max> [options]` - generuje słownik do ataku brute force na postawie podanych opcji.

## Ważne pojęcia matematyczne

### Dzielenie z resztą

Dla liczb całkowitych _a_ i _b_ mówimy, że przystają do siebie modulo liczby naturalnej _n_ gdy:

n | (a - b)

czyli _n_ dzieli różnice _a_ i _b_. Pisze się wtedy:

a = b (mod n)

zapisy ten jest równoważny _a = n * k + b_ dla _k_ będącej liczby całkowitej. Liczba _b_ może być wtedy resztą dizelenia.

W jęsykach programowania, takie działanie jest wykonane operatorem `%` który zwraca resztę dzielena _a_ przez _b_: `a % b`.

### Chińskie twierdzenie o resztach

Jeżeli liczby _m1, m2, ..., mn_ są parami względnie pierwsze to układ kongruencji:

x = a1 (mod m1)

x = a2 (mod m2)

...

x = an (mod mn)

Ma rozwiązanie. Rozwiązanie to jest jednoznaczne modulo produkt liczb _m1, m2, ..., mn_.

### Funkcja Eulera

Funkcja Eulera, oznaczana przez _phi(n)_, dla _n >= 1_ wyznacza liczbę liczb całkowitych względnie pierwszych z _n_ z przedziału _[1,n]_.

### Twierdzenie Eulera

Dla dowolnych liczb całkowitych _a_ oraz liczby naturalnych _n_, jeżeli największy wspólny dzielnik _a_ i _n_ jest 1, to 

a ^ phi(n) = 1 (mod n).

### RSA

RSA jest systemem szyfrowania asymetrycznego, czyli jeden klucz do encrypcji (publiczny) oraz jeden, inny, do dekrypcji (prywatny).

Aby wyznaczyć klucze publiczne oraz prywatne wybieramy najpierw dwie różne liczby pierwsze _p_ i _q_.

Następnie oblicza się _n_ jako produkt liczby _p_ z _q_, oraz _phi(n) = (p - 1) * (q - 1)_.

Wybierana jesy liczba _e_ względnie pierwsza z _phi(n)_.

Obliczana jest odwortność modulo liczby _e_ modulo _phi(n)_:

ed = 1 (mod phi(n))

Para liczb _(n, e)_ jest kluczem publicznym. Liczba _d_ jest kluczem prywatnym.

Wiadomość _m_ można zaszyfrować wstawiając ją do potęgi _e_ modulo _n_:

c = m ^ e (mod n)

Szyfrogam _c_ można odszyfrować wstawiając go do potęgi _d_ modulo _n_:

m = c ^ d (mod n)

Algorytm ten jest uznawany za niebezpieczny.

## Dodatkowe informacje

Zadania w CTFach często są matematyczne. Popularne jest wykorzystać wariację RSA którą łatwo złamać. Sposoby na to są zbyt różne, żeby je opisać. Znając natomiast metodę wykorzystaną do szyfrowania wiadomości można to złamać. Można do tego wykorzystać metodę trial and error. Polecane jest też robienie notatek na kartce.

## Author

- [kiszkot](https://gists.github.com/kiszkot)

## Źródła

1. Alfred J. Menezes, Paul C. van Oorschot, Scott A. Vanstone. _Kryptografia stosowana_, WNT, Warszawa, 2005