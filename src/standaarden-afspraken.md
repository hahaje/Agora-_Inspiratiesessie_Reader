# Standaarden/ Afspraken

In de wereld van de programmeurs is het gebruikelijk om bepaalde standaarden af te spreken, hoe je code schrijft. Enkele afspraken zijn:

Variabelen worden in zogeheten camelCase geschreven. Dit betekent dat een naam van variabele altijd begint met een kleine letter en dat vervolgens ieder zelfstandig naamwoord in die naam begint met een hoofdletter, bijvoorbeeld

```java
int diameterCirkel;
float gespaardBedrag;
```

Ook is het belangrijk om duidelijke namen te kiezen, bij voorkeur namen die iets zeggen over de waarde die je erin stopt. Zoals bovenstaande voorbeelden.

Verder is het voor de leesbaarheid van je code belangrijk dat je af en toe wat lege regels toevoegt, na bijvoorbeeld een if-statement of voor en na de setup() en draw().

Voeg spaties toe na een komma, voor en na de "=", voor en na een wiskundige operator (b.v. "+"). Dit verhoogt ook de leesbaarheid van je code.

Code die heel compact geschreven is, dus zonder spaties en lege regels, is vaak moeilijker te lezen.

Een andere, belangrijke afspraak, die ook de leesbaarheid verhoogt, is het volgende. Na een "{" begin je de volgende regel met inspringen. Dat wil zeggen dat je een aantal spaties toevoegt vóór de regel, meestal 3.

Je hebt in deze reader daar al wel wat voorbeelden van gezien. Bijvoorbeeld bij de draw() en setup(), maar ook bij het if-statement.

```java
if ( conditie ) {
   statement1;
   statement2;
} else {
   statement3;
}
```

Zie je dat na een "}" de nieuwe regel begint met een aantal spaties?

Merk op dat bij een "}" er weer van voren af aan begonnen wordt met de regel.
