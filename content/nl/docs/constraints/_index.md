---
title: "Randvoorwaarden"
linkTitle: "Randvoorwaarden"
description: "Wat moet en kan er ingesteld worden om de applicatie te kunnen gebruiken?"
date: 2023-12-20
weight: 1
---

Om gebruik te maken van de cijferregistratieapplicatie moet er aan de volgende eisen zijn voldaan:
- Het vak moet in SIS, UvANose en Canvas ingericht zijn via de standaard koppeling tussen de systemen.
- Degene die cijfers invoert moet in Canvas als docent aan het vak zijn gekoppeld (of een andere rol met rechten om cijfers in Canvas in te voeren).
- Degene die cijfers inlevert moet in UvANose gekoppeld zijn als examinator op het vak of de groep.
- Degene die cijfers inlevert moet [SURF-2FA](https://medewerker.uva.nl/content-secured/az/tweestapsverificatie/surf/surf.html) hebben geactiveerd.

### Wijzigingen in systemen
Wijzigingen aan het vak in UvANose (bijv. nieuwe instanties, examinatoren) worden binnen een uur verwerkt in de CRA. Wijzigingen in GLASS (in/uitschrijven studenten) komen in real-time binnen. Een vak komt pas binnen in de CRA als het ook in GLASS staat; de data over groepen en studenten zou altijd 1-op-1 overeen moeten komen.

### Getoonde studenten
Alle studenten die voor het vak staan ingeschreven in GLASS worden getoond. Studenten die afgemeld zijn van een vak, verdwijnen van de lijst indien er geen eindcijfer is opgevoerd (anders blijven ze staan als handmatig toegevoegde studenten). Er wordt momenteel niet gekeken naar de status van de inschrijving voor de opleiding.

### Beoordelingsvoet
De mogelijke beoordelingen worden bepaald door de geldige rij met waarden van de beoordelingsvoet in SIS (bijv. HLF = halve cijfers, AN = AVV/NAV, DC1 = decimaal 1 cijfer). Cijfers tussen de 5 en 6 kunnen niet gegeven worden indien het vak een effective date voor 1 september 2018 heeft in SIS. Voor vakken met de NON-beoordelingsvoet is het niet mogelijk om cijfers in te leveren.

### Tentamendatum 
De toetsdatum wordt als volgt bepaald:
1.	De laatste datum van de geroosterde tentamenactiviteiten (eerste kans, types Tent en DigiToets) of hertentamenactiviteiten (tweede kans, types HerT en HertDigiToets) in TermTime gebruikt. Voor het tentamen geldt hier als uitzondering dat als er een college na het tentamen plaatsvindt (niet zijnde vragenuur, inzage of overig), de datum van de laatste activiteit wordt overgenomen.  
2.	Indien er geen geroosterd tentamen is, dan wordt de eerste (eerste kans) of laatste (tweede kans) dag van de laatste week van de periode (conform sessie op de studieactiviteit voor aanmeldingen) gebruikt (waarbij de gekozen toetsdatum nooit op de laatste dag van de maand valt). 

De toetsdatum is niet aanpasbaar door de docent, maar indien de toetsdatum in de toekomst ligt bij het indienen óf de toetsdatum van een herkansing voor de toetsdatum van de eerste poging ligt, dan wordt de datum van doorboeken gebruikt. In het scherm overzicht becijfering is het mogelijk om de tentamendatum aan te passen en daarmee de automatisch bepaalde waarde te overschrijven.

### Doorwerking naar SIS
Bij doorboeken worden de cijfers direct doorgezet naar SIS, in een proces dat op de achtergrond wordt gestart na het ondertekenen. Het proces biedt de cijfers aan SIS aan als inschrijvingsaanvragen, in batches van maximaal 100 cijfers. Hierbij wordt ook het UvAnetID van de examinator meegestuurd. De cijfers worden altijd op het Y-studiedeel geboekt. 

De tool maakt in principe een nieuwe Y-activiteit aan om de cijfers op te boeken, op basis van de periode van het vak (en dus niet de tentamendatum van het cijfer). De codering van de activiteiten is als volgt, waarbij XX het nummer van de instantie van het vak is (01, 02, etc.):
- CTXX voor de eerste kans
- CHXX voor het hertentamen
- CEXX voor een tweede hertentamen
- CL00 voor verlate cijfers

De studenten worden ingeschreven voor de studieactiviteit met een actieve loopbaan die overeenkomt met het niveau van de cursus, of met de eerste actieve loopbaan als deze niet bestaat.

Cijferlijsten die vanwege een fout of een openstaande goedkeuring niet direct (volledig) zijn doorgeboekt worden elke nacht opnieuw aan SIS aangeboden, totdat ze zijn verwerkt of afgevinkt op het [beheerscherm]({{< ref "../admin/_index.md" >}}).

### Partieel doorboeken
Er kan per vak ingesteld worden (met studiedeelkenmerk CVPA op de onderwijseenheid in SIS, te vullen vanuit UvANose) of de cijfers in delen ingeleverd kunnen worden. Als deze optie aanstaat, dan is het mogelijk om studenten aan te vinken en voor de selectie de cijfers door te voeren. Zo niet, dan moeten alle studenten een cijfer krijgen (bijv. een NAP). De docent heeft de mogelijkheid om alle overgebleven studenten in 1 keer een NAP te geven. 

### Configuratieopties per faculteit
Per faculteit (waarbij FMG telt als 4) kan ingesteld worden:
- Of het mogelijk is om studenten toe te voegen aan een cijferlijst
- Wat de einddatum is voor cijferregistratie (d.w.z. tot welke datum per academisch jaar docenten cijfers kunnen indienen). Let op: het is voor docenten nooit mogelijk om cijfers in te leveren in een vak van voor het laatst afgelopen academisch jaar.
- [Herinneringen](../admin/settings#herinneringsmails)

### Vrijstellingen
Het is momenteel niet mogelijk om vrijstellingen via de CRA te boeken; dit gebeurt direct in SIS en kan op een aparte Y-activiteit gedaan worden. Wanneer een student die een vrijstelling heeft gekregen toch voor het vak ingeschreven staat, dan levert dat geen problemen op indien de docent een NAV of NAP geeft. Het cijfer wordt dan geblokkeerd bij het doorboeken.

### Cijferblokkades
Via de cijferblokkade-optie in het admin settings dialoogje in het cijferscherm is het mogelijk om specifieke studenten uit te sluiten voor het vak. Docenten kunnen dan geen cijfers invoeren voor deze studenten: de student wordt wel getoond op het scherm maar invoer is niet mogelijk. De cijferlijst kan zonder deze studenten worden ingeleverd, ook wanneer partieel doorboeken uit staat.

### Tweede herkansing
Beheerders kunnen via een knop in het admin settings dialoogje in het cijferscherm voor een vak een tweede herkansing toevoegen, nadat er cijfers voor de eerste herkansing zijn ingeleverd. Deze tweede herkansing verschijnt als extra kolom in het cijferscherm en kan door de docent ingevuld worden. De tentamendatum wordt niet opgehaald, maar kan door een beheerder ingesteld worden. Cijfers worden verder verwerkt op dezelfde manier als een eerste herkansing.

### Bewaartermijnen
De tool bewaart alle ingeleverde cijfers minimaal 7 jaar en de volledig historie is op ieder moment terug te kijken.

### Activeren tool per vak
Het is mogelijk om de tool te deactiveren voor een vak in de beheersinstellingen:

![Beheersinstellingen](/course_setup.nl.png)

Het is dan niet voor docenten mogelijk om cijfers in te leveren. Datzelfde geldt voor vakken met beoordelingsvoet NON in SIS.

### Hulp bij problemen 
Problemen met de tool kunnen gemeld worden via de datanose-fnwi mailbox of via de TOPdesk behandelaarsgroep 'FNWI DataNose beheer'.
