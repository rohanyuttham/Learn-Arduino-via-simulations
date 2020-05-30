# LIne following robot

**Making a simple line following differential drive robot using the theory learnt in last tutorial**

**Electrical Components used**:
1. IR Sensor- It will act as an input device for us which will detect the color of the ground.
    1. Crux- When the sensor is above a white surface, it will give a HIGH signal and when it is above a black surface, it will give a low signal.
    1. The sensors will be placed at the front side of the robot facing the ground:
    ![image](https://user-images.githubusercontent.com/42930138/82197353-88b43e00-9918-11ea-884c-41463b8e8905.png)
1. Two DC Motors to drive the wheel.
1. Arduino UNO Board
1. L298 Motor Driver

For other components used, you may refer to the following slide made by Robotics Club, IITD:
[RW on Line following robot](https://drive.google.com/open?id=1nGk8AG7Ent-GKmRkeSjkaip3T2FgikwI)

**Circuit**
1. IR Sensor has 3 pins
    1. Connect Vcc to 5V of arduino
    1. Connect GND to ground of arduino
    1. Connect SIG(Signal pin) to any of the digital pin of arduino
1. The connections of other electronics are already covered in the previous tutorial: [DC Motor Speed Control](https://github.com/rohanyuttham/Learn-Arduino-via-simulations/blob/master/13-Speed-Control-of-DC-Motor-L298.md)

**Concept:**
1. When both left and right sensor senses white then robot move forward.(Both wheels move with same speed) ![image](https://user-images.githubusercontent.com/42930138/82198585-265c3d00-991a-11ea-9fd1-d7c7e4c78e41.png)
1. If left sensor comes on black line then robot turn left side.(speed of right wheel will be more than speed of left wheel) ![image](https://user-images.githubusercontent.com/42930138/82198684-455acf00-991a-11ea-8172-22b0a684228c.png)
1. If right sensor sense black line then robot turn right side until both sensor comes at white surface. When white surface comes robot starts moving on forward again. ![image](https://user-images.githubusercontent.com/42930138/82198750-63283400-991a-11ea-8f89-a323364ef713.png)
1. If both sensors comes on black line, robot stops. 

![image](https://user-images.githubusercontent.com/42930138/82198818-7e933f00-991a-11ea-8f5c-c8b9cb30a1bb.png)

**Code:**
That's your next assignment ;)
