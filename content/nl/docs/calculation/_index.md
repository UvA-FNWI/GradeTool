---
title: "Cijferberekening"
linkTitle: "Cijferberekening"
description: "Beschrijving van functionaliteit voor cijferberekening"
date: 2022-04-13
weight: 5
---
De handleiding van de cijferberekeningsfunctionaliteit is [op Canvas](https://canvas.uva.nl/courses/169/modules#module_103508) te vinden. Deze pagina beschrijft de werking van een aantal functionaliteiten.

### Berekeningsinstellingen
Cijferberekingen zijn in de regel gebaseerd op deelcijfers uit Canvas. Hier kan ruwweg met twee soorten beoordelingen gewerkt worden: punten (eventueel met een weergave als percentage of letter scale) of voldaan/niet voldaan. In beide gevallen kan het bijzondere cijfer EX (=excused) worden ingevoerd om een vrijstelling aan te geven.

De volgende berekeningstypes kunnen gebruikt worden:
- Gewogen gemiddelde: er dient per onderdeel een gewicht worden opgevoerd
- Som: de subonderdelen worden opgeteld zonder weging
- Laatste poging: het deelcijfer dat het laatste voorkomt in de ordening telt
- Maximum: het maximum van de deelcijfers telt 

Daarnaast kunnen per onderdeel een aantal opties ingesteld worden:
- Vereist: student krijgt een NAV (of NAP, indien geconfigureerd) indien er geen cijfer is vastgelegd voor dit onderdeel 
- Minimumcijfer: student krijgt een NAV (of het deelcijfer zelf, indien geconfigureerd) als niet aan de voorwaarde is voldaan
- Bonus/malus: het cijfer telt mee als bonus of malus

Voor een berekend cijfer met beoordeling voldaan/niet voldaan kunnen de 'vereist' en 'minimumcijfer' opties gebruikt worden om een berekende beoordeling in te stellen. Ook kan de optie om de laagste N cijfers te laten vallen hier ingezet worden om constructies te bouwen van de vorm "3 van de 4 opdrachten moeten gehaald zijn".

### Afronding
Cijfers kunnen in Canvas tot op maximaal twee decimalen nauwkeurig ingevoerd worden en worden ook op die manier in de berekening gebruikt. Intern rekent de taal met 7 decimalen voor berekende tussencijfers, in de weergave worden er altijd twee decimalen getoond. Eindcijfers worden afgerond volgens de in SIS ingesteld beoordelingsvoet, waarbij het in de resultaten per student wel mogelijk is om het onafgeronde eindcijfer te zien. 

### Koppelingen met toetssystemen
Naast assignments uit Canvas, biedt de tool de mogelijkheid om cijfers uit de toetssystemen ANS, SOWISO en TestVision te gebruiken. In alle gevallen dient eerst een koppeling door een beheerder gemaakt te worden in het beheervenster van het vak:

![Beheersinstellingen](/course_setup.nl.png)

Na koppelen kunnen toetsen uit de systemen worden toegevoegd via de 'bestaand onderdeel' optie. Voor ANS worden de cijfers automatisch binnengehaald bij berekening, voor SOWISO en TestVision is dit een aparte actie in het dropdownmenu cijferberekening. 

Voor de laatste twee systemen wordt niet alleen het cijfer van de toets zelf binnengehaald, maar ook van alle vragen. De cijferberekening uit het bronsysteem wordt dus niet gebruikt, maar er wordt een aparte cijferberekening gedaan. Hierbij wordt de kansscore bij MC-vragen op een standaardmanier meegewogen:

![Scoreberekening](/score_calc.nl.png)

Hier is "score" de score van de student en "punten" het totaal aantal te behalen punten.

### Kopiëren tussen jaren
Bij het openen van de tool voor een vak waarbij er nog geen cijferberekening is ingesteld, maar er wel een instantie bestaat in het vorige jaar met een berekening, biedt de tool aan om deze berekening te kopiëren. Hierbij worden de assignments uit Canvas gematcht op naam, dus dit werkt alleen als deze (nog) niet zijn aangepast. Onderdelen uit andere systemen worden momenteel niet gekopieerd.