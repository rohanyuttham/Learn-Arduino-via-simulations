# Program for line following robot

Write down a code for a line following robot which has 2 DC motors, an L298 motor controller and 2 IR sensors.
The previous two tutorials can be referred for any doubts.

**Reading data from the sensor:**
1. First, you need to define the sensor as an inout device using the *pinMode* function inside void setup():
```C++
pinMode(IRpin, INPUT);
```
2. digitalRead() is used to know the state of the sensor as
```C++
state = digitalRead(IRpin); //This will give HIGH for white surfaces and LOW for black surfaces
```
3. Use if() statements to control the speed of the motors depending on the state of IR sensor


Note: Tinkercad does not have IR sensors in it. So, you only need to submit the code part for this assignment.

