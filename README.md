# Arduino
## What is Arduino?

Arduino is an open-source electronics platform based on easy-to-use hardware and software. The core of arduino lies in its easily modifiable code and hardware.

An Arduino Board is a microcontroller on a circuit board reads inputs and drives outputs from compiled code. Below are some examples of both inputs and outputs available:
  * Inputs: Buttons, Switches, etc.
  * Outputs: LEDs, LCD Screen, etc.

### How to Start
The first step is to plug in your Arduino Board to your computer using the USB it is supplied with. Once you have done that, the drivers will begin to install and you are ready to start your first project in Arduino!

First off, we will need to access the online editor [Here](https://create.arduino.cc/editor/) and create a new Arduino account.

Once the editor is set up and ready to go, you should see something similar to this:
```
/*

*/

void setup() { // Initialization function
    
}

void loop() { // Main loop - continuously executes our code
    
}
```
Our Arduino program has two main functions:
  * setup() - Initializes variables and other things
  * loop() - Main loop which continuously executes our code
  
### Hello World!
Our first project will involve us taking an LED we have plugged into our board and turning it on. To achieve this, we use the code below:
```
int ledPin = 13;

void setup()
{
  pinMode(ledPin, OUTPUT);
}
void loop()
{
  digitalWrite(ledPin, HIGH);
}
```
In the first line, all we are doing is creating a variable named *ledPin* and assigning it to pin 13 on our Arduino Board.

* pinMode tells the compiler what type of module we are using and takes 2 parameters:
  * ledPin (The pin we are writing to)
  * OUTPUT (The type of module we are using. Can be OUTPUT or INPUT)
  
* digitalWrite writes to our module, telling it what we want it to do. It also has 2 parameters:
  * ledPin (Same as before)
  * HIGH (Tells the module to switch ON, in our case lighting the LED. Can be HIGH or LOW)

Before we compile and run our code, we still need to hardwire the arduino board itself.

<img src="https://www.arduino.cc/en/uploads/Tutorial/ExampleCircuit_bb.png" alt="Blink Setup" width="250" /><img src="https://www.arduino.cc/en/uploads/Tutorial/ExampleCircuit_sch.png" alt="Blink Setup Diagram" width="250"/>

Now we can compile our code in the web editor and run it...

### Goodbye World!
We can also turn the LED off by changing our digitalWrite function:
```
int ledPin = 13;

void setup()
{
  pinMode(ledPin, OUTPUT);
}
void loop()
{
  digitalWrite(ledPin, LOW);
}
```
We now have the ability to turn our LED on and off whenever we want, but what if we need it to blink?

`delay(1000)`

This will cause our code to delay by 1000ms or 1 second. Plugging this into our code we have:
```
int ledPin = 13;

void setup()
{
  pinMode(ledPin, OUTPUT);
}
void loop()
{
  digitalWrite(ledPin, HIGH);
  delay(1000);
  digitalWrite(ledPin, LOW);
  delay(1000);
}
```
