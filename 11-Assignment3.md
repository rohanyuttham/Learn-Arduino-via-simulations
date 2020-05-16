# Design a smart room with following features:
1. If a person is inside a room and pushes the button, light will be turned on until the fan makes 5 oscillations and then will be turned off.
2. If a person is not inside the room, and pushes on the button, the light will be turned on only until one oscillation of the fan.
3. However, the user can override the 2nd condition by long pressing the button. In this case, point no. 1 will be valid.

**Equivalents in this circuit:**
1. Here, inside the room means, the person is in the range of 30-100cm of an ultrasonic sensor.
1. Light is an LED bulb
1. Fan is a servo motor. One oscillation means going from 0-180degree and again returning to zero degrees.
1. Long press means that the button is pressed for more than 3 seconds.

Note: 
1. Make a neat circuit with clear connections.
1. Do not put more than one wire in one Arduino pin. Use a breadboard if needed.
