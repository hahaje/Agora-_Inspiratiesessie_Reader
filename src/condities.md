# Condities

Vaak wil je pas iets uitvoeren als er aan een bepaalde voorwaarde (conditie) is voldoen. Processing heeft hiervoor het **if**-statement.

De syntax (schrijfwijze) hiervan is:

```java
if ( conditie ) {
   statement1;
   statement2;
   //etc...
}
```

Let hier op de () en {}, deze zijn verplicht!

Je kan deze if lezen als: **ALS** conditie waar is **DAN** voer de statements uit.

Een voorbeeld. Stel ik heb een spel waarin de speler een aantal levens heeft. Als deze op zijn dan is het spel voorbij en wordt er "Game Over" in het midden van het scherm geprint. Het aantal levens hou ik bij in een variabele met de naam **aantalLevens**.

Dan zou ik het bovenstaande als volgt kunnen programmeren:

```java
if (aantalLevens == 0) {
   text("Game Over", width / 2, height / 2);
}
```

Let op de dubbele ==, dit kun je lezen als 'is gelijk aan'. In tegenstelling tot de enkele =, die gebruikt wordt om een 'waarde toe te kennen' aan een variabele.

De volgende vergelijkingen zijn beschikbaar:

|Vergelijking|Betekenis|
|---|:---|
|==|is gelijk aan|
|\<|is kleiner dan|
|\>|is groter dan|
|\<=|is kleiner of gelijk|
|\>=|is groter of gelijk|
|!=|is ongelijk aan (de ! kun je lezen als 'is niet')|

Ook is het mogelijk om het if-statement uit te breiden met wat er zou moeten gebeuren als niet aan de conditie is voldaan.

```java
if ( conditie ) {
   statement1;
   statement2;
} else {
   statement3;
}
```

Dit kan je lezen als: **ALS** conditie waar is **DAN** voer de statement1 en statement2 uit **ANDERS** voer statement3 uit.

Als je meerdere condities hebt die moeten gelden, kun je deze 'koppelen' door er && (en) tussen te zetten of \|\| (of). De '\|' zit op je toetsenbord, rechts, boven de Enter toets.

```java
if (conditie1 && conditie2){
   statement1;
}
```

Dit kun je lezen als: **ALS** conditie1 **EN** conditie2 waar zijn **DAN** voer statement1 uit.

```java
if (conditie1 || conditie2){
   statement1;
}
```

Dit kun je lezen als: **ALS** conditie1 **OF** conditie2 waar is **DAN** voer statement1 uit.
