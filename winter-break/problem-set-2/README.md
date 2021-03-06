# Winter Break Problem Set

Before you start this problem set, please make sure that you can successfully complete all of the activities from [Workshop 2 - Coding and Arduino](https://bmesbuildteamucla.github.io/Workshops/Workshop%202%20-%20Coding%20and%20Arduino/README.md). The solutions to those activities can be found at the bottom of the page for your reference. Even if you are super confident about these activities, please read through the solutions and make sure you understand everything.

These five problems are more complex than the ones we did in workshop and will help you practice your skills. Try your best to use your current knowledge to solve them. Do not hesitate to message any of us for help.

Do each problem in a separate TinkerCAD circuit. When you finish,  email [bmes.build.team@gmail.com](mailto:bmes.build.team@gmail.com) with the TinkerCAD share link (found at the top right of the page) for each problem. Please make your circuits organized enough so we can see the connections.

## Problems:

#### Problem 1 - Traffic Light
* You are setting up a new traffic light for the De Neve crosswalk. You want to give both the pedestrians and the drivers the power to change the light at the press of a button. Let’s assume that people don’t press the button unless they need to (so a pedestrian doesn’t stop to push the button if he or she can already cross).

* Set up a circuit with a green, yellow, and red LED like a standard traffic light. Initially the red LED will be on. When the button is pressed the first time (we assume by a driver), the light will turn green and stay green until the button is pressed again. When the button is pressed next (this time by a pedestrian), transition the LEDs from green to red. This involves turning the yellow LED on for 5 seconds before the red LED is turned on. Further button presses will continue this pattern. Construct a circuit and Arduino code that will accomplish this task. 

  - *Note: Assume that the button will only be pressed when it is not in a transition state (i.e. when the yellow LED is on). This means you can use delay().*

#### Problem 2 - LED Game
* You’re bored and decide to make a game for your friends. In this game, you have 5 LEDs that each have their own button. The LEDs are set up in a row. When an LED’s button is pressed, its state changes (meaning if it was on, it turns off, and vice versa). It will also change the state of the two LEDs next to it. For example, if the button for the 4th LED is pressed, the 3rd, 4th, and 5th LED would change states. If the button for the 1st or 5th LED is pressed, the state change wraps around. For example, if the 5th button is pressed, the 4th, 5th, and 1st LED change states. The objective of the game is to figure out what sequence of button presses turns all of the LEDs on.

* Construct this circuit and corresponding Arduino code for the game. Additionally, comment the correct sequence of button presses at the bottom of the code (you can insert a comment using // in Arduino).

  - *Hint: Use arrays!!*

#### Problem 3 - Save Energy...Save the World
* As New Year’s Day quickly approaches, you decide to be more aware of your energy usage. The first area you focus on is your light usage. You want to know how long an LED has been on. If it has been on for longer than 20 seconds, it will automatically turn off.

* Implement this system using a light switch button and LED. When you press the button once, the LED turns on. The LED will either turn off when the button is pressed again or turn off automatically after 20 seconds. When the LED turns off, you want to print the following message to the Serial Monitor: `“The LED was on for [number of seconds LED was on] seconds.”`

#### Problem 4 - Newton’s Luminescent Cradle
* You are a hot shot at a big time company because of all the experience you got from Build Team. You need some trinkets for your desk, but you want them to be unique. You really like the trinket called Newton’s Cradle, but being the hot shot you are, the physical device is trivial. You decide to make a Newton’s cradle made of LEDs instead.

* In its resting state an LED on the end of a line of 5 LEDs is illuminated. When a button is pressed and released, analogous to pulling back one of the balls on a normal Newton’s Cradle and releasing it, the “light” bounces to each LED and goes back and forth across the 5 LEDs. However, you want it to be very similar to a normal Newton’s Cradle and the bouncing stops at some point. Have the “bouncing” of light slow down and eventually stop on one of the LEDs on the end. You can assume that the button will only be pressed if the light is not “bouncing”.

  - *Hint: It will be much easier if you store your leds pins in an array.*

  - Optional challenge: If you have completed this problem, try to control the bouncing of lights using a sine function.

#### Problem 5 - Morse Code
* Write a program that lets you to input a word or sentence into the serial monitor and translate it to Morse code. Have an LED flash the Morse code.

	- *Hint: Read in inputted string and cycle through it using loops*
	- *Optional: Print out Morse code in Serial Monitor and produce Morse code sound using piezo buzzer*
  - Try your best with this problem, but do not worry if you can't finish it
	- Morse code array:
	```c++
	String morse[26] = {".-", "-...", "-.-.", "-..", ".", "..-.", "--.", "....", "..",     // A-I
			                ".---", "-.-", ".-..", "--", "-.", "---", ".--.", "--.-", ".-.",   // J-R 
			                "...", "-", "..-", "...-", ".--", "-..-", "-.--", "--.."};         // S-Z
	```
	- Serial read functions:
	```c++
	if (Serial.available() > 0) // send data only when you receive data
	Serial.read() // reads incoming serial data
	Serial.readString() // reads characters from the serial buffer into a String
	```


<!--
hide solutions
-->

## Solutions:
* [Problem 1 - Traffic Light]()
* [Problem 2 - LED Game]()
* [Problem 3 - Save Energy...Save the World]()
* [Problem 4 - Newton’s Luminescent Cradle]()
* [Problem 5 - Morse Code](https://bmesbuildteamucla.github.io/Winter%20Break/Problem%20Set%202/Problem%205%20-%20Morse%20Code/README.md)
