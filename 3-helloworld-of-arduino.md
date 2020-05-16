# LED Blink Project
## The aim is to get you familiarised with the basic code structure of Arduino IDE

**Creating the circuit**
1. Open a new circuit file on Tinkercad
1. From the list of components, drag an Arduino UNO, LED and a resistor in the workspace.
1. Connect the cathode of the LED to one of the ground pins of arduino.
1. Connect the anode to one end of the resistor. Connect the other end of the resistor to a digital pin on arduino,     say pin 9. 1 kohm resistor is added to limit the current through the LED.

*We are done with the circuit part here*

![image](https://user-images.githubusercontent.com/42930138/82121578-c778b580-97ab-11ea-8924-6cf0682d9ee9.png)


**Writing the code**
1. We start by declaring the global variables.

```C++
int myLED = 9;// This stores integer 9 in a variable named myLED
```
2. The next section is the *setup*. This section runs only once during the code execution
```C++
void setup()
{
  //pinMode is an arduino library function which configures specific pin of arduino as i/o 
  //It takes in 2 inputs seperated by 'comma'
  //The first input asks the pin number and second input is either INPUT or OUTPUT depending on the
  //use of the input device
  //In this example myLED is the pin number and the LED is acting as an OUTPUT device
  pinMode(myLED, OUTPUT); 
}
```
3. The next section is the *loop*. This part of the code runs in a loop till the time arduino is turned off
```C++
void loop()
{
  //digitalWrite makes a pin HIGH OR LOW
  // turn the LED on (HIGH is the voltage level)
  digitalWrite(myLED, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  // turn the LED off by making the voltage LOW
  digitalWrite(myLED, LOW);
  delay(1000); // Wait for 1000 millisecond(s)
}
```
**Following is the complete code**
```C++
int myLED = 9;
void setup()
{
  pinMode(myLED, OUTPUT);
}

void loop()
{
  digitalWrite(myLED, HIGH);
  delay(1000);
  digitalWrite(myLED, LOW);
  delay(1000); 
}
```

