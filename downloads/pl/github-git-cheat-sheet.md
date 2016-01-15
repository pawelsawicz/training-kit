---
layout: cheat-sheet
title: Ściąga z GitHub Git
byline: Git jest projektem open source rozproszonego systemu kontroli wersji. Ta ściąga to jest podsumowanie najważniejszych i najczęściej używanych komend w Git.
leadingpath: ../
---

{% capture colOne %}
## Instalacja Git-a
Dodatkowo Github posiada aplikacje desktopowa z interfejsem graficzny z najbardziej popularnymi akcjami jakie możesz zrobić na repozytorium.

### GitHub na Windows
http://windows.github.com

### GitHub na Mac
http://mac.github.com

Dystrybucje Git-a na Linux oraz POSIX są dostępne na oficjalnej stronie Git SCM.

### Git na wszystkie platformy
http://git-scm.com

## Konfiguracja narzędzia
Konfiguruje informacje użytkownika dla wszystkich lokalnych repozytoriów

```$ git config --global user.name "[name]"```

Ustawia nazwę, która będzie dołączona podczas zatwierdzenia


```$ git config --global user.email "[email address]"```

Ustawia adres email, który będzie dołączony podczas zatwierdzenia


## Tworzenie repozytoriów
Tworzy nowe repozytorium lub pobiera już istniejące


```$ git init [project-name]```

Tworzy nowe lokalne repozytorium o danej nazwie


```$ git clone [url]```

Ściąga projekt który już istnieje, wraz z jego historią

{% endcapture %}
<div class="col-md-6">
{{ colOne | markdownify }}
</div>


{% capture colTwo %}

## Wprowadzanie zmian
Przeglądanie zmian oraz manipulacja zatwierdzeniem


```$ git status```

Lista wszystkich nowych lub zmodyfikowanych plików do zatwierdzenia


```$ git diff```

Pokazuje różnice zmian które nie zostały jeszcze zatwierdzone


```$ git add [file]```

Dodaje bieżący stan pliku do wersjonowania


```$ git diff --staged```

Pokazuje różnice zmian plików pomiedzy zatwierdzonymi do wersjonowania a ich ostatnią historią


```$ git reset [file]```
Resetuje plik z zatwierdzenia, ale zatrzymuje jego zawartość


```$ git commit -m"[descriptive message]"```
Dodaje bieżący stan na stałe do historii wersji wraz z wiadomością

## Zmiany grupowe

Name a series of commits and combine completed efforts


```$ git branch```

Wyświetla listę wszystkich lokanych gałęzi w aktualnym repozytorium


```$ git branch [branch-name]```

Tworzy nową gałąź o podanej nazwie


```$ git checkout [branch-name]```

Zmienia aktywną gałąź na podaną w nazwie, oraz uaktualnia robocze foldery


```$ git merge [branch-name]```

Scala historie zmian gałęzi do aktualnej gałęzi na której pracujemy


```$ git branch -d [branch-name]```

Usuwa podaną gałąź
{% endcapture %}
<div class="col-md-6">
{{ colTwo | markdownify }}
</div>
<div class="clearfix"></div>

---

{% capture colThree %}
## Refaktoryzacja nazw plików
Zmiana oraz usuwanie wersjonowanych plików


```$ git rm [file]```

Usuwa plik z aktualnie roboczego folderu, oraz zatwierdza usunięcie


```$ git rm --cached [file]```

Usuwa pliki z kontroli wersji ale nie usuwa pliku lokalnie


```$ git mv [file-original] [file-renamed]```

Zmienia nazwe pliku oraz przygotowuje do zatwierdzenia

## Wyłączenie śledzeń
Wyłącza śledzenie tymczasowych plików oraz scieżek

```
*.log
build/
temp-*
```

Plik tekstowy o nazwie `.gitignore` wstrzymuje przed przypadkowym wersjonowaniem plików oraz ścieżek które pasują do podanego wzorca


```$ git ls-files --other --ignored --exclude-standard```

Lista wszystkich zignorowanych plików w tym projekcie

## Cząstkowe zapisywanie
Trzymanie i odnawianie niedokończonych zmian


```$ git stash```

Tymczasowo przetrzymuje wszystkie śledzone pliki które zostały zmodyfikowane do schowka


```$ git stash pop```

Odzyskuje ostatnie pliki które są przechowywane w schowku


```$ git stash list```

Lista wszystkich przetrzymywanych zmian w schowku


```$ git stash drop```

Odrzuca, usuwa ostatnie zmiany które są przechowywane w schowku 
{% endcapture %}
<div class="col-md-6">
{{ colThree | markdownify }}
</div>

{% capture colFour %}
## Przeglądanie historii zmian
Przeglądanie oraz sprawdzanie ewolucji naszego projektu


```$ git log```

Lista historii wersji aktualnej gałęzi


```$ git log --follow [file]```

Lista historii wersji dla danego pliku, zawiera takze zmiany nazwy tego pliku


```$ git diff [first-branch]...[second-branch]```

Pokazuje różnice zmian pomiedzy dwoma gałęziami


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