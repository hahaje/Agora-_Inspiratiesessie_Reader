# Variabelen

Een ander belangrijk bergrip in programmeren zijn variabelen. Soms heb je een bepaalde (berekende) waarde meer dan één keer nodig in je programma. In dat geval kun je -- i.p.v. die waarde steeds opnieuw te berekenen -- de waarde opslaan in een variabele en dan gewoon de naam van de variabele gebruiken. Technisch gezien is een variabele een plekje in het geheugen van de computer die je zelf een (duidelijke en logische) naam kunt geven en waar je vervolgens een waarde aan kunt geven, en deze waarde kun je vervolgens ook wijzigen. Om je daar een voorstelling van te kunnen maken, zou je een variabele kunnen zien als een doosje waar je een bepaalde waarde instopt en die je er ook weer uit kunt halen en zelfs wijzigen.

Een variabele maken, noemen we '**declareren**'. Je moet de computer laten weten hoe je variabele moet gaan heten. Een variabele een waarde geven noemen we **'initialiseren'**.

In veel programmeertalen moet je ook aangeven wat het zogeheten **type** van de variabele is. Is het een geheel getal, of een komma-getal, of een tekst? Dit zijn veel voorkomende types, maar je kunt ook variabelen maken die een plaatje kunnen bevatten.

De types die wij gaan gebruiken voor het spel zijn:

-   **int** hier kunnen gehele getallen (integers) in.

-   **float** voor komma-getallen.

-   **String** voor tekst.

> Let op: Processing is hoofdletter gevoelig, als je **Int** zou schrijven i.p.v. **int**, dan krijg je een foutmelding. **String** wordt, anders dan de andere types, met een hoofdletter geschreven. Dit is dus geen typefout. Waarom dit zo is, is op dit moment niet zo belangrijk.

-   **boolean** deze kan 2 waarden bevatten, **true** of **false** (waar of niet-waar).

> Een beetje een vreemde variabele misschien, maar deze is enorm handig in situaties, waarbij je afhankelijk van of iets waar of nietwaar is, iets wel of juist niet wil doen.

-   **Pimage** hier kun je plaatjes in opslaan.

Je kunt nu bijvoorbeeld een variabele **leeftijd** maken, waar je je leeftijd in op kan slaan (b.v. 13). Dit kun je als volgt doen:

**int leeftijd;** met deze regel declareer je de variabele

**leeftijd = 13;** hier geef je de variabele een waarde

Dit kan ook in 1 keer:

**int leeftijd = 13;**

In ons programma declareren we variabelen helemaal boven in het programma, boven de **void setup()**. In de **setup()** zelf geven we onze variabelen een start-waarde.

Dus bovenstaande variabele zouden we in ons programma als volgt kunnen definiëren en een waarde geven:

```java
int leeftijd;

void setup(){
   leeftijd = 13;
}
```

Naast standaard functies heeft Processing ook een aantal handige standaard variabelen. Degene die wij in ons spel gaan gebruiken zijn:

**width** hierin is de breedte van het venster opgeslagen

**height** hierin is de hoogte van het venster opgeslagen

**mouseX** hierin is de x-positie van de muis-cursor (pijltje) opgeslagen

**mouseY** hierin is de y-positie van de muis-cursor (pijltje) opgeslagen

**mousePressed** hierin is opgeslagen of je de linker muis knop hebt ingedrukt of niet. Deze heeft dus de waarde **true** (er is op de linker button geklikt) of **false** (er is niet geklikt).

Deze variabelen krijg je cadeau, en hoef je dus niet zelf te maken en dus ook niet bovenin je programma op te schrijven.
