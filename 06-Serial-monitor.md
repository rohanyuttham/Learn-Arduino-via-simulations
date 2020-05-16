# A quick intro to very useful tool in arduino programming- Serial Monitor
When you are in the code section on tinkercad, look on the bottom of your screen to find the Serial Monitor. Click on it to pop it up

1. To use Serial monitor, first of all you need to write following piece of line in your void setup()
```C++
Serial.begin(9600); //initializes a serial communication b/w board and your computer at 9600 bits/s
```
2. **Serial.println();** : 
   This function takes a variable as its input and prints it on the Serial Monitor
   You can also print a constant string by inputting a text within double inverted commas as the argument of this function

Why use this?
1. Get real-time readings from a sensor
2. Embed debug messages in code: Print to the serial monitor at crucial points in execution, to help with troubleshooting

You will understand it better in the future tutorials and assignments

   
