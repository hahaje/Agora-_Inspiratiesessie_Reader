# Bijlage E: Code {#bijlage-e-code .unnumbered}

```Java
//variabelen om de gegevens van de appel in te bewaren.
float appelXPositie, appelYPositie, appelDiameter;

//variabelen om de gegevens van de held in te bewaren.
float heldXPositie, heldYPositie, heldDiameter;

//variabelen om de gegevens van het virus in te bewaren.
float virusXPositie, virusYPositie, virusDiameter;

//variabelen om de gegevens van de knop in te bewaren.
float knopX, knopY, knopBreedte, knopHoogte;

//variabelen om de gegevens van de afbeeldingen in te bewaren.
PImage held, virus, appel;

//variabelen om de stap die het virus zet richting held in te bewaren
float stapX, stapY;

//variabele om de score in te bewaren.
int score;

//variabele om de snelheid waarmee het virus beweegt in te bewaren.
int snelheid;

//variabele om het aantal verstreken milliseconden in te bewaren.
int vorigeVerstrekenMillis;

//variabele om de text grootte in te bewaren.
int textGrootte;

//variabele om de status van het spel in te bewaren: is het spel afgelopen? waar of niet-waar //(true/false)
boolean gameOver;

void setup() {
   size(400, 800); //Java modus

   //fullScreen(); //Android modus
   //orientation(PORTRAIT); //Android modus

   //plaatjes inladen
	held = loadImage("smiley.png");
	appel = loadImage("appel.png");
	virus = loadImage("corona.png");

	//grootte en startpositie van de appel
	appelDiameter = width/20;
	appelXPositie = random(appelDiameter/2, width - appelDiameter/2);
	appelYPositie = random(appelDiameter/2, height - appelDiameter/2);

	//grootte en startpositie van de held
	heldDiameter = width/8;
	heldXPositie = mouseX;
	heldYPositie = mouseY;

	//grootte en startpositie van het virus
	virusDiameter = width/13;
	virusXPositie = 100;
	virusYPositie = 100;

	//positie en formaat van de 'try again' knop

	knopX = width/2;
	knopY = height - height/8;

	knopBreedte = width / 3;
	knopHoogte = height / 20;

	//begin- score en snelheid
	score = 0;
	snelheid = 1;

	//variabele om te kunnen bepalen of er al weer een bepaalde tijd is verstreken.

	vorigeVerstrekenMillis = 0;

	//variabele waarin bijgehouden wordt of het gameOver is (true) of niet (false)
	//het spel begint natuurlijk met gameOver = false
	gameOver = false;

	//textgrootte hangt af va de breedte van het scherm.
	//Wanneer je het scherm groter maakt, wordt de tekst ook groter.
	textGrootte = width/8;

}

void draw() {
   background(0, 0, 0);

   //schrijf score
   fill(255, 255, 255);
   textSize(textGrootte);
   textAlign(LEFT);
   text("Score: " + score, 10, height/10 - 10);

   //teken held, eerst als cirkel, later als plaatje
   //fill(255, 255, 0);
   //circle(heldXPositie, heldYPositie, heldDiameter);
   imageMode(CENTER);
   image(held, heldXPositie, heldYPositie, heldDiameter, heldDiameter);

   //teken virus, eerst als cirkel, later als plaatje
   //fill(0, 255, 0);
   //circle(virusXPositie, virusYPositie, virusDiameter);
   imageMode(CENTER);
   image(virus, virusXPositie, virusYPositie, virusDiameter, virusDiameter);

   //teken appel, eerst als cirkel, later als plaatje
   //fill(255, 0, 0);
   //circle(appelXPositie, appelYPositie, appelDiameter);
   imageMode(CENTER);
   image(appel, appelXPositie, appelYPositie, appelDiameter, appelDiameter);

   if (gameOver == false) {
      //als held en appel botsen dan score + 1 en 'nieuwe' appel spawnen op willekeurige positie
      heldXPositie = mouseX;
      heldYPositie = mouseY;

      if (dist(heldXPositie, heldYPositie, appelXPositie, appelYPositie) <= (heldDiameter + appelDiameter)/2) {
         score = score + 1;
         appelXPositie = random(appelDiameter / 2, width - appelDiameter / 2);
         appelYPositie = random(appelDiameter / 2, height - appelDiameter / 2);
      }

      //het virus komt een stape dichterbij. Hier wordt bepaald hoe groot en in welke richting
      //de stap moet zijn
      stapX = (heldXPositie - virusXPositie) / dist(heldXPositie, heldYPositie, virusXPositie, virusYPositie);
      stapY = (heldYPositie - virusYPositie) / dist(heldXPositie, heldYPositie, virusXPositie, virusYPositie);

      virusXPositie = virusXPositie + snelheid * stapX;
      virusYPositie = virusYPositie + snelheid * stapY;

      //als er 2 seconden zijn verstreken, dan wordt de snelheid van het virus iets opgehoogd
      if (millis() - vorigeVerstrekenMillis > 2000) {
         snelheid = snelheid + 1;
         vorigeVerstrekenMillis = millis();
      }
   }

   //als de held botst met het virus, dan is het game over en wordt de \'try again\' knop getoond
   if (dist(heldXPositie, heldYPositie, virusXPositie, virusYPositie) <= (heldDiameter + virusDiameter)/2) {
      gameOver = true;

      //schrijf de tekst 'Game Over' in het midden van het scherm
      fill(255, 0, 0);
      textSize(textGrootte);
      textAlign(CENTER, CENTER);
      text("Game Over!", width / 2, height / 2);

      //teken de 'try again' knop
      fill(0, 255, 0);
      rectMode(CENTER);
      rect(knopX, knopY, knopBreedte, knopHoogte, 10);
      textAlign(CENTER, CENTER);
      textSize(knopBreedte / 5);
      fill(0);
      text("Try again", knopX, knopY);

      //als er op de knop wordt geklikt en als de muis op de knop staat,
      //dan wordt het spel opnieuw gestart.
      if (mousePressed == true) {
         if (mouseX > knopX - knopBreedte / 2 && mouseX < knopX + knopBreedte / 2 && 
             mouseY > knopY - knopHoogte / 2 && mouseY < knopY + knopHoogte / 2) {
             
            appelXPositie = random(appelDiameter / 2, width - appelDiameter / 2);
            appelYPositie = random(appelDiameter / 2, height - appelDiameter / 2);

            heldXPositie = mouseX;
            heldYPositie = mouseY;

            virusXPositie = 100;
            virusYPositie = 100;

            score = 0;
            snelheid = 1;
            vorigeVerstrekenMillis = 0;
            gameOver = false;
         }
      }
   }
}
```