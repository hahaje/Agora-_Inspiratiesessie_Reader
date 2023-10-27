# Android modus

Als je tevreden bent met het resultaat, wordt het tijd om te gaan kijken hoe het er uit ziet op je mobiel. Hiervoor moeten we een paar kleine aanpassingen in de code aanbrengen. In de **setup()** moet de **size(400,800)** weggehaald worden. Je kan dit doen door er commentaar van te maken door er // voor te zetten. Processing zal deze regels dan negeren.

In plaats hiervan zet je de volgende 2 regels in de setup();

```java
fullScreen();
orientation(PORTRAIT);
```

Save je programma en selecteer in de rechter bovenhoek de **Android** modus. Wanneer je nu over de 'play' button hoovert, zie je de tekst 'Run on device'. Sluit nu je mobiel aan op je laptop met je usb-kabel (Zorg dat je de ontwikkelaarsopties hebt aangezet, zie [Bijlage C](bijlage-c.md)). Als je nu op de play-button klikt, zal Processing je programma naar je telefoon sturen/installeren en starten.

Wanneer je de melding krijgt 'no device detected'. Zet dan, terwijl je mobiel aan je computer hangt, de ontwikkelaarsopties een keer uit en weer aan. Wellicht moet je dan ook nog op je mobiel toestemming geven aan je laptop om bestanden over te zetten.