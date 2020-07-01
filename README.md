# git-readme
git readme
# Git

Git ist eine Versionskontrollsoftware, die einem dabei hilft, seine Programmier- und Latex-Projekte zu organisieren und zu backupen und die Zusammenarbeit mehrerer Menschen am selben Projekt erleichtert.

Die Idee ist folgende: Wann immer man eine Änderung an seinem Code gemacht hat, die man für speichernswert hält, macht man einen Snapshot (commit genannt) und kann dann in alle Ewigkeit auf diesen Zustand zurückgreifen.
 
Eine umfassende Einführung findet man in dem exzellenten Buch

    https://git-scm.com/book/en/v2

Hier soll eine kurze Einführung für die Arbeit in der Arbeitsgruppe gegeben werden.


### Arbeiten mit git

Nehmen wir an, du hast ein Programmierprojekt, das am Ende die Dateien

    readme.txt

    cool_program1.m

    cool_program2.m

enthalten soll, aber noch hast du nichts programmiert. Zunächst erstellst du ein Repository auf einem Server, den du von überall erreichen kannst. Etwa auf Github.


#### Erklärung von Git

Der folgende Abschnitt ist nur für das Verständnis und kann der Verwendung von Sourcetree übersprungen werden. Bei Sourcetree sind alle Befehle durch Buttons ausführbar.


Nun musst du das (leere) Repository herunterladen mit 

    git clone url-des-Repositorys-auf-dem-Server

Wenn man ein Repo(sitory) klont, kopiert man es sich auf den eigenen Rechner und sagt git, dass das Repo auf dem Server das Hauptrepository ist.

Jetzt kannst du anfangen zu Programmieren. Du legst die Datei `readme.txt` an. Leider musst du nun weg und möchtest deinen Status sichern. Dafür musst du deine bisherige Arbeit vormerken mit

    git add readme.txt

Jetzt ist `readme.txt` in der sogenannten staging area. Um sie nun tatsächlich zu speichern und für alle Ewigkeit in dieser Version abrufbar zu machen, musst du die Staging area nun commiten:

    git commit

Git wird dich nach einer commit-Message fragen, die beschreiben sollte, was du verändert hast. Zur Sicherheit solltest du am Ende eines Tages deine Änderungen auch auf den Server schieben. Dies geschieht mit

    git push

Das hat zwei Vorteile: Einerseits sind deine Daten dann auch sicher, sollte dein Computer abbrennen. Andererseits kannst du nun von jedem anderen Ort, der den Server erreicht, weiterarbeiten.

Sagen wir, du bist nun woanders. Du musst dir das Repo also in der aktuellen Version herunterladen. Das hast du schon mal mit clone gemacht. Dein lokales Repository weiß schon, wo sein Haupt-Repo liegt. In diesem Fall holst du dir die Änderungen mit

    git pull

Nun kannst du (etwa auf deinem Laptop) weiterarbeiten und am Ende alle Änderungen vormerken (`git add *`) und dann commiten (`git commit`). Dann liegen sie in deinem lokalen Verzeichnis und du bringst sie wieder auf den Server mit `git push`.



