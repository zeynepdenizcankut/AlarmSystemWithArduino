# Alarm System with Arduino
The main goal was to create an alarm system using an Arduino with an Entry/Exit zone. One of the main goals was to give chance to user to activate and deactivate the system. It was needed to provide a strong security system for users. The system has 3 sensors. These sensors place in such a way as to be able to detect immediately when somebody enter the house from the door or windows. It also includes a method for arming/disarming the system. 
The alarm system has, an Arduino Uno, a breadboard, an lcd screen, a keypad, a buzzer, two ultrasonic sensors, one pir motion sensor, and resistors. The most important thing about this alarm system is the entry-exit zone. In alarm systems, time must be given to user to leave or enter the area. If time is not given to user, alarm will go off as soon as the system is activated. This means that user can’t enter or leave the area. The idea of using keypad is for giving chance to user to activate and deactivate the system. The keypad will also make possible to change password for the system. The active buzzer and the leds will be for showing the current state of the system. If the alarm is activated, the yellow led will work. If the alarm goes off, the buzzer will sound and red led will work. The buzzer will also sound for every push on the keypad. The lcd screen is going to be one of the most major compenents of the alarm system. The lcd will always give information about the current situation of the system. The lcd will show that on its screen how to activate the system and how to change password for the system. The lcd will give information about delays of entry-exit area for example how many seconds left for deactivating. It will also show that if the password is entered wrongly. It will always give information for the every possible situation of the system. 

HARDWARE DESIGN

KEYPAD:
These are the 4X4 matrix keypads pin connections to the Arduino. Since this is a 4X4 there is a need for 8 ports (4 rows + 4 columns). A wire is connected to each row and column of this keypad. Once a key is pressed a connection is made between the wire connected to that column and that row.

![keypad](https://user-images.githubusercontent.com/57444208/72442517-ba2bca00-37bd-11ea-8ce8-7257e657406c.png)

LCD WITH I2C:
The circuit below is of the LCD with the I2C bus adapter the only connection needed are GND, VCC (5V) an SDA and a SCL connection. The ports for the SDA (A4) and the SCL (A5) are shown below in this schematic. 

![lcd](https://user-images.githubusercontent.com/57444208/72442583-d4fe3e80-37bd-11ea-8218-725f71d58f08.png)

ULTRASONIC SENSOR:
Here is the Ultrasonic sensor and the outputs of the alarm system. The Ultrasonic sensor has four pins VCC, GND, Trigger and Echo it can handle 3.3-5V of supply voltage. The Trigger and Echo pins both require a Pulse Width Modulation pin slot each on the Arduino board. This is because the Trigger and Echo pins are constantly monitoring the changes between the distances of pings. 
The circuit was made via tinkercad.com. There was not ultrasonic sensor with 4 pins. For this reason, the circuit was shown like this. Trig pin1 went to pin A2 and Echo pin1 went to pin A3 on the Arduino. Trig pin2 went to pin 10 and Echo pin2 went to pin 11 on the Arduino. Vcc and Gnd were connected to the breadboard where the 5v and Gnd came from the Arduino.

![ultrasonic](https://user-images.githubusercontent.com/57444208/72442667-fa8b4800-37bd-11ea-9c67-f61a2b169877.png)

PIR SENSOR:
This is the PIR sensor circuit with the alarm systems outputs. This component is similar to the ultrasonic as it is also a motion detection sensor. This sensors operation is dependent on an imbalance between two infrared measurement levels. Once somebody enter the first IR range the PIR will detect that this is different to the 2nd’s level range and this will set off the alarm.
The PIR module has three pins one for VCC, GND and output, the output can be connected to a 3.3V-5V supply. The output pin of this sensor must be connected to a pulse width modulation slot on the Arduino as it is constantly measuring the change in IR levels checking for an imbalance. 
Here is the PIR was placed, the GND and VCC were connected and the output pin was connect to pin 12.

![pir](https://user-images.githubusercontent.com/57444208/72442711-1262cc00-37be-11ea-8161-4357ad7f990d.png)

Full circuit of the alarm system:

![circuit](https://user-images.githubusercontent.com/57444208/72442740-1f7fbb00-37be-11ea-8d4e-4135bb41911a.png)






