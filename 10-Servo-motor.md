# Controlling a servo motor using Arduino UNO
Because servo motors use feedback to determine the position of the shaft, you can control that position very precisely. As a result, servo motors are used to control the position of objects, rotate objects, move legs, arms or hands of robots, move sensors etc. with high precision. Servo motors are small in size, and because they have built-in circuitry to control their movement, they can be connected directly to an Arduino.  

Most servo motors have the following three connections: 
1. Black/Brown ground wire. 
1. Red power wire (around 5V). 
1. Yellow or White PWM wire.

**Circuit**: In this experiment, we will connect the power and ground pins directly to the Arduino 5V and GND pins. The PWM input will be connected to one of the Arduino's digital output pins.

**Code**:
The new functions used should be self understood by you. Their use requires an import of servo library. See first line of the code below
```C++
#include <Servo.h>

int pos = 0;

Servo servo_9; //declaring the name of servo as servo_9 

void setup()
{
  servo_9.attach(9); //the servo is attached to pin 9

}

void loop()
{
  // sweep the servo from 0 to 180 degrees in steps
  // of 1 degrees
  for (pos = 0; pos <= 180; pos += 1) {
    // tell servo to go to position in variable 'pos'
    servo_9.write(pos);
    // wait 15 ms for servo to reach the position
    delay(15); // Wait for 15 millisecond(s)
  }
  for (pos = 180; pos >= 0; pos -= 1) {
    // tell servo to go to position in variable 'pos'
    servo_9.write(pos);
    // wait 15 ms for servo to reach the position
    delay(15); // Wait for 15 millisecond(s)
  }
}
```




