# Arduino UNO Board Breakdown
![image](https://user-images.githubusercontent.com/42930138/82119745-9d6cc680-979e-11ea-8364-ce4edd6c978c.png)

1. **Reset Button** – This will restart any code that is loaded to the Arduino board 
2. **AREF** – Stands for “Analog Reference” and is used to set an external reference voltage
3. **Ground Pin** –There are a few ground pins on the Arduino and they all work the same
4. **Digital Input/Output** – Pins 0-13 can be used for digital input or output 
5. **PWM** – The pins marked with the (~) symbol can simulate analog output 
6. **USB Connection** – Used for powering up your Arduino and uploading sketches
7. **TX/RX** – Transmit and receive data indication LEDs 
8. **ATmega Microcontroller** – This is the brains and is where the programs are stored 
9. **Power LED Indicator**– This LED lights up anytime the board is plugged in a power source
10. **Voltage Regulator** – This controls the amount of voltage going into the Arduino board 
11. **DC Power Barrel Jack** – This is used for powering your Arduino with a power supply
12. **3.3V Pin** – This pin supplies 3.3 volts of power to your projects 
13. **5V Pin** – This pin supplies 5 volts of power to your projects
14. **Ground Pins** – There are a few ground pins on the Arduino and they all work the same
15. **Analog Pins** – These pins can read the signal from an analog sensor and convert it to digital 


## Power Supply to the board
1. Via USB cable from your computer
2. Using an external 9V DC Jack
3. Using 5V input on the ‘Vin’ pin of the arduino

Note:
>Always use only one out of the above three options. 
>This is because if the ground of more than one source will be connected to the board,they all will 
>become common(will get internally connected on the board). These ground inputs in most of the 
>practical scenarios will not be exactly 0V. So, the different ground inputs will create a finite 	
>potential difference in a 0 resistance path. This will make the current very large b/w two grounds 
>of the arduino which may blow up the board.

