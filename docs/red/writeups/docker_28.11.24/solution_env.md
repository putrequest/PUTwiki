# Rozwiązanie - ENV

Skoro mamy dostępny tylko obraz możemy zrobić dwie rzeczy:
- Zobaczyć polecenia budujące obraz używająć `docker history`
- Przeglądać pliki gotowego obrazu 

Zobaczmy zatem `docker history`

```sh
docker pull typicalam/mysecondapp
docker history --no-trunc typicalam/mysecondapp
```

Nic ciekawego nie widać, większość warstw bierze się z obrazu bazowego zawierającego `go`. Przechodzimy więc do drugiego kroku, narzędziem `dive` zobaczmy co jest w środku obrazu:


```sh
go install github.com/wagoodman/dive@latest
dive typicalam/mysecondapp:latest
```

lub

```sh
docker run --rm -it -v /var/run/docker.sock:/var/run/docker.sock wagoodman/dive:latest typicalam/mysecondapp:latest
```

Interesująca wydaje się instrukcja `COPY . /app`, którą widać było w `docker history` - dodaje ona wszystkie pliki aplikacji do kontenera docelowego. Jeżeli przesuniemy się do tej instrukcji używając `dive` zauważamy, że ma ona digest `sha256:3a99e5f4470d934f8b254bb351e17593cd7a429dfc5c903a0b08702a4a64f0b6`. Możemy użyć tego jako identyfikatora warstwy obrazu, rozpakujmy go:

```sh
docker save typicalam/mysecondapp:latest -o obraz.tar
mkdir obraz
tar xvf obraz.tar --directory=obraz
cd obraz/blobs
file 3a99e5f4470d934f8b254bb351e17593cd7a429dfc5c903a0b08702a4a64f0b6 # Nasz digest znaleziony przez dive
3a99e5f4470d934f8b254bb351e17593cd7a429dfc5c903a0b08702a4a64f0b6: POSIX tar archive
```

Rozpakujmy archiwum, aby dostać się do plików w tej warstwie:

```sh
mkdir warstwa
tar x
tar xvf --directory=warstwa 3a99e5f4470d934f8b254bb351e17593cd7a429dfc5c903a0b08702a4a64f0b6
ls -la warstwa
app
cd warstwa/app
ls -la
.  ..  Dockerfile  .env  .git  .gitignore  go.mod  main.go
```

Oprócz standardowych rzeczy - plików `go` do budowy programu widzimy jeszcze parę doatkowych rzeczy, takich jak:
- Folder `.git` - możemy zobaczyć po `.git/config`, że jesteśmy w repo `https://github.com/TypicalAM/VulnerableENV`
- Plik `.gitignore z treścią `.env` - w takim razie deweloperzy nie chcieli, aby ten plik był gdziekolwiek wypuszczony. Zwykle pliki `.env` zawierają zmienne środowiskowe używane przez deweloperów do testowania swoich programów.

Być może plik ten był używany do testowania funkcjonalności aplikacji, gdyż instrukcja uruchomienia `-e HELLO_USER=imie` w `docker run` kazała nam nadpisać zmienną środowiskową. Sprawdźmy zawartość `.env`:

```sh
cat .env
HELLO_USER="PUTrequest{zanieczyszczenie_srodowiska}"
```

i tak oto zdobyliśmy drugą flagę!
