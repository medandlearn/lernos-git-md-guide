## Guide schreiben
### Vereinbarungen

### Howto: Ergänzen neuer Kapitel und Seiten
Im gewählten learn-theme von Hugo gibt es geneu zwei Ebenen, die Kapitelebene und die Pages-Ebene. Tiefer lässt sich die Textstruktur hier nicht verschachteln.

#### Ein neues Kapitel anlegen
```batch
$ hugo new --kind chapter week2/_index.md
```
Hierdurch wird automatisch die Seite für ein neues Kapitel erstellt.

```md
+++
title = "Week3"
date = 2020-11-03T21:24:17+01:00
weight = 4
chapter = true
pre = "<b> </b>"
+++

### Woche 3

# Wochenüberblick

Lorem Ipsum.
```
Mit weight wird die Position des Kapitels angegeben. Im MOment folgen die Wochen in direkter Reihenfolge. Falls wir hier Kapitel einschieben wollen, können wir hier umgewichten (z. B. in 5er- Schritten).
In den pre-Teag könnte man eine vorangestellte Kennzeichnung verwenden. Diese habe ich zunächst leer gelassen.

Title kann man anpassen, dieser erscheint auch als Navigationshinweis. 
Nach der Reihe +++ kann man den eigentlichen Inhalt der Seite editieren (Markdown).

#### Eine neue Seite anlegen
```batch
hugo new week3/kata.md
```
Dies erzeugt im Ordner week3 ein neues Markdown-Dokument mit folgendem Inhalt:
```md
---
title: "Kata"
date: 2020-11-04T09:54:27+01:00
draft: true
---

```
Auch hier lässt sich das Attribut weight verwenden um die Reihenfolge der Seiten innerhalb eines Kapitels zu steuern. Hier können wir uns auf eine passende Grundstruktur einigen. Nach dem Dateikopf (hinter den 3 Bindestrichen) wird wieder der Inhalt der Seite mit normalen MArkdown gestaltet. 

#### Besonderheiten
Um mit Mermaid Graphen erzeugen zu können, reicht eine Attributergänzung im Kopf einer Seite oder eines Kapitels.
```md
mermaid: true
```
Ein beispiel ist hier noch im Testbereich zu finden. [mermaid](content\create-content\teil_3.md)
