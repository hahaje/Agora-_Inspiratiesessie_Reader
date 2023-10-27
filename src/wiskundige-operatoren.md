# Wiskundige operatoren

In alle programmeertalen kun je ook wiskundige berekeningen uitvoeren. De belangrijkste voor nu zijn de onderstaande:

|Operator|Betekenis|
|---|:---|
|\+|optellen|
|\-|aftrekken|
|/|delen|
|\*|vermenigvuldigen|

Deze werken overigens alleen met getallen. Zo zal **println(10.2 + 3.5)** de volgende regel in de console printen:

**13.7**

Je kan natuurlijk ook berekening uitvoeren met variabelen, deze moeten dan wel van het type **int** of **float** zijn (er zijn nog meer standaard typen die getallen kunnen bevatten, maar die laten we even buiten beschouwing).

De volgende code:
```java
float getal1 = 10.2;
float getal2 = 3.2;
println(getal1 + getal2);
```

Levert dezelfde output op:

**13.7**

Zoals gezegd werk dit dus alleen met getallen. Een uitzondering is de + operator. Deze werkt ook op strings en variabelen van het type **String.** Het effect hiervan is dat de teksten die 'opgeteld' worden, als het ware aan elkaar 'geplakt' worden. Even een voorbeeld:

**println("Hello" + "World");**

levert als output in de console:

**HelloWorld**

Let op: Zoals je ziet zonder spatie!

Met variabelen, zou het als volgt eruit kunnen zien:

```java
String groet = "Hello";
String iedereen = "World";
println(groet + iedereen);
```

Dit levert dezelfde output op:

**HelloWorl**d

Wil je een spatie tussen de woorden dan zal je die zelf moeten toevoegen, bijvoorbeeld als volgt:

**println("Hello" + " " + "World");**

of

**println(groet + " " + iedereen);**

Dit werkt ook met combinaties van Strings en integer:

**println("Mijn leeftijd is: " + 13);**

levert op

**Mijn leeftijd is: 13**

Mooier is natuurlijk om dit behulp van een variabele te doen, dus:

```java
int leeftijd;
leeftijd = 13;
println("Mijn leeftijd is: " + leeftijd);
```

Dit levert dezelfde output op, maar is flexibeler in gebruik. Ik hoef dan alleen de waarde van de variabele **leeftijd** te wijzigen, om een andere zin te printen.
