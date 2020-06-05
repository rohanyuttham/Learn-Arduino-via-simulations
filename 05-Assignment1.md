# LED Blink project without using delay function
**delay() is a handy function but it has some disadvantages in certain scenarios**
>No other reading of sensors, mathematical calculations, or pin manipulation can go on during the delay function, 
>so in effect, it brings most other activity to a halt.

millis() function can be manipulated to use in place of a delay().

Your task is to read about millis() [here](https://www.arduino.cc/reference/en/language/functions/time/millis/).

Then, write a code for an LED blink using millis() and not delay().
