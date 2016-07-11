# Grove - Infrared Reflective Sensor
----------
【**[中文版](http://www.seeedstudio.com/wiki/index.php?title=Grove_-_Infrared_Reflective_Sensor_%E7%BA%A2%E5%A4%96%E5%8F%8D%E5%B0%84%E4%BC%A0%E6%84%9F%E5%99%A8&uselang=zh)**】

## Introduction ##
![500px-Infrared_Reflective_Sensor-1](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/blob/master/image/500px-Infrared_Reflective_Sensor-1.JPG?raw=true)

**Grove - Infrared Reflective Sensor** is used to detect the presence of an object within a specific range. The sensor consists of an IR LED and a photosensor (phototransistor) pair. The light emitted by the IR LED gets reflected by any object placed in front of the sensor and this reflection is detected by the photosensor(phototransistor). Any white (or lighter) colored surface reflects more than black (or darker) colored surface.
When the reflected light is detected, it produces **Digital HIGH** (or **Binary 1**) output on the **SIG** pin. The on-board LED indicator will also glow. If no reflection is detected or if the object is too far from the sensor, the output on the **SIG** pin stays at **Digital LOW** (**Binary 0**). The on-board LED indicator will be off as well. The detectable range of this sensor is 4–16 mm. The module incorporates a Rail-to-Rail Operational Amplifier to amplify the output of phototransistor. There is a potentiometer which can be used to adjust the gain of the amplifier, that is, sensitivity of detection.
With this sensor, you can build the following (but not limited to) applications: **line following robots**,  **optical encoders** and **object counting applications**.

!!!Note
    This product is also mildly sensitive to non-IR radiations and hence any bright light on photosensor impairs or disturbs IR light detection.

### Version Tracker ###

Product version| Release date	|Support status	| Notes
---:|:---:|:---:|:---:
Versions older than v1.2	|  June 2012‎	|Not supported	|None
Version 1.2(current version)	|April 2016	|Supported|	None


[![enter image description here](http://www.seeedstudio.com/wiki/images/thumb/d/d0/Get_One_Now_Banner.png/150px-Get_One_Now_Banner.png)](https://www.seeedstudio.com/item_detail.html?p_id=1230)

## Features ##
- Grove compatible and easy to use
- Highly sensitive and reliable
- Small footprint
- Adjustable sensitivity for different occasions

## Specification ##

---|---
:---|:---:
Operating voltage(V)	|4.5–5.5V
Operating current(mA)	|14.69–15.35 mA
Effective detectable distance	|0.5–4.5 cm
Response time|	10 μs
Phototransistor: Peak sensitivity wavelength	|800 nm
IR LED: Peak light emitting wavelength	|940 nm
Reflective photosensor|	**[datasheet](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/raw/master/resource/RPR-220.pdf)**
Output operational amplifiers|	**[datasheet](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/raw/master/resource/LMV358_datasheet.pdf)**
Weight|	4 g

### Platform supported ###

Platform|	Seeeduino/Arduino	|Rasberry Pi	|LinkIt One	|Beaglebone
---:|:---:|:---:|:---:|:---:|
**Supported status**	|Supported	|Supported (using GrovePi)	|Not Supported|	Supported(only with **[Grove Base Cape for Beaglebone](https://www.seeedstudio.com/item_detail.html?p_id=2644)**)

!!!Notes	
    If no version number is mentioned for a specific platform, it means this product supports all versions within this platform. But, you will need additional Grove Shield like **[Grove - Base shield v2](https://www.seeedstudio.com/item_detail.html?p_id=1378)** board.


## Hardware Overview ##

![](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/blob/master/image/600px-Grove_-_Infrared_Reflective_Sensor_v1.2_hardware_overview_1200_z.jpg?raw=true)

- RPR220 Reflective photosensor, Highly sensitive reflective photosensor.
- LMV358, rail-to-rail operational amplifier.
- LED Indicator, The LED will switch on when the received infrared light intensity exceeds a preset level.
- Light sensitivity adjustment potentiometer , adjust the sensitivity of photosensor to light.

### Package includes ###

Parts name	|Quantity
---:|:---:
Grove - Infrared Reflective Sensor	|1 piece
Grove cable	|1 piece

## Getting Started ##
Let us see how to implement few basic applications with this module:

### With Arduino ###
#### Materials required ####
- 1x **[Grove Infrared Reflective Sensor ](https://www.seeedstudio.com/item_detail.html?p_id=1230)**
- 1x **[Arduino UNO](https://www.seeedstudio.com/item_detail.html?p_id=694)** (other compatible boards) 
- 1x **[Grove cable ](https://www.seeedstudio.com/item_detail.html?p_id=925)**
- 1x **[Grove Base shield](https://www.seeedstudio.com/item_detail.html?p_id=754)**

#### Line Following ####
This sensor can be used to help a robotic car follow a black line.

<ol>1. Adjusting </ol>

<ol>Place the sensor such that there is 12mm between reflective photosensor and white (or light) colored surface.</ol>

![](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/blob/master/image/300px-Infrared_Reflective_Sensor-4.JPG?raw=true)

<ol>2. Adjust the potentiometer with a screwdriver to change the sensitivity of reflective photosensor, until the LED indicator glows. As your rotate clockwise, the reflective photosensor will be more sensitive to light. </ol>

!!!Note 
    Use a proper screw-driver to adjust the tiny potentiometer. Applying heavy pressure or frequent adjustments might damage the wiper of the potentiometer.

![](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/blob/master/image/300px-Infrared_Reflective_Sensor-5.JPG?raw=true)

<ol>3. By maintaining the vertical distance, move the sensor horizontally above the black line. The indicator LED must go off over the black line. If it is still on, adjust the potentiometer until it is off.</ol>

![](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/blob/master/image/300px-Infrared_Reflective_Sensor-6.JPG?raw=true)

![](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/blob/master/image/300px-Infrared_Reflective_Sensor-7.JPG?raw=true)

#### Rotary Speed Detection ####
Let us implement simple optical encoder to detect the speed of a motor
<ol>1. Connect the Infrared Reflective Sensor to the **D2 port** of Grove - Base Shield like this:</ol>

![](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/blob/master/image/300px-Infrared_Reflective_Sensor-11.JPG?raw=true)

<ol>2. Attach a round, white paper plate (with a black line marked on it) to the motor. Place the sensor near this rotatory encoder. Run the motor.</ol>

![](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/blob/master/image/500px-Infrared_Reflective_Sensor-8.JPG?raw=true)

![](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/blob/master/image/500px-Infrared_Reflective_Sensor-9.JPG?raw=true)

<ol>3. Download the library **[Arduino timer1 library](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/raw/master/resource/TimerOne-ArduinoLib.zip)** and add it into the libraries file of Arduino IDE. A **[<span style ="color: red">guide</span>](http://www.seeedstudio.com/wiki/Guide_to_use_demos_downloaded_from_Seeed%27s_Github)** about how to run our demo code.</ol>

<ol>4. Upload the demo code to your Arduino/Seeeduino.</ol>

```
unsigned int counter=0;
void blink()
{
  counter++;
} 
void timerIsr()
{
  Timer1.detachInterrupt();  //disable the timer1
  Serial.print("The speed of the motor: "); 
  Serial.print(counter,DEC);  
  Serial.println("round/s"); 
  counter=0;  
  Timer1.attachInterrupt( timerIsr );  //enable the timer1
}
void setup() 
{
  Serial.begin(9600);
  Timer1.initialize(1000000); // set a timer of length 1sec
  attachInterrupt(0, blink, RISING);  //INT0
  Timer1.attachInterrupt( timerIsr ); // attach the service routine here
} 
void loop()
{
  ;  //do nothing
}
```

<ol>5. Open the Serial Monitor to read the data.</ol>

![](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/blob/master/image/400px-Infrared_Reflective_Sensor-10.JPG?raw=true)

![](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/blob/master/image/Infrared_Reflective_Sensor-12.JPG?raw=true)

### With Raspberry Pi ###
#### Material required ####
- 1x Raspberry Pi (other models also are fine)
- 1x **[GrovePi](https://www.seeedstudio.com/item_detail.html?p_id=1672)** or **[GrovePi+](https://www.seeedstudio.com/item_detail.html?p_id=2241)**
- 1x **[Grove cable](https://www.seeedstudio.com/item_detail.html?p_id=925)** 

#### Hardware Connections and Software Work ####
<ol>1. You should have got a Raspberry Pi and a GrovePi or GrovePi+. In this demo, we use GrovePi.</ol>

<ol>2. We assume you have built the development environment successfully. If not, follow this **[<span style="color: red">tutorial</span>](http://www.seeedstudio.com/wiki/GrovePi%2B#Introducing_the_GrovePi.2B)**.</ol>

<ol>3. Connection:</ol>
<ol>Plug Grove - Infrared Reflective Sensor into port **D4** on GrovePi with **[Grove cables](https://www.seeedstudio.com/item_detail.html?p_id=925)**</ol>

<ol>4. Navigate to the demos' directory, run the following command in a terminal:</ol>

<ol>**cd yourpath/GrovePi/Software/Python/**</ol>

<ol>Run the command in a terminal:</ol>

<ol>**nano grove_infrared_reflective_sensor.py**</ol>

Copy and save the following code into it:

```
import time
import grovepi
 
# Connect the Grove Infrared Reflective Sensor to digital port D4
# SIG,NC,VCC,GND
sensor = 4
 
grovepi.pinMode(sensor,"INPUT")
 
while True:
    try:
        # Sensor returns HIGH on a black surface and LOW on a white surface
        if grovepi.digitalRead(sensor) == 1:
            print "black surface detected"
        else:
            print "white surface detected"
 
        time.sleep(.5)
 
    except IOError:
        print "Error"
```

<ol>5. To run the demo, execute the following command in terminal:</ol>

<ol>**sudo python grove_infrared_reflective_sensor.py**</ol>


## Resources ##
- **[Grove-Infrared Reflective Sensor Eagle Files](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/raw/master/resource/Grove_-_Infrared_Reflective_Sensor_v1.0_SourceFile.zip)**
- **[Arduino Timer1 Library](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/raw/master/resource/TimerOne-ArduinoLib.zip)**
- **[RPR220 ](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/raw/master/resource/RPR-220.pdf)**
- **[RPR200](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/raw/master/resource/RPR220_datasheet.pdf)**
- **[LMV358_datasheet](https://github.com/SeeedDocument/Grove_Infrared_Reflective_Sensor/raw/master/resource/LMV358_datasheet.pdf)**


##Is this page helpful?
<iframe style="height: 600px; width: 500px; margin: 10px 0 10px;" allowTransparency="true" src="https://www.surveymonkey.com/r/MSLNQ7H" frameborder="0"></iframe>