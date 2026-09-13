# 02-push-button-led
My 2nd Embedded Systems project-Control Led with push button

Project 2: Push Button LED Control

Description
This is my second embedded systems project where I controlled an LED using a push button — pressing the button turns the LED ON, and releasing it turns the LED OFF.

Hardware Used
 * Board: Arduino Uno
 * LED (Red)
 * Push Button
 * Resistor: 220 ohm (for LED)
 * Pull-down Resistor (for button)
 * Breadboard
 * Jumper wires

How It Works
The push button is connected to pin 2 and the LED to pin 12. When the button is pressed, a HIGH signal is received on pin 2, which turns the LED ON. Releasing the button changes the signal to LOW, turning the LED OFF.

Code:

​```cpp

int buttonPin = 2;
int ledPin = 12;
int buttonState = 0;

void setup() {
  pinMode(ledPin, OUTPUT);
  pinMode(buttonPin, INPUT);
}

void loop() {
  buttonState = digitalRead(buttonPin);
  
  if (buttonState == HIGH) {
    digitalWrite(ledPin, HIGH); 
  } else {
    digitalWrite(ledPin, LOW);   
  }
}

```

Demo Video (https://youtu.be/0y8Jxy8abOY?si=4VabWjSVQsWfRlsm)

 * How digital input pins work
 * Using the digitalRead() function
 * The concept of pull-down resistor circuits
 * Conditional logic (if/else) in embedded code
