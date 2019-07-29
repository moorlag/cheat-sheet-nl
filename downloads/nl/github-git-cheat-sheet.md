---
layout: cheat-sheet
redirect_to: false
title: GitHub Git Spiekbriefje
byline: Git is de open source versiecontrole systeem. Dit spiekbriefje vat de Git-opdrachtregelinstructies samen, veel plezier!
leadingpath: ../../../
---

{% capture colOne %}
## Git installieren
GitHub biedt desktop-clients met een grafische gebruikersinterface voor de meest voorkomende acties op repositories, evenals een automatisch bijgewerkte command prompt van Git voor geavanceerde scenario's.
### GitHub voor Windows
http://windows.github.com

### GitHub voor Mac
http://mac.github.com

Git-Distributionen für Linux- und POSIX-Systeme sind auf der offiziellen Git SCM-Webseite verfügbar.

### Git voor alle andere Plattformen
http://git-scm.com

## Tool configureren
Configuratie van gebruikersinformatie voor alle lokale repositories

```$ git config --global user.name "[name]"```

Stelt de naam in die u wilt toevoegen aan uw commits

```$ git config --global user.email "[email address]"```

Stel het e-mailadres in dat u wilt toevoegen aan uw commits

## Repositories anlegen
Maak een nieuwe repository of download een van een bestaande URL

```$ git init [project-name]```

Maak een nieuwe lokale repository met een gedefinieerde naam

```$ git clone [url]```

Dupliceert een project en laadt de versiegeschiedenis in.

{% endcapture %}
<div class="col-md-6">
{{ colOne | markdownify }}
</div>


{% capture colTwo %}

## Veranderingen voorbereiden
Veranderingen controleren en een commit in concept voorbereiden

```$ git status```

Verzamel alle veranderingen nieuwe en veranderde data voor een commit.

```$ git diff```

Laat zien welke verschillen tussen work space en staging area.

```$ git add [file]```

Voeg een bestand toe aan je staging area.

```$ git diff --staged```

Laat zien welke verschillen er zijn tussen de staging area en de repo.

```$ git reset [file]```

Unstage een bestand met behoud van de wijzigingen in de work space.

```$ git commit -m"[descriptive message]"```

Commit je staged inhoud als een nieuwe commit snapshot.

## Branch & Merge
Werk in branches isoleren, context veranderen en veranderingen integreren.

```$ git branch```

Toon alle branches. Aan het sterretje (*) zie je welke branch actief is.

```$ git branch [branch-name]```

Maak een nieuwe branch

```$ git checkout [branch-name]```

Verander van branch en open de work space.

```$ git merge [branch-name]```

Mergde een specifieke branch geschiedenis in de huidige branch.


```$ git branch -d [branch-name]```

Verwijder een branch
{% endcapture %}
<div class="col-md-6">
{{ colTwo | markdownify }}
</div>
<div class="clearfix"></div>

{% capture colThree %}
## Refactor namen
Verwijder en verplaats bestnaden.

```$ git rm [file]```

Verwijder het bestand en indexeert deze verwijdering.

```$ git rm --cached [file]```

Entfernt die Datei aus der Versionskontrolle, behält sie jedoch lokal
Verwijder het bestand uit de versiecontrole, maar behoudt het in de lokale workspace.

```$ git mv [file-original] [file-renamed]```

Ändert den Namen der Datei und bereitet diese für den Commit vor
Verander de naam van het bestand en bereidt deze voor om te comitten.

## Tracking tijdelijk uitschakelen
Tijdelijk bestanden en adressen van uitsluiten

```
*.log
build/
temp-*
```

Eine Textdatei namens `.gitignore` verhindert das versehentliche Committen von Dateien und Pfaden mit den spezifizierten Patterns


```$ git ls-files --others --ignored --exclude-standard```

Listet alle innerhalb dieses Projekts ignorierten Dateien auf

## Fragmente speichern
Aufschieben und Wiederherstellen unvollständiger Änderungen


```$ git stash```

Speichert temporär alle getrackten Dateien mit Änderungen


```$ git stash pop```

Stellt die zuletzt zwischengespeicherten Dateien wieder her


```$ git stash list```

Listet alle zwischengespeicherten Änderungen auf


```$ git stash drop```

Verwirft die zuletzt zwischengespeicherten Änderungen
{% endcapture %}
<div class="col-md-6">
{{ colThree | markdownify }}
</div>

{% capture colFour %}
## Historie überprüfen
Durchsuchen und Inspizieren der Evolution von Projektdateien


```$ git log```

Listet die Versionshistorie für den aktuellen Branch auf


```$ git log --follow [file]```

Listet die Versionshistorie für die aktuelle Datei auf, inklusive Umbenennungen


```$ git diff [first-branch]...[second-branch]```

Zeigt die inhaltlichen Unterschiede zwischen zwei Branches


```$ git show [commit]```

Gibt die Änderungen an Inhalt und Metadaten durch den angegebenen Commit aus

## Commits wiederholen
Fehler beseitigen und die Historie bereinigen


```$ git reset [commit]```

Macht alle Commits nach `[commit]` rückgängig, erhält die Änderungen aber lokal


```$ git reset --hard [commit]```

Verwirft die Historie und Änderungen seit dem angegebenen Commit

## Änderungen synchronisieren
Registrieren eines externen Repositories (URL) und Tauschen der Repository-Historie


```$ git fetch [remote]```

Downloadt de totale geschiedenis van een externe repository

```$ git merge [remote]/[branch]```

Intergreert de externe branch in de actuele lokale branch.

```$ git push [remote] [branch]```

Push alle commits van de lokale branch naar GitHub.

```$ git pull```

Pullt de geschiedenis van een externe repository en combineert de veranderingen.
Pullt die Historie vom externen Repository und integriert die Änderungen
{% endcapture %}
<div class="col-md-6">
{{ colFour | markdownify }}
</div>
