# Speed Control of DC Motor using L298 Motor Control

Before, we start, this particular motor control is not available on tinkercad. I chose this one because it's one of the 
most common motor controller used in small projects. That being said, tinkercad has another motor controller which you might wish to explore for simulation purpose.

## L298 Motor Board
![image](https://user-images.githubusercontent.com/42930138/82190333-82b95f80-990e-11ea-828b-a346fed4435a.png)

### **Circuit**
1. First, of all to power up the L298 board, we connect a DC power source(a battery) with its positive terminal to +12V and negative terminal to the GND pin of L298
1. This motor driver has two channels. Connect the terminals of first motor to MotorA pins and of the second motor to MotorB pins.
Note that the order of wire connecting motor and board does not matter. Their order will change the sign of voltage being sent to the
motor which in turn will change the direction of its rotation. However, this is not an issue because we can control the 
direction in our code.
1. Coming to the connections between the arduino and controller:
    1. Connect the pins IN1, IN2, IN3 and IN4 to any four digital pins of your Arduino UNO.
        1. The pins IN1 and IN2 will be used to control the direction of rotation of MotorA.
        1. The pins IN3 and IN4 will be used to control the direction of rotation of MotorB.
    1. Connect ENA and ENB(PWM Signal) to two of the PWM pins(a digital pin on arduino recognised by '~' sign at its side) of your board.
        1. These are called enable pins. They will be used to control the speed of the motor.
    1. Lastly, when we have uploaded the code to the board, we would like it to have independent power supply. Remove the USB cable and connect the +5V pin of L298 to Vin of the Arduino. Also connect GND of L298 to a ground pin on Arduino.
    
We are done with the circuit connections.

### **Code:**
Note that the following code is for controlling only MotorA. You can extend the same for controlling both motors as well:
1. Initialising the global variables in the beginning:
```C++
int enA=9; //note that pin 9 is a PWM pin. It has '~' on its side
int in1=4;
int in2=5;
int speedA=100; //This value can be varied b/w 0 and 127, 0 being no rotation and 127- the highest speed
```
    
The analog value given to the variable named 'speedA' maps the voltage output of DC MotorA b/w 0V and 5V.

2. Setup:
```C++
void setup()
{
  pinMode(enA, OUTPUT);
  pinMode(in1, OUTPUT);
  pinMode(in2, OUTPUT);
}
```
3. Loop:
```C++
void loop()
{
  //The following 2 lines will make the motor rotate in one direction. Reverse the order of the HIGH and LOW, and motor will 
  //start rotating in the reverse direction of this.
  digitalWrite(in1, HIGH); 
  digitalWrite(in2, LOW);
  
  //Following line is for speed control
  analogWrite(enA, speedA);
}
```

Entire code can also be found in the *codes* folder.




    

    
    
