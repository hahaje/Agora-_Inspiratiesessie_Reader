# Uitwerking

De code vind je in [bijlage E](bijlage-e.md).

Zorg ervoor dat je plaatjes in een directory staan met de naam ***data.***

Let op: dit is een mogelijke uitwerking en niet persé de enige juiste uitwerking. Sterker zelfs, ik denk dat als ik het nog een keer zou uitwerken, het er dan hoogstwaarschijnlijk anders zou hebben uitgezien: andere namen, andere volgorde etc. Dat is heel gebruikelijk als je programmeert. Je probeert continu je code steeds 'beter' te maken: duidelijkere namen, makkelijker aan te passen/ uit te breiden etc.

## Android modus

Als je tevreden bent met het resultaat, wordt het tijd om te gaan kijken hoe het er uit ziet op je mobiel. Hiervoor moeten we een paar kleine aanpassingen in de code aanbrengen. In de **setup()** moet de **size(400,800)** weggehaald worden. Je kan dit doen door er commentaar van te maken door er // voor te zetten. Processing zal deze regels dan negeren.

In plaats hiervan zet je de volgende 2 regels in de setup();

```java
fullScreen();
orientation(PORTRAIT);
```

Save je programma en selecteer in de rechter bovenhoek de **Android** modus. Wanneer je nu over de 'play' button hoovert, zie je de tekst 'Run on device'. Sluit nu je mobiel aan op je laptop met je usb-kabel (Zorg dat je de ontwikkelaarsopties hebt aangezet, zie [Bijlage C](bijlage-c.md)). Als je nu op de play-button klikt, zal Processing je programma naar je telefoon sturen/installeren en starten.

Wanneer je de melding krijgt 'no device detected'. Zet dan, terwijl je mobiel aan je computer hangt, de ontwikkelaarsopties een keer uit en weer aan. Wellicht moet je dan ook nog op je mobiel toestemming geven aan je laptop om bestanden over te zetten.


## Gebruikte plaatjes

![image21](images/image21.png)

![image22](images/image22.png)

![image23](images/image23.png)


## Aanvullingen/uitdagingen

1.  Zorg dat de held altijd **helemaal** binnen het scherm blijft.

2.  Hou een highscore bij:

    a.  Zet de highscore in de regel met de score

    b.  Voor het bewaren en ophalen van de highscore kun je gebruik maken van de *loadStrings()* en *saveStrings()* functies van Processing

3.  Maak van het spawnen van de appel een functie spawnAppel(), en gebruik deze 2 keer, in plaats van de gecopieerde code.

4.  Zelfde geldt voor het instellen van de variabelen bij de start van het spel (in de setup()) en bij het drukken op de "Try again" button. Maak hiervoor een functie initialiseerSpel() en roep deze op de 2 betreffende plaatsen aan.
