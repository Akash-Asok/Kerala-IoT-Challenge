# Kerala-IoT-Challenge

> [**Foxlab Makerspace**](https://www.facebook.com/foxlabmakerspace/) in association with [**GTech - Group of Technology Companies**](https://atfg.gtechindia.org/) in Kerala is launching the program **“Kerala IoT Challenge”**, with a vision to mold 100 IoT experts in Kerala, hosting on the µLearn platform. **Kerala IoT Challenge** is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation.

> This page is maintained so as to keep the track of my experiments at different levels of the **Kerala IoT Challenge**.

# About Me
Hi,everyone I am A Akash,Currently pursuing B-tech from RIT Kottayam,My field of interests are
* IoT
* Chaos theory
* Compliant mechanisms
* Robotics

# Experiment-1 HELLO WORLD LED BLINKING
Iintoduction to Arduino IDE and Its programming is intended here

## Components Required
* Arduino Uno R3 *1
* Bread Board *1
* Jumper Wires(Male to male ) *2
* LED *1
* 220 Ohm resistor *1
* Usb A to B cable *1
 
## Circuit Diagram
 ![Exp1](https://user-images.githubusercontent.com/85242299/167358514-47d3a5ae-87ce-4d61-a675-96a7deb52b97.JPG)
 
##  Code
 ```
 
 int ledPin=5;  //defining ledpin as pin 5
void setup() {
   pinMode(5,OUTPUT); //define pin5 as output type: 
}

void loop() {
  digitalWrite(ledPin,HIGH);//setting pin to on position
  delay(1000); //delay of 1 second
  digitalWrite(ledPin,LOW);//set led to off position
  delay(1000); //wait for a second
  
  

}
 ```
## Output
The LED blinks with a delay of one second 
## Output video


# Experiment-2 Traffic Light

## Components Required

* Arduino board *1
* USB type A to B cable *1
* Red Led*1
* Yellow  LED*1
* Green LED*1
* 220ohm resistor *3
* Breadboard*1
* Breadboard jumper wires* several

## Circuit Diagram
![Exp2](https://user-images.githubusercontent.com/85242299/167358890-e1f23eef-eeee-4e37-959b-1109bf8e8ca6.JPG)

## Code

```
int Green=5;//defining ledpin as pin 5
int Yellow=8;//defining ledpin as pin 8
int Red=6;//defining ledpin as pin 6
void setup() {
   pinMode(5,OUTPUT); //define pin5 as output type: 
   pinMode(8,OUTPUT); //define pin8 as output type:
   pinMode(6,OUTPUT); //define pin6 as output type:
}

void loop() 
{
  digitalWrite(Green,HIGH);//setting Green to On position
  delay(5000); //delay of 5 second
  digitalWrite(Green,LOW);//set led to off position
  delay(1000); //wait for a second
  for(int i=1;i<=3;i++)
     {
      digitalWrite(Yellow,HIGH);//setting Yellow to On position
      delay(500); //delay of 0.5 second
      digitalWrite(Yellow,LOW);//set led to off position
      delay(500); //wait for 0.5 second
     }    // Blinks Yellow 3 times
      digitalWrite(Red,HIGH);//setting RED to On position
      delay(500); //delay of 5 second
      digitalWrite(Red,LOW);//set led to off position
      delay(500); //wait for 0.5 second
     
}
```
## Output
The green Led lights for five seconds followed by yellow LED blinking three times with a delay of 0.5seconds followed by the red LED ON for 5 seconds 
## Output video


# Experiment-3 LED Chasing Effect
 In this experiment, we compile a program to simulate LED chasing effect.
 
## Components Required
* Arduino Uno *1nos
* Bread Board *1nos
* Usb Type A to Type B *1nos
* Jumper Cable *13nos
* Led *6nos
* 220ohm resistor*6nos

## Circuit Diagram
![Exp3](https://user-images.githubusercontent.com/85242299/167359151-0d57b5d1-a030-45ae-adc4-1e3c0dd9b79d.JPG)


## Code
```
int BASE = 2;  // the I/O pin for the first LED
int NUM = 6;   // number of LEDs
void setup()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     pinMode(i, OUTPUT);   // set I/O pins as output
   }
}
void loop()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, LOW);    //  turn off LEDs one by one.
     delay(200);        // delay
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, HIGH);    // turning on LED s one by one
     delay(200);        // delay
   }  
}
```
##  OUTPUT

The Leds will all lights up with a delay of 0.2 seconds and then turns of one by one with a delay of 0.2 second
## Output video

 
#  Experiment 4 BUTTON CONTROLLED LED
 
Taking feedback from a button to control any output pin,also to study setting of pins as input.
 
##  Components Required 
 * Arduino Uno*1
 * Usbtype A to type B cable*1
 * Button switch*1
 * Red M5 LED*1
 * 220ΩResistor*1
 * 10KΩ Resistor*1
 * Breadboard*1
 * Breadboard Jumper Wire*6
 
##  Circuit Diagram
 ![Exp4](https://user-images.githubusercontent.com/85242299/167359608-5e83a9f5-94a9-4586-be62-bd0c5bb3e644.JPG)


 
##  Code
 ```
 int ledpin=11;
int button=7;
int val;// define val
void setup()
{
pinMode(ledpin,OUTPUT);// set LED pin as output type
pinMode(button,INPUT);// set button as input pin
}
void loop()
{
val=digitalRead(button);// read the level value of pin 7 and assign if to val
if(val==LOW)// check if the button is pressed, if yes, turn on the LED
  {
  digitalWrite(ledpin,LOW);
  }
else
  { 
  digitalWrite(ledpin,HIGH);}
  }
  ```
##  OUTPUT 
  
The led blinks as the button is pressed.
## output vedio

# EXPERIMENT 5 Buzzer
 
## AIM
 
 To control a buzzer
 
## COMPONENTS REQUIRED
 
 * Arduino Uno
 * Buzzer*1
 * Breadboard*1
 * Breadboard Jumper Wire*2
 * USB type A to type b*1
  
## CIRCUIT DIAGRAM
 ![Exp5](https://user-images.githubusercontent.com/85242299/167361647-5a811454-89b4-46b7-bf08-5ce5e0848d4e.JPG)


 
## CODE
 ```
int buzzer=8;// initialize digital IO pin that controls the buzzer
void setup() 
{ 
  pinMode(buzzer,OUTPUT);// set pin mode as “output”
} 
void loop() 
{
digitalWrite(buzzer, HIGH); // produce sound
}
```

## OUTPUT

The buzzer buzzes.
## OUTPUT VEDIO


# EXPERIMENT 6 RGB LED

## AIM

To control the RGB LED to give diffrent pattern output

## Note

An RGB LED bulb uses three diodes in Red, Green and Blue. These are mixed in different intensities to produce a variety of different colours. The process is based on additive color mixing, the same technique which is used in TV sets, computer monitors and flat screens.

analogWrite() takes two or three arguments:
pin: the number of the pin whose value you wish to set
value: the duty cycle: between 0 (always off) and 255 (always on). Since 0.6.0: between 0 and 255 (default 8-bit resolution) or 2^(analogWriteResolution(pin)) - 1 in general.
frequency: the PWM frequency (optional). If not specified, the default is 500 Hz.


## Components required
* Arduino Uno *1
* USB Cable type A to type B * 1
* RGB LED * 1
* Resistor 220ohm *1
* jumper wire*5
## Code
```
int redpin = 11; // red LED
int bluepin =10; //  blue LED
int greenpin =9;//  green LED
int val;
void setup() {
  pinMode(redpin, OUTPUT);
  pinMode(bluepin, OUTPUT);
  pinMode(greenpin, OUTPUT);
  Serial.begin(9600);
}
void loop() 
{
for(val=255; val>0; val--)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
for(val=0; val<255; val++)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
 Serial.println(val, DEC);
}
```
## Circuit Diagram
![Exp6](https://user-images.githubusercontent.com/85242299/167363046-a40c6800-fab6-41fe-9f31-9371ef019834.JPG)


## OUTPUT
The  RGB LED glows with aspecific pattern and brightness level
## OUTPUT VIDEO


# EXPERIMENT 7-LDR Light Sensor

## LDR sensor
LDR ( light dependent resistor ) also called photoresistors are responsive to light. Photoresistors are used to indicate the intensity or the presence or the absence of light. When there is darkness the resistance of photoresistor increases and when there is sufficient light it dramatically decreases.
## COMPONENTS REQUIRED
 * Arduino Uno 
 * Photo Resistor
 * Red M5 LED*
 * 10KΩ Resistor
 * 220Ω Resistor
 * Breadboard
 * Breadboard Jumper Wire
 * USB cable
## CIRCUIT DIAGRAM
![Exp7](https://user-images.githubusercontent.com/85242299/167362905-faa094f5-1361-48ee-be36-3bbff050fafe.JPG)

## CODE
```
int in=0;
int ledpin=11; 
int val=0;
void setup()
{
pinMode(ledpin,OUTPUT);
Serial.begin(9600);
}
void loop()
{
val=analogRead(in);
Serial.println(val);
analogWrite(ledpin,val/4);
delay(10);
}
```
## NOTE
 * Ldr resistance will decrease as the incident light increases
 * The analogread() varies from 0 to 1023 
 * analogWrite() varies from 0 to 255 (1/4 th)
## OUTPUT
When the light falling on the Ldr the analog value is read and is fed to the led as duty cycle of range 255.and the Led attains brightness at the same rate the light in the room decreases.
## OUTPUT VIDEO



# EXP-8 Flame Sensor

## WORKING
When fire burns it emits a small amount of Infra-red light, this light will be received by the Photodiode (IR receiver) on the sensor module. Then we use an Op-Amp to check for a change in voltage across the IR Receiver, so that if a fire is detected the output pin (DO) will give 0V(LOW), and if the is no fire the output pin will be 5V(HIGH).
## COMPONENTS REQUIRED
  * Arduino Uno (any Arduino board can be used)
  * Flame sensor module
  * LED
  * Buzzer
  * Resistor
  * Jumper wires
    
## CODE
```
int buzzer = 13;
int LED = 12;
int flame_sensor = 4;
int flame_detected;

void setup()
{
  Serial.begin(9600);
  pinMode(buzzer, OUTPUT);
  pinMode(LED, OUTPUT);
  pinMode(flame_sensor, INPUT);
}

void loop()
{
  flame_detected = digitalRead(flame_sensor);
  if (flame_detected == 0)
  {
    Serial.println("Flame detected! take action immediately.");
    digitalWrite(buzzer, HIGH);
    digitalWrite(LED, HIGH);
    delay(200);
    digitalWrite(LED, LOW);
    delay(200);
  }
  else
  {
    Serial.println("No flame detected");
    digitalWrite(buzzer, LOW);
    digitalWrite(LED, LOW);
  }
  delay(1000);
}

```

## CIRCUIT DIAGRAM

![Exp8](https://user-images.githubusercontent.com/85242299/167363531-0d9aecee-ea43-4792-8ed4-1013f451566e.JPG)

  
## OUTPUT VIDEO


## OUTPUT
The flame sensor detects the presence of fire or flame based on the Infrared (IR) wavelength emitted by the flame and triggers the alarm in case of fire deteced



# EXP-9  LM35 Temperature Sensor

## LM35 SENSOR
LM35 is an analog, linear temperature sensor whose output voltage varies linearly with change in temperature.It can measure temperature from-55 degree celsius to +150 degree celsius. The voltage output of the LM35 increases 10mV per degree Celsius rise in temperature. LM35 can be operated from a 5V supply.
## COMPONENTS REQUIRED
 * Arduino Uno 
 * LM35
 * Breadboard
 * Breadboard Jumper Wire
 * USB cable
## CIRCUIT DIAGRAM
![Exp9](https://user-images.githubusercontent.com/85242299/167364061-2e4eefc1-64c4-4c06-90de-9a49e032389f.JPG)

## CODE

```
int potPin = 0; 
void setup()
{
Serial.begin(9600);// set baud rate at”9600”
}
void loop()
{
int val;// define variable
int dat;// define variable
val=analogRead(0);
dat=(125*val)>>8;
Serial.print("Temp");
Serial.print(dat);
Serial.println("C");
delay(500);
}

```
## NOTE
 LM35 is an analog temperature sensor. This means the output of LM35 is an analog signal. Microcontrollers dont accept analog signals as their input directly. We need to convert this analog output signal to digital before we can feed it to a microcontroller’s input. For this purpose, we can use an ADC( Analog to Digital Converter).Arduino uno has an in built 10 bit ADC (6 channel). We can make use of this in built ADC of arduino to convert the analog output of LM35 to digital output.
 
## OUTPUT
The temperature is displayed on serial monitor

