---
title: "Cijferberekening"
linkTitle: "Cijferberekening"
description: "Beschrijving van functionaliteit voor cijferberekening"
date: 2021-03-21
weight: 5
---
De handleiding van de cijferberekeningsfunctionaliteit is [op Canvas](https://canvas.uva.nl/courses/169/modules#module_103508) te vinden. Deze pagina beschrijft de werking van een aantal functionaliteiten.

### Koppelingen met toetssystemen
Naast assignments uit Canvas, biedt de tool de mogelijkheid om cijfers uit de toetssystemen ANS, SOWISO en TestVision te gebruiken. In alle gevallen dient eerst een koppeling door een beheerder gemaakt te worden in het beheervenster van het vak:

![Beheersinstellingen](/course_setup.nl.png)

Na koppelen kunnen toetsen uit de systemen worden toegevoegd via de 'bestaand onderdeel' optie. Voor ANS worden de cijfers automatisch binnengehaald bij berekening, voor SOWISO en TestVision is dit een aparte actie in het dropdownmenu cijferberekening. 

Voor de laatste twee systemen wordt niet alleen het cijfer van de toets zelf binnengehaald, maar ook van alle vragen. De cijferberekening uit het bronsysteem wordt dus niet gebruikt, maar er wordt een aparte cijferberekening gedaan. Hierbij wordt de kansscore bij MC-vragen op een standaardmanier meegewogen:

![Scoreberekening](/score_calc.nl.png)

Hier is "score" de score van de student en "punten" het totaal aantal te behalen punten.

### Kopiëren tussen jaren
Bij het openen van de tool voor een vak waarbij er nog geen cijferberekening is ingesteld, maar er wel een instantie bestaat in het vorige jaar met een berekening, biedt de tool aan om deze berekening te kopiëren. Hierbij worden de assignments uit Canvas gematcht op naam, dus dit werkt alleen als deze (nog) niet zijn aangepast. Onderdelen uit andere systemen worden momenteel niet gekopieerd.