---
title: "Randvoorwaarden"
linkTitle: "Randvoorwaarden"
description: "Wat moet en kan er ingesteld worden om de applicatie te kunnen gebruiken?"
date: 2021-04-23
weight: 1
---

Om gebruik te maken van de cijferregistratieapplicatie moet er aan de volgende eisen zijn voldaan:
- Het vak moet in SIS en Canvas ingericht zijn via de standaard koppeling tussen de twee systemen.
- Degene die cijfers invoert moet in Canvas als docent aan het vak zijn gekoppeld (of een andere rol met rechten om cijfers in Canvas in te voeren).
- Degene die cijfers inlevert moet in SIS gekoppeld zijn als examinator op de studieactiviteit van de werkvorm.
- Degene die cijfers inlevert moet [SURF-2FA](https://medewerker.uva.nl/content-secured/az/tweestapsverificatie/surf/surf.html) hebben geactiveerd.

### Activeren tool per vak
In de huidige pilotsituatie moet de tool per vak aangezet worden voordat de 'Cijfers inleveren' knop voor docenten actief is. Deze tijdelijke optie is voor een (Canvas-)beheerder beschikbaar via de beheersinstellingen per vak in de tool zelf:

![Beheersinstellingen](/course_setup.nl.png)

### Recente wijzigingen in SIS
De cijferregistratieapplicatie wordt minimaal elke nacht bijgewerkt met wijzigingen vanuit SIS. Als een vak recenter dan dat is aangemaakt, dan kan het zijn het vak nog niet bekend is en dat de melding "course not found" wordt getoond bij het openen van de tool. Het is mogelijk om vanaf dat foutscherm een update vanuit SIS te triggeren, door op "Update course from SIS" te klikken en de SIS course ID op te geven. Alle gegevens van het vak worden dan in real-time vanuit SIS binnengehaald.

Hetzelfde geldt voor wijzigingen in het vak die op de dag zelf zijn gedaan (bijv. een aanpassing in de studieactiviteit) of het inschrijven van een student, deze kunnen door iemand met beheerdersrechten in Canvas worden binnengehaald via de "Gegevens bijwerken" knop in de cijfertool:

![Gegevens bijwerken](/update_data.nl.png)

### Getoonde studenten
Alle studenten die voor het vak staan ingeschreven op een studieactiviteit op de werkvorm worden getoond. Er wordt niet gekeken naar inschrijven op studieactiviteiten in een T- of H-sessie. Studenten die waarvan de vakaanmelding wordt gestopt, verdwijnen van de lijst indien er geen eindcijfer is opgevoerd (anders blijven ze staan als handmatig toegevoegde studenten). Er wordt niet gekeken naar de status van de inschrijving de opleiding.

### Beoordelingsvoet
De mogelijke beoordelingen worden bepaald door de geldige rij met waarden van de beoordelingsvoet in SIS. Cijfers tussen de 5 en 6 kunnen niet gegeven worden indien het vak een effective date voor 1 september 2018 heeft in SIS.

### Tentamendatum 
De toetsdatum wordt als volgt bepaalt (zie ook [de flowchart](/flowchart_toetsdatum.pdf)):
1.	Indien er een T-studieactiviteit bestaat (T of S sessie voor eerste kans, H sessie voor tweede kans) en hier een einddatum is ingericht, dan wordt deze gebruikt (`CLASS_MTG_PAT.END_DT`). Bij meerdere studieactiviteiten wordt de laatste einddatum gebruikt. NB: het scherm in SIS toont hier altijd een datum, maar dat betekent niet dat er ook een datum is opgeslagen.
2.	Zo niet, dan wordt de laatste datum van geroosterde tentamenactiviteiten (eerste kans, types Tent en DigiToets) of hertentamenactiviteiten (tweede kans, types HerT en HertDigiToets) in Syllabus+ gebruikt.
3.	Indien deze niet bestaat, dan wordt de eerste (eerste kans) of laatste (tweede kans) dag van de laatste week van de periode (conform sessie op de studieactiviteit voor aanmeldingen) gebruikt (waarbij de gekozen toetsdatum nooit op de laatste dag van de maand valt). 

De toetsdatum is niet aanpasbaar door de docent, maar indien de toetsdatum in de toekomst ligt bij het indienen óf de toetsdatum van een herkansing voor de toetsdatum van de eerste poging ligt, dan wordt de datum van doorboeken gebruikt. De data uit SIS wordt 1 keer per dag bijgewerkt (en kan met de "[update data](#recente-wijzigingen-in-sis)" knop worden bespoedigd), informatie uit het rooster komt in real-time binnen.

### Doorwerking naar SIS
Bij doorboeken worden de cijfers direct doorgezet naar SIS, in een proces dat op de achtergrond wordt gestart na het ondertekenen. Het proces biedt de cijfers aan SIS aan als inschrijvingsaanvragen, in batches van maximaal 100 cijfers. Hierbij wordt ook het UvAnetID van de examinator meegestuurd. De cijfers worden altijd op een T-studiedeel geboekt, tenzij het een individueel vak betreft. Als er geen T-studiedeel bestaat voor een niet-individueel vak, dan kunnen er momenteel geen cijfers worden geboekt. 

De tool zoekt eerst (via een QAS-query) een bestaande T-activiteit (standaard of herkansing) om de cijfers op te boeken, op basis van de sessie van het vak en de eventueel geselecteerd werkgroep. Indien deze niet bestaat, dan maakt de tool de activiteit aan via de component interface van SIS met een zo specifiek mogelijke sessie (bijv. T21 i.p.v. T2). In beide gevallen hoeven er geen studenten in SIS ingeschreven te worden; de tool doet dit bij het boeken van de cijfers. Indien een student al ingeschreven staat, wordt de bestaande inschrijving gebruikt. Zo niet, dan wordt de student ingeschreven met een actieve loopbaan die overeenkomt met het niveau van de cursus, of met de eerste actieve loopbaan als deze niet bestaat.

Cijferlijsten die vanwege een fout of een openstaande goedkeuring niet direct (volledig) zijn doorgeboekt worden elke nacht opnieuw aan SIS aangeboden, totdat ze zijn verwerkt of afgevinkt op het [beheerscherm]({{< ref "../admin/_index.md" >}}).

### Partieel doorboeken
Er kan per vak ingesteld worden (met studiedeelkenmerk CVPA op de onderwijseenheid in SIS, te vullen vanuit UvANose) of de cijfers in delen ingeleverd kunnen worden. Als deze optie aanstaat, dan is het mogelijk om studenten aan te vinken en voor de selectie de cijfers door te voeren. Zo niet, dan moeten alle studenten een cijfer krijgen (bijv. een NAP). De docent heeft de mogelijkheid om alle overgebleven studenten in 1 keer een NAP te geven. 

### Configuratieopties per faculteit
Per faculteit (waarbij FMG telt als 4) kan ingesteld worden:
- Of het mogelijk is om studenten toe te voegen aan een cijferlijst
- Wat de einddatum is voor cijferregistratie (d.w.z. tot welke datum per academisch jaar docenten cijfers kunnen indienen)
- [Herinneringen](../admin/reminders)

### Bewaartermijnen
De tool bewaart alle ingeleverde cijfers minimaal 7 jaar en de volledig historie is op ieder moment terug te kijken. 

### Hulp bij problemen 
Problemen met de tool kunnen gemeld worden via de datanose-fnwi mailbox of via de TOPdesk behandelaarsgroep 'FNWI DataNose beheer'.