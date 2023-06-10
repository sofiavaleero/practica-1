# PRACTICA 1: BLINK

L'objectiu de la pràctica és entendre algunes funcions bàsiques d'Arduino: el setup i loop, sortides per terminal o l'assignació i utilització de pins.

```cpp 
#include <Arduino.h>
#define PIN 16

void setup() {
  Serial.begin(115200);
  pinMode(PIN, OUTPUT);
}

void loop() {
  digitalWrite(PIN, HIGH);
  Serial.println("ON");
  delay(500);
  digitalWrite(PIN, LOW);
  Serial.println("OFF");
  delay(500);
}
```
Primer hem definit el pin pel led 

#define PIN 16

a continuació declarem el setup() amb les funcions:

  Serial.begin(115200);
  pinMode(PIN, OUTPUT);

on definim que el codi s'executarà una vegada i el mode del pin com a pin de sortida

Finalment en el loop (bucle) duem a terme el que volem que fagi el programa:

digitalWrite(PIN, HIGH);
  Serial.println("ON");
  delay(500);

La primera linia de codi assignarà al pin un valor alt, el que farà encendre el led que hi tenim conectat. Per poder fer un seguiment sense necessitat del led farem apareixer per pantalla "ON" quan el led estigui encés. Posteriorment el programa esperarà mig segon (500 ms) abans d'executar les següents linies de codi:

  digitalWrite(PIN, LOW);
  Serial.println("OFF");
  delay(500);

Seguidament s'assigna un valor baix al pin. El que farà que el led deixi de romandre encés. Novament es mostrarà un missatge per pantalla: "OFF". Finalment el programa tornarà a esperar 500ms per continuar. Un cop acabat el delay es tornarà a executar el loop desde el principi.

## SORTIDA PEL TERMINAL

<img src="terminal1.png" width="480" align="center">

## DIAGRAMA DE TEMPS

<img src="diagrama1.png" width="480" align="center">
