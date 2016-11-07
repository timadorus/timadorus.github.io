---
title: "Ziele und Ausrichtung des Projekts Timadorus"
permalink: general_de_goals.html
sidebar: home_de_sidebar
lang: de
---

Timadorus ist darauf ausgerichtet Werkzeuge, Dienste sowie eine Umgbung zur Verbesserung der technischen Grundlage von MMORPGs zu schaffen. Um sich diesem, etwas hoch gesteckten, Ziel zu nähern  hat sich Timadrus eine Reihe von Aufgaben gestellt. Einige davon sind recht herausfordernd. Eine Umsetzung wird der Gegenstand einer langen Reihe von kleinen Schritten sein. Die letztendliche Vision ist eine MMORPG Plattform welche den gleichen Reichtum an möglichen Spielformen wie ein [Tischrollenspiel](https://de.wikipedia.org/wiki/Pen-%26-Paper-Rollenspiel) bietet.

Für Timadorus ist aber nicht nur das Endziel interessant, sondern auch der Weg um dorthin zu gelangen. Das Projekte wird als Lehrmittel, Forschungswerkzeug und -gegenstand zur Entwicklung von Software als Ingenieursdisziplin verwendet. Einzelheiten wie dies ereicht wird werden [hier][general_de_workflow] gegeben.

## Software für eine neue Art MMORPG ##

Timadorus will ein interesantes MMORPG werden; ein neues MMORPG; ein MMORPG das sich von existierenden Spielen abhebt, damit es nicht zu einer bloßen Kopie wird. Es verdankt seinem akademischen Wurzeln Fähigkeiten, die von Insidern der Spielindustrie als unmöglich bezeichnet wurden.

### Non-Stop ###
''Für Änderungen am Spiel darf es keine Unterbrechung des Dienstes geben''

Den Dienst jeden Mittwoch-morgen für zwei Stundne abzuschalten ist nicht länger akzeptabel. Egal ob es sich um geplante oder ungeplaten Abschaltungen handelt.

### Keinen Single-Point-of-Failure ###
''Es darf keine Komponente existieren deren Ausfall eine Unterbrechung des Dienstes bedeutet. Verschlechterungen müssen für die überwiegende Mehrheit der Benutzer akzeptabel sein und für alle vorübergehend.''

### Durchgängig ###
''Es darf keine Brüche im Spiel geben, welche die Immersion beinträchtigen. Außerdem darf es keine technische Einschränkngen der Interaktion geben, die für Spieler sichtbar sind.''

Dies bedeutet das es keine Realms, Shards, Zonen oder ähnliches geben kann, welches eine Abgrenzung der Spielerschaft zur Folge hätte. Natürlich können technische Aufteilungen notwendig sein. Aber diese müssen für den Benutzer vollkommen transparent sein.

### Skalierbar ###
Keine Komponente darf die Anzahl der gleichzeitigen Benutzer des Systems begrenzen. Egal ob sie technisch oder menschlich sind. Die Zielgröße für Timadorus im Vollausbau sind eine Million gleichzeitige Benutzer. Ebenso sollte dich räumliche Größe des Systems nicht begrenzt sein.


### Manipulationsbeständig ###

''Schummeln sollte so schwierig oder von so geringem Vorteil sein, das niemand einen relevanten Nutzen daraus ziehen kann. Schummeln sollte, wenn nicht unmöglich, wenigsten so schwierig das für Teilnehmer von mehr Vorteil ist, zur Gemeinschaft beizutragen als ihr zu schaden. Und wenn unerwünschte Manipulation nicht aufgehalten werden kann, dann sollte sie wenigstens Detektierbar sein.''

Kernpunkt dieser Diskussion für dieses Ziel ist Betrachtung war eigentlich Schummeln darstellt und was eine gekonnte Manipulation des Spieldesigns. Die Basis für weitere Gedanken ist die Philosophy das alles was möglich ist auch erlaubt sein sollte und alles das nicht erlaubt ist auch nicht möglich sein sollte.

Diese Anforderung ist ausschlaggebend um den Client des Spieles für externe Entwickler zu öffnen. Die meisten MMO Spiele benötigen strikte Kontrolle über den Client um ein Mindestmaß an anti-schummel Maßnahmen umsetzen zu können. Einige Anbieter machen den Netzwerkverkehr ihre Clients absichtlich schwer zu lesen oder verschlüsseln diesen sogar wirklich um Manipulationen zu erschweren. Dies führt lediglich zu einem Wettrüsten zwischen den Authoren von Manipulationswerkzeugen auf einer Seite und den Spieldienst Anbieter auf der anderen Seite, die versuchen dies zu entdecken und zu verhindern.


### Zukunftssicher ###

Es gibt wohl kaum ein Gebiet der Informatik das sich so schnell entwickelt wie die Qualität von Computer-ezeugten Bildern und 3D Welten. Entscheidungen die heute bezüglich akzeptabler Detailtreue für eine Darstellung in Echtzeit auf heutiger Hardware gemacht werden, können schon Monate später veraltet wirken.

Dies erfordert eine Erzeugung und Verwaltung von visuellen Resourcen die sich von heutigen Gewohnheit der Spieleindustrie unterscheidet, jedes Asset für jedes Produkt neu zu erschaffen. Stattdessen sollte Master-Modelle in der höchsten möglichen Detailierung erstellt werden. Prozesse, Methoden und Werkzeuge um diese automatisch in Assets für die Verwendung in Spielen herunterzurechnen müssen entwickelt und eingesetzt werden. Diese Prozesse sollten die minimal mögliche menschliche Einwirkung erfordern, diese aber unterstützen wenn notwendig oder gewünscht.

## Basisanforderungen ##

Natürlich müssen alle Anforderungen, die heute an ein MMORPG im Produktions-Einsatz gestellt werden auch von einem neuen erfüllt werden:

### Interaktiv ###

Das Spiel muss angemessen und zügig auf Eingaben des Anwenders reagieren. Während es eine Reihe von Techniken gibt um Serververzögerungen zu verstecken sollte das Spiel sich immer als gut ansprechbar anfühlen.

### Persistent ###

Auch wenn der Dienste nie unterbrochen werden sollte, muss es den vollständigen Weltzustand speichern auch wenn Clients die Verbindung abbrechen oder die Spielserver einzeln oder vollständig ausfallen.

Die Speicherung der Daten bietet auch die Möglichkeit der späteren Auswertung und Analyse, z.B. für E-Sport, Auswertung für Forschung, etc.

### Snap-Shots ###

Selbst wenn die Welt nicht angehalten wird, sollte es möglich sein Abzüge der Welt zu erzeugen um ein bestimmten Zustand für Analyse und Fehlersuche einzufrieren. Dies kann außerdem verwendet werden um alternative Spielwelten zu erzeugen.

{% include links.html %}
