# Rozwiązanie - Wywrotka

```
Zasady:
- Nie modyfikujesz kontenera
- Sukces jest wtedy, gdy aplikacja wydrukuje `SUKCES`
```

Po uruchomieniu widzimy:

```sh
docker run --rm -it unknow/wywrotka
ERROR: Brak pliku konfiguracyjnego
```

Musimy w takim razie znaleźć jakiś sposób na podanie pliku konfiguracyjnego. Sprawdźmy `docker history`:

```sh
docker history --no-trunc unknow/wywrotka
```

Widnieją trzy interesujące instrukcje:

```Dockerfile
ENTRYPOINT ["../../../../../../../../../../../../../../../starter.sh"]
ADD starter.sh /starter.sh
apk update && apk add dash && mv /usr/bin/dash /bin/runner && chmod +x /starter.sh && rm /bin/sh /bin/ash /bin/cat /bin/ls /usr/bin/*
```

czyli `starter.sh` jest kopiowany z maszyny hosta podczas budowania i jest on programem odpalanym podczas uruchamiania kontenera. Dostańmy się do niego!

```sh
dive unknow/wywrotka # Zgarniamy hash sha256:4cbf6d0f4b1c9dc83277051f6c6244b7d828bdbecff86fbeecb099c81e5cb821
docker save unknow/wywrotka -o obraz.tar
mkdir obraz && tar xvf obraz.tar --directory=obraz
cd obraz/blobs/sha256
mkdir warstwa && tar xvf 4cbf6d0f4b1c9dc83277051f6c6244b7d828bdbecff86fbeecb099c81e5cb821 --directory=warstwa 
cd warstwa
ls # starter.sh
cat starter.sh
```

Widzimy zawartość pliku:

```sh

#!/bin/runner
fail() { echo "ERROR: $1"; rm $0; exit 1;}
cfg=/app/config
fix=$((2+2*2))

if [ ! -f $cfg ]; then
    fail "Brak pliku konfiguracyjnego"
fi

. $cfg

if [ -z "$version" ]; then
    fail "Brak definicji wersji oprogramowania"
fi

if [ $version -ne $fix ]; then
    fail "Wersja oprogramowania nie jest poprawna"
fi

echo "Wszystko dziala poprawnie"
echo "SUKCES!"
```

Czyli braktuje nam pliku konfiguracyjnego `/app/config`, jest on source'owany używając polecenia [. $cfg](https://ckziumragowo.pl/technik-informatyk/systemy/linux/bash-source). Ten plik powinien definiować wersję odpowiadającą zmiennej `fix`:

```sh
echo $((2+2*2))
6
```

dobra, stwórzmy sobie plik `config` na hoście:

```
echo version=6 > config
```

i podepnijmy go jako wolumin z danymi do kontenera:

```
docker run --rm -it -v ./config:/app/config unknow/wywrotka
Wszystko dziala poprawnie
SUKCES!
```

Sukces! Działa to dlatego, że `ENTRYPOINT` uruchamiane jest dopiero po zamontowaniu wszystkich woluminów oraz sieci.
