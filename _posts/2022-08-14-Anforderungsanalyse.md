---
layout: post
title:  "Anforderungsanalyse"
date:   2022-08-14 23:49:09 +0200
categories: project update
---
## Versuchsraum 4

Vor der eigentlichen Anforderungsanalyse ist es natürlich wichtig, sich ersteinemal im klaren zu sein, was der Untersuchungsgegenstand ist. In unserem Falle ist dies der Versuchsraum-4 (VR-4) der Universität Regensburg.
VR-4 befindet sich in der TechBase und ist in drei Bereiche aufgeteilt.

![Laborübersicht](/assets/2022-08-14-lab.jpg)

1. Labor
Hier befinden sich hauptsächlich Arbeitsbereiche für Studierende, Dozierende und Labornutzer:innen für ihre jeweiligen Projekte (Bachelor-, Master-, Forschungsarbeiten o.ä.).
2. Werkstatt
Mit einer Ausstattung von Lötkolben, 3D-Drucker und vielen Hardware-Teilen, ist die Werkstatt sehr gut geeignet für verschiedene Hardwareprojekte.
3. Studio
Das Studio wird hauptsächlich für Virtual-Reality-Studien benutzt. Mit Hilfe von Motion-Capturing-Kameras und leistungsstarken Computern, können hier VR-Projekte durchgeführt werden.

## Nutzergruppen VR-4

Durch eigene Erfahrung und erstem Beobachten im Labor, konnten wir folgende Nutzergruppen feststellen:
- Studierende
- Betreuer:innen
- SHKs

Diese Nutzergruppen konnten wir zunächst durch uns vorliegende Bachelorarbeiten über das VR-4 und auch später durch die Experteninterviews validieren.

## Interviews
 
Wir haben zwei verschiedene Interviewarten durchgeführt. Zum einen semi-strukturierte Interviews mit den Expert:innen des VR-4 und andererseits eine Online-Umfrage der Nutzer:innen der letzen Monate. 

### Online-Umfrage

Wir haben die Nutzer:innen des VR-4 Labors der letzten Monate durch eine Mailingliste benachrichtigt. Die Meisten nutzten ausschließlich das Studio. 

Die Umfrage haben wir in verschiedene Bereiche geteilt: Übersichtlichkeit (Belegungsplan, etc.), Interaktion bezüglich VR-4, Arbeiten im Labor, Ablauf der Reservierung.
Die Zufriedenheit in diesen Bereichen konnte auf einer Likert-Skala zwischen 1 (=gar nicht zufrieden) und 5 (=sehr zufrieden) beantwortet und anschließend mit offenen Kommentaren weiter ausgeführt werden.

Die Ergebnisse der Umfrage ergab, dass die Abläufe bezüglich des Labors bereits gut ablaufen. Da der Reservierungsplan zwischenzeitlich erneuert wurde, sind in der Umfrage Zufriedenheit und Antworten u.a. noch mit dem alten System zusammenhängend.

![Onlineumfrage-Ergebnis](/assets/2022-08-14-umfrage_ergebnis.jpg)

### Experteninterviews

Die Experteninterviews wurden mit Betreunde und SHKs des Labors durchgeführt. Es war semi-strukturiert, damit wir bei interessanten Themen eigens noch näher nachfragen konnten.
Es wurden Fragen zum Aufgabenfeld und der Labornutzung gestellt, sowie wie nach Expertenmeinung Tätigkeiten und Interaktionen mit Objekten konkret unterstützt werden können.
Ebenfalls haben wir uns nach typischen Nutzergruppen des Labors erkundigt und konnten auch mit den Experteninterviews unsere Einteilung der Nutzergruppen validieren.
Anschließend gab es ein fiktives Szenario zur kreativen Anregung. Hier haben wir die Situation erfunden, dass extrem viel Geld dem Labor zur Verfügung steht und man jegliches Inventar einkaufen könnte.
Abschließend konnten die Interviewpartner noch eigene Themen ansprechen, die noch nicht im Interview genannt wurden.

Für die Auswertung haben wir die Interviews transkribiert, wichtige Stellen markiert und anschließend codiert. 
Dabei konnten wir 8 Codegruppen feststellen:
1. Tutorials / FAQs
2. Inventarupgrade
3. Inventarliste
4. Tracking von Nutzern
5. Buchunsgsystem
6. Community
7. Demos / Vorführbarkeit
8. IOT

![Laborübersicht](/assets/2022-08-14-Codes.jpg)

## Ergebnisse

Die weitere Auswertung haben wir unter diesen Codegruppen fortgeführt und bestehende Probleme mit möglichen Lösungen gegenübergestellt.

### Tutorials / FAQs
Leichtgewichtiges Frontend als Voraussetzung. Eine übersichtliche virtuelle Einführung in das Labor.

- Viele Studierende benötigen angepasste *Tutorials* für die Handhabung von Laborequipment
- Sichtbare Projekte sollten einsehbar transparent dokumentiert sein (z.B. *Information zu Ausstellungsstücken oder Poster*)
- *Laborregeln* sollten immer und jederzeit einsehbar sein und möglichst im Vordergrund stehen

### Community
Neuorganisation der Kommunikation durch ein Chatinterface. Hier kann auch auf bereits bestehende Systeme zurückgegriffen werden.

- Eine transparente und *offene Kommunikation* unter Labornutzenden ist wünschenswert
- Eine *Chatgruppe* für die Labore würde die Flexibilität der Buchungen verbessern
- Damit eine Übersicht gewährleistet ist, sollte eine *zentrale Liste* exisitieren, in der man *Schäden von Laborequipment* aufnehmen kann

### IOT
Hardwarelastiges Projekt, welches ein zentrales Steuersystem zur Laborautomatisierung voraussetzt.

- Beamer und Laptops sollten über unterschiedliche Dockingstatons über eine *HDMI-Matrix* miteinander verbunden werden können
- Eine drahtlose HDMI-Schnittstelle (z.B. *Chromecast*) ist möglich
- Gut platzierte LED Strips sollen die Atmosphäre bei Laborführungen verbessern oder farblich angeben, ob gerade eine Studie stattfindet. Zuzüglich sollte auch die Studienatmosphäre verbessert werden. (*Moodlighting*)
- Es ist erwünscht den *Belegungsplan* im Raum zu *visualisieren*

### Tracking
Möglichst niedrigschwelliges, aber verpflichtend bzw. automatisches System Nutzende im Labor zu tracken

- Eine *Ein- und Abmeldung* von Labornutzer:innen ist zum administrativen Protokollieren von Vorteil


## Zeitplan / Nächste Schritte

*Anfang August - Mitte August*
Baseline für die Sub-Projekte (Frameworks, Software-Environments, etc.)

*ab Mitte August*
Start der Sub-Projekte (Hardware und/oder Software-Projekte)

![Laborübersicht](/assets/2022-08-14-zeitplan.jpg)
