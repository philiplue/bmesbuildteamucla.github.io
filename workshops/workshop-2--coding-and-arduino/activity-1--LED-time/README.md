# [Workshop 2 - Coding and Arduino](https://bmesbuildteamucla.github.io/workshops/workshop-2--coding-and-arduino)

## Activity 1 - LED Time

### Task:
Turn the LED on after 5 seconds using a conditional statement. (Don’t use delay().)

### Circuit:
![Circuit](https://bmesbuildteamucla.github.io/workshops/workshop-2--coding-and-arduino/activity-1--LED-time/circuit.PNG)

### Code:
```c++
//Note: it is recommended to wire the circuit with a resistor in series with
//the LED to prevent the LED from burning out from too high of a current.

int led = 13; //makes it easier to remember which pin is used for what if you declare a variable for the pin

void setup()
{
  pinMode(led, OUTPUT); //label the pin as an output pin
  Serial.begin(9600); //begin the Serial monitor at a baud rate of 9600 bits per second
}

void loop()
{
  int time = millis(); //more flexible to use a variable and millis(), which is
  if (time >= 5000) {  //an integer that indicates time (in milliseconds) since the Arduino booted up
    digitalWrite(led, HIGH); //turns on the 13th digital pin
  }
}
```
