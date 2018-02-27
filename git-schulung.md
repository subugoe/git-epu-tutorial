

Git EPU Schulung
========================================================
author: Najko Jahn
date: 28.2.2018
autosize: true

Motivation
========================================================

<div align="center">
<img src="http://www.phdcomics.com/comics/archive/phd101212s.gif"></img>
</div>

Motivation
========================================================

<div align="center">
<img src="http://media.springernature.com/full/springer-static/image/art%3A10.1186%2F1751-0473-8-7/MediaObjects/13029_2013_Article_88_Fig3_HTML.jpg"></img>
</div>
 
Ram, K., 2013. Git can facilitate greater reproducibility and increased transparency in science. Source Code for Biology and Medicine, 8(1), p.7. Available at: <http://dx.doi.org/10.1186/1751-0473-8-7>.

Anwendungsfälle:

- Lab notebook
- Facilitating collaboration
- Backup and failsafe against data loss
- Mechanism to solicit feedback and reviews 
- Lowering barriers to reuse


Git Repository initiieren
========================================================


```bash
git init my_git_repo
```

- `my_git_repo` Platzhalter für Name des Ordners mit dem Git Repository
- `git init .` initiiert Repository im aktuellen Verzeichnis
- Git sichert alle Änderungen im Unterordner `.git`

Aufgabe: Iniitiert ein Git Repository mit dem Namen `spielwiese`

Zeige den Stand des Git-Repositories
========================================================


```bash
cd spielwiese
git status
```

Mit `git status` kannst du Änderungen am Repository nachverfolgen

Füge eine Textdatei hinzu
========================================================

Erstelle oder kopiere eine Textdatei in dein Repository. Nutze dafür den Editor deiner Wahl, z.B. Atom, Sublime oder Notepad

```bash
sublime hallo.txt
```

**Aufgabe: Wie lautet nun der Status deines Repositories?**

Dateien zu Git hinzufügen
========================================================

Dateien mit Git zu versionieren, bedarf zweierlei 

1. `git add dateiname`
2. `git commit -m "bedeutungsvolle nachricht"`

Git erkennt Dateien in deinem Repository. So kannst du Git befehlen, die Datei nachzuverfolgen:


```bash
git add hallo.txt
```

Um Git zu sagen, dass es dauerhaft eine Version speichern soll:


```bash
git commit -m "ich habe mit der einleitung begonnen"
```

**Aufgabe: Fügt Eure Datei zu Git hinzu und lasst euch anschließend den Status anzeigen**

Versionierung
==========================================================

**Aufgabe: Ändert Eure Datei und fügt die aktualisierte Version zu Git hinzu**

Tipp:


```bash
git add -u
```

Dokumentiert nur Änderungen bei Dateien, die Git bereits nachverfolgt. Ihr müsst also nicht mehr den Dateinamen angeben

**Führt anschließend `git log` aus. Was erkennt ihr?**

Versionierung: Was passiert?
===========================================================

![](https://swcarpentry.github.io/git-novice/fig/git-staging-area.svg)

Funktioniert auch mit mehreren Dateien auf einmal:

![](https://swcarpentry.github.io/git-novice/fig/git-committing.svg)

**Aufgabe: Fügt eine weitere Datei zu Git hinzu und versioniert diese!**

Wie kann ich auf meine Versionen zurückgreifen?
============================================================


```bash
git diff 6ad274c1de8cd9e60aa7e8fb65cac17649c95951 hallo.txt
```

Tipp: Git Services wie GitHub haben viel schönere Möglichkeiten, durch die Versionsgeschichte zu browsen!

**Aufgabe: Fügt eine Zeile zur Textdatei hinzu und gebt anschließend `git diff hallo.txt`ein. Was passiert?**

Wie kann ich dezentral an meinem Git Repo arbeiten
============================================================

Git Server wie GitLab der GWDG oder GitHub bieten die Möglichkeit, Repositories in der Cloud zu speichern. Achtung, GitHub macht bei Default alle Repositories öffentlich, private nur im gegen Bezahlung möglich.

Für SUB Arbeiten bietet sich daher der Gitlab-Server der GWDG an:

<https://gitlab.gwdg.de/>

Aufgabe: Meldet euch bei GitLab mit euer GWDG Kennung an und legt ein neues Repository an!

Repositories über GitLab teilen
============================================================

Fügt Metadaten hinzu

```
git config --global user.name "Najko"
git config --global user.email "najko.jahn@sub.uni-goettingen.de"
```

URL hinzufügen und zwar unter dem Namen `origin`

```
git remote add origin https://gitlab.gwdg.de/jahn34/dddd.git
```

Änderungen hinzufügen:

```
git push -u origin master
```

Änderungen in das Repository zurückholen

```
git pull origin master
```

Git Repositories lokal nachnutzen
============================================================

```
git clone [URL zu Git Repository]
```

**Aufgabe: Erstellt eine lokale Kopie des Open APC Repositories**

Recap
===========================================================

```
# initiieren oder clonen
git init mein_repo 
cd mein_repo
git remote add origin URL zu Git Repo

# dateien bearbeiten und versionieren
git add meine_dateien
git commit -m "ich habe folgende dinge gemacht, weil"

# repository auf webserver speichern
git push origin master

# daten vom websever holen
git pull origin master
```

Tools
===========================================================

- CLI tig
- Desktop Clients für GitHub <https://desktop.github.com/>
- Git Integration Editoren und IDEs (Sublime, Atom, RStudio)

Weitere Schritte
============================================================

Kollaboratives bearbeiten von Git Repositories:

- Arbeiten mit Branches
- Pull Requests
- Beseitigen von Mergekonflikten

GitHub als Open-Science-Publiaktionsumgebung

### weitere Infos 
Spickzettel:

- <https://education.github.com/git-cheat-sheet-education.pdf>

Tutorials:

- <https://swcarpentry.github.io/git-novice/>

Bei Problemen, Najko fragen!
