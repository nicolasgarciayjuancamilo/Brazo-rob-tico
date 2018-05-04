# Brazo-rob-tico

#include <Servo.h>

int a=1;
float ba=90, iz=90, de=90, ga=90;

#define pinBas 12
#define pinIzq 11
#define pinDer 10
#define pinGarra 9

#define Bases 90
#define Garras 100
#define Izqu 90
#define Dere 90

Servo Base;
Servo Izquierda;
Servo Derecha;
Servo Garra;

void setup() {
  Base.attach(pinBas);
  Izquierda.attach(pinIzq);
  Derecha.attach(pinDer);
  Garra.attach(pinGarra);
}

void loop() {
   Base.write(Bases+10);
  delay(500);
  Garra.write(Garras+30);
  delay(500);
  Base.write(Bases-10);
  delay(500);
  Garra.write(Garras-30);
  delay(500);
  Izquierda.write(Izqu+10);
  delay(500);
  Derecha.write(Dere+10);
  delay(500);
  Izquierda.write(Izqu-10);
  delay(500);
  Derecha.write(Dere-10);
  delay(500);
  Base.write(Bases-30);
  delay(500);
  Base.write(Bases-10);
  delay(500);
}
