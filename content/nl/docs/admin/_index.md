---
title: "Beheerschermen"
linkTitle: "Beheerschermen"
description: "Overzicht van de werking van de beheersschermen voor onderwijsadministraties"
date: 2021-07-30
weight: 4
---

De beheerschermen voor de cijferregistratie zijn momenteel toegankelijk via https://datanose.nl (of https://acc.datanose.nl voor de testomgeving). Er zijn twee hoofdschermen: een scherm ‘Openstaande cijferlijsten’ om lijsten met niet-ingeschreven studenten af te handelen en een overzichtsscherm ‘Overzicht cijferlijsten’. Daarnaast zijn er een aantal ondersteunende schermen en is er ook voor elk vak een overzichtsscherm beschikbaar. 

### Rollen
Er zijn een aantal verschillende rollen die aan gebruikers toegekend kunnen worden binnen de beheerschermen:
- Facultair beheerder: kan rollen toekennen/weghalen en globale instellingen zetten
- Cijferbeheerder (UvA): heeft toegang tot alle cijferschermen, kan cijfers goedkeuren en doorboeken, reminders instellen en data aanpassen
- Cijferbeheerder (alleen lezen): heeft toegang tot alle cijferschermen maar kan niets aanpassen
- Cijferinleveraar: kan namens iedere examinator cijfers inleveren en doorboeken
- Latecorrectiegoedkeurder: heeft toegang tot het overzicht correcties en kan laat ingediende correcties goed of afkeuren
- Medewerker VU-cijferverwerking: kan studenten opzoeken en VU-cijfers binnenhalen

### Overzicht cijferlijsten

![Overzicht cijferlijsten](/grade_overview.nl.png)

Dit scherm toont alle ingediende cijferlijsten, in drie categorieën: 
- Ingevoerd: ingeleverd door de docent, maar nog niet ondertekend.
- Doorgeboekt: ondertekend, maar nog niet (volledig) in SIS verwerkt.
- Afgehandeld: in SIS verwerkt of afgevinkt.

Onder doorgeboekt of afgehandeld worden de volgende statussen getoond:
- ![warning](/error.png): de lijst heeft openstaande fouten (indien de fout is dat de student niet is ingeschreven, dan is het icoon grijs, anders geel).
- ![tick](/tick.png): lijst is succesvol verwerkt.
- ![cog](/cog.png): lijst moet (deels) nog verwerkt worden.

Je kunt doorklikken naar het vak of de cijferlijst direct openen via het ![page](/page.png)-icoontje, waarna de detailpagina opent. 

Ook kunnen deze lijsten in het overzicht worden afgevinkt om ze naar ‘afgehandeld’ te verplaatsen, ook al staan nog niet alle cijfers in SIS door in het overzichtsscherm een vink te zetten. Na op 'vernieuwen' klikken is de lijst verdwenen uit het overzicht van openstaande lijsten.

### Details cijferlijst

Voor cijferlijsten die nog niet volledig in SIS zijn verwerkt is het mogelijk om de tentamendatum aan te passen en de lijst direct naar SIS door te boeken:

![Instellingen cijferlijst](/list_info.nl.png)

Let op: als de cijferlijst al deels is doorgeboekt en je past daarna de toetsdatum aan dan komt de nieuwe toetsdatum mee met alle daarna doorgeboekte cijfers. In SIS bestaan dus verschillende toetsdata voor dit vak.

Per cijfer zie je de verwerkingsstatus, met een mouseover met meer informatie (bijv. in het geval van een fout wat er precies fout is gegaan). Er worden een aantal standaardfouten getoond:
- Kan geen studieactiviteit aanmaken. Het is niet mogelijk om de benodigde T-activiteit aan te maken, bijv. doordat het studiedeel op inactief staat.
- Student heeft geen actieve inschrijving. De student is niet actief voor inschrijving in de betreffende periode.
- De tentamendatum valt buiten de sessie. De opgegeven tentamendatum komt niet overeen met de sessie van het vak.

Overige (onverwachte) fouten worden als 'onbekende fout' getoond; door de cijferlijst nogmaals te laten verwerken kun je zien wat er precies foutgaat. Op deze fouten wordt actief gemonitord door centraal beheer.

### Openstaande cijferlijsten

Dit scherm is qua opzet vergelijkbaar met het overzicht, maar toont alleen de cijferlijsten waarvoor er nog een of meer niet-ingeschreven studenten of na 40 dagen corrigeerde studenten beoordeeld moeten worden:

![Openstaand cijfer](/list_other_row.png)

Via de knoppen aan het einde van de rij kan het cijfer geaccepteerd (wordt in de nacht naar SIS doorgezet) of afgewezen (met reden, geen verdere actie) worden.

### Overzicht correcties

Dit scherm toont alle ingediende correcties, met een aantal extra kolommen die meer inzicht geven in de ernst van de correctie:
- Aantal gecorrigeerde cijfers
- Aantal weken na indienen van het oorspronkelijke cijfer
- Aantal cijfers dat van voldoende naar onvoldoende is gecorrigeerd
- Reden correctie

Verder worden dezelfde statussen getoond als in de andere lijsten en kan er doorgeklikt worden naar de details van de lijst.

### Overzicht becijfering
Dit scherm toont alle relevante vakken voor een faculteit, met de huidige status van de becijfering. De tentamendata worden getoond, en ook de data waarop er cijfers zijn ingeleverd (indien dit het geval is). Het is mogelijk om op een vak door te klikken om te zien wat voor reminders er zijn verstuurd, welke groepen er zijn en welke examinatoren daaraan zijn gekoppeld.

### Informatie per vak
Door naar een vak door te klikken of via de zoekfunctie rechtsboven een vak op te zoeken op naam of studiegidsnummer en dan naar ‘Cijfers inleveren’ te gaan, kom je op de overzichtspagina per vak. Hier zie je alle ingeleverde lijsten met status: 

![Openstaand cijfer](/course_lists.nl.png)

Daarnaast kun je via de optie ‘Alle cijfers tonen’ een overzicht inzien van alle ingeleverde cijfers voor dit vak in het gekozen jaar.