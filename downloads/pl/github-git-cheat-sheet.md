---
layout: cheat-sheet
title: Ściąga z GitHub Git
byline: Git jest projektem open source rozproszonego systemu kontroli wersji. Ta ściąga to jest podsumowanie najważniejszych i najczęściej używanych komend w Git.
leadingpath: ../
---

{% capture colOne %}
## Instalacja Git-a
Dodatkowo GitHub dostarcza Ci desktopowego klienta który posiada interfejs graficzny z najbardziej popularnymi akcjami jakie możesz zrobić na repozytorium.

### GitHub na Windows
http://windows.github.com

### GitHub na Mac
http://mac.github.com

Dystrybucje Git-a na Linux oraz POSIX sa dostepne na oficjalnej stronie Git SCM.

### Git na wszystkie platformy
http://git-scm.com

## Konfiguracja narzędzia
Skonfiguruj informacje użytkownika dla wszystkich lokalnych repozytoriów

```$ git config --global user.name "[name]"```

Ustawia twoja nazwe, ktora bedzie dołączona podczas commita


```$ git config --global user.email "[email address]"```

Ustawia twój email który bedzie dołączony do commita


## Tworzenie repozytoriów
Tworzenie nowego repozytorium lub pobranie juz istniejącego


```$ git init [project-name]```

Tworzy nowe lokalne repozytorium, o danej nazwie


```$ git clone [url]```

Ściąga projekt który już istnieje, wraz z jego historią

{% endcapture %}
<div class="col-md-6">
{{ colOne | markdownify }}
</div>


{% capture colTwo %}

## Wprowadzanie zmian
Przeglądanie zmian oraz manipulacja commitem


```$ git status```

Lista wszystkich nowych lub zmodyfikowanych plików do zatwierdzenia


```$ git diff```

Pokazuje różnice zmian które nie zostały jeszcze zatwierdzone


```$ git add [file]```

Dodaje bieżący stan pliku do przygotowania wersjonowania


```$ git diff --staged```

Shows file differences between staging and the last file version


```$ git reset [file]```
Resetuje plik, ale zatrzymuje jego 


```$ git commit -m"[descriptive message]"```
Dodaje bieżący stan na stałe do histoerii wersji

## Zmiany grupowe Group changes
Name a series of commits and combine completed efforts


```$ git branch```

Wyświetla listę wszystkich lokanych gałęzi w aktualnym repozytorium


```$ git branch [branch-name]```

Tworzy nową gałąź o podanej nazwie


```$ git checkout [branch-name]```

Zmieniamy aktywną gałąź do tej podanej w nazwie, oraz uaktualnia robocze foldery


```$ git merge [branch-name]```
Scala historie zmian z podanej gałęzi do aktualnej gałęźi na której pracujemy 


```$ git branch -d [branch-name]```

Usuwa podaną gałąź

{% endcapture %}
<div class="col-md-6">
{{ colTwo | markdownify }}
</div>
<div class="clearfix"></div>

---

{% capture colThree %}
## Refaktoryzacja nazw plików Refactor file names
Zmiana oraz usuwanie wersjonowanych plików


```$ git rm [file]```

Usuwa plik z aktualnie roboczego folderu, oraz zatwierdza usunięcie


```$ git rm --cached [file]```

Usuwa pliki z kontroli wersji ale nie usuwa pliku lokalnie


```$ git mv [file-original] [file-renamed]```

Zmienia nazwe pliku oraz przygotowuje do zatwierdzenia

## Suppress tracking
Wyłanczanie tymczasowych plików oraz scieżek

```
*.log
build/
temp-*
```
Plik tekstowy o nazwie `.gitignore` 
A text file named `.gitignore` suppresses accidental versioning of files and paths matching the specified patterns


```$ git ls-files --other --ignored --exclude-standard```
Lista wszystkich zignorowanych plików w tym projekcie

## Cząstkowe zapisywanie
Trzymanie i odnawianie niedokończonych zmian


```$ git stash```

Tymczasowo zapisuje wszystkie śledzone zmodyfikowane pliki


```$ git stash pop```

Odzyska ostatnie schowane pliki (???)


```$ git stash list```

Lista wszystkich zmian


```$ git stash drop```

Odrzuca 
Discards the most recently stashed changeset
{% endcapture %}
<div class="col-md-6">
{{ colThree | markdownify }}
</div>

{% capture colFour %}
## Przeglądanie historii zmian
Przeglądanie oraz podglądanie jak ewoluowały nasze pliki w projekcie (????)


```$ git log```

Lista historii wersji aktualnej gałęźi


```$ git log --follow [file]```

Lista histoerii wersjii dla danego pliku, zawiera takze zmiany nazwy tego pliku 


```$ git diff [first-branch]...[second-branch]```

Pokazuje różnice zmian pomiedzy dwoma gałeźiami 


```$ git show [commit]```

Wyświetla metadane oraz treść zmian dla danej zmiany

## Cofnij zmiany

Wymaż błędy oraz praca nad zmianą historii


```$ git reset [commit]```

Cofnij wszystkie zmiany zaraz po `[commit]`, zatrzymuje wszystkie zmiany lokalnie


```$ git reset --hard [commit]```

Odrzuć całą historiie i zmiany do danej wersji, nie pozostawia zmian lokalnie

## Synchronizacja zmian
Zarejestruj zdalne reposytorium (URL), i synchronizuj historie zmian repozytorium


```$ git fetch [remote]```

Ściągnij całą historie zmian z zdalnego repozytorium


```$ git merge [remote]/[branch]```

Scal zdalną gałąź do aktualnej gałeźi w projekcie


```$ git push [remote] [branch]```

Wyślij wszystkie lokalne zmiany z gałęźi do GitHub-a


```$ git pull```

Ściągnij i scal historie oraz zmiany
{% endcapture %}
<div class="col-md-6">
{{ colFour | markdownify }}
</div>
