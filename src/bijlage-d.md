# Bijlage D: Processing Reference {#bijlage-d-processing-reference .unnumbered}

Hier vindt je de Nederlandse vertaling van enkele Processing functies uit de Processing Reference ([Reference / Processing.org]).

## setup()

**Beschrijving**

> De functie setup() wordt eenmalig uitgevoerd wanneer het programma wordt gestart. Het wordt gebruikt om initiële eigenschappen zoals schermgrootte te definiëren en om media zoals afbeeldingen en lettertypen te laden wanneer het programma wordt gestart. Er kan slechts één functie setup() zijn voor elk programma. setup() wordt automatisch aangeroepen en mag nooit expliciet worden aangeroepen.
>
> Als de schets een andere dimensie heeft dan de standaardinstelling, moet de functie size() of de functie fullScreen() de eerste regel in setup() zijn.
>
> Opmerking: Variabelen die zijn gedeclareerd in setup() zijn niet toegankelijk binnen andere functies, waaronder draw().

**Syntax**

> setup()

**Retourneert**

> void

## draw()

**Beschrijving**

> Wordt direct na de setup() aangeroepen en voert continu de coderegels in het blok uit totdat het programma wordt gestopt of noLoop() wordt aangeroepen. draw() wordt automatisch aangeroepen en mag nooit expliciet worden aangeroepen. Het scherm wordt pas ververst nadat alle coderegels in de draw() zijn uitgevoerd.
>
> Het aantal keren dat draw() in elke seconde wordt uitgevoerd, kan worden geregeld met de functie frameRate().
>
> Het is gebruikelijk om background() aan te roepen aan het begin van de draw() lus om de inhoud van het venster te wissen. Het weglaten van background() kan onbedoelde resultaten opleveren, zoals afbeeldingen de blijven staan en waar vervolgens overheen getekend wordt.
>
> Er kan slechts één draw() -functie zijn voor elke programma en draw() moet bestaan als u wilt dat de code continu wordt uitgevoerd of als je gebeurtenissen zoals mousePressed() wilt verwerken. Soms heb je een lege draw() functie nodig om te tekenen in je programma, zoals onderstaand voorbeeld. In dit voorbeeld wordt er bij elke muisklik een cirkel, met diameter 50, getekend op de plek waar er geklikt is.


```java
void setup() {
   size(200, 200);
}

// Ondanks dat de draw() hier leeg is, is die wel nodig, zodat het programma
// user input kan verwerken (muiskliks in dit geval).

void draw() {

}

void mousePressed() {
   circle(mouseX, mouseY, 50);
}
```

**Syntax**

> draw()

**Retourneert**

void

\<\<Under construction\>\>
