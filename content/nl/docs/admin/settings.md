---
title: "Instellingen"
linkTitle: "Instellingen"
description: "Globale instellingen per afdeling en herinneringsmails voor niet-ingeleverde cijfers"
date: 2021-07-27
weight: 1
---

## Basisinstellingen

Op het scherm "Instellingen afdelingen" kunnen er globale instellingen worden gezet voor de cijferberekening. Momenteel zijn er twee instellingen:
- Einddatum: na deze datum is het voor docenten niet meer mogelijk om zelf cijfers in te leveren (medewerkers van de onderwijsadministratie die daartoe bevoegd zijn, kunnen dat wel)
- Studenten toevoegen uitschakelen: indien ingesteld is het niet mogelijk voor docenten om studenten toe te voegen aan de cijferlijst

De instellingen kunnen op elk niveau (instelling, faculteit of subafdeling) ingesteld worden. Er wordt altijd het laagste niveau gebruikt dat is ingesteld.

## Herinneringsmails
Op het scherm "Herinneringen instellen" kunnen per faculteit herinneringsmails geconfigureerd worden. De herinneringen worden vervolgens automatisch verstuurd in een dagelijks batchproces voor alle vakken waarvoor er minstens 1 student is die nog een cijfer moet krijgen. Er kunnen meerdere herinneringen ingesteld worden, met verschillende data. Per herinnering kan ingesteld worden

- Hoeveel dagen na de tentamendatum deze verstuurd wordt (of voor de tentamendatum, door een negatieve waarde in te vullen)
- De naam en email van de afzender
- Een optioneel adres waar een cc naar wordt gestuurd
- Het onderwerp en de inhoud van de mail

Bij het instellen van de inhoud kunnen er een aantal parameters gebruikt worden.

### Planning en selectie

Elke werkdag om 9 uur worden de mails uitgestuurd voor vakken waarbij er nog een cijfer openstaat en de betreffende mail niet eerder is gestuurd. Daarbij geldt:

- Individuele vakken en vakken met 0 EC worden niet meegenomen in de selectie
- De mail wordt verstuurd als de ijkdatum (tentamendatum plus het ingestelde aantal dagen) in het verleden ligt, maar niet meer dan 15 dagen, om te verhinderen dat er achterhaalde mails verstuurd worden bij het instellen van een nieuwe herinnering
- De mail gaat naar alle examinatoren die bij het vak betrokken zijn, ook al hebben zij misschien in hun eigen groep geen cijfers meer openstaan

De testknop op het configuratiescherm kan gebruikt worden om te kijken of er in de volgende run een mail verstuurd gaat worden voor een zeker vak.