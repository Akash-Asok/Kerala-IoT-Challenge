# Kerala-IoT-Challenge

> [**Foxlab Makerspace**](https://www.facebook.com/foxlabmakerspace/) in association with [**GTech - Group of Technology Companies**](https://atfg.gtechindia.org/) in Kerala is launching the program **“Kerala IoT Challenge”**, with a vision to mold 100 IoT experts in Kerala, hosting on the µLearn platform. **Kerala IoT Challenge** is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation.

> This page is maintained so as to keep the track of my experiments at different levels of the **Kerala IoT Challenge**.

# About Me
Hi,everyone I am A Akash,Currently pursuing B-tech from RIT Kottayam,My field of interests are
* IoT
* Compliant mechanisms
* Robotics

# Experiment-1 HELLO WORLD LED BLINKING
Intoduction to Arduino IDE and its programming is intended here

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
 
 int ledPin=10;  //defining ledpin as pin 10
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


https://user-images.githubusercontent.com/85242299/167548335-7f5455c0-93f3-4257-90a8-845c7d86dc61.mp4



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
int Green=5;//defining ledpin as pin 4
int Yellow=8;//defining ledpin as pin 7
int Red=6;//defining ledpin as pin 10
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
The green Led turns on for five seconds followed by yellow LED blinking three times with a delay of 0.5seconds followed by the red LED turning on  for 5 seconds 
## Output video




https://user-images.githubusercontent.com/85242299/167553498-c7ab24dd-08af-424b-b0f2-5a9e2f112a1f.mp4





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

The Leds will all lights up with a delay of 0.2 seconds and then turns off one by one with a delay of 0.2 second
## Output video


https://user-images.githubusercontent.com/85242299/167548392-81ca97df-4da8-4c51-8402-4878a6c6d539.mp4


 
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

## Note
As I had no 10KOhm resistors I have used 5 56KOhm resistors in parallel to get an effective resistance of 11.2KOhm which seems to serve the purpose.
 
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
## output video


https://user-images.githubusercontent.com/85242299/167555719-5ec42c1c-ecac-4ab7-9581-24e72f653e3a.mp4


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

The buzzer buzzes continuously.
## OUTPUT VIDEO


https://user-images.githubusercontent.com/85242299/167548482-2368a445-ec0b-4c8a-81b0-cf280aaa8a03.mp4



# EXPERIMENT 6 RGB LED

## AIM

To control the RGB LED to give different colours.

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
The  RGB LED glows with different colours.
## OUTPUT VIDEO


https://user-images.githubusercontent.com/85242299/167556797-95f2eb71-3aa4-4bf5-b8e5-c27b9ea95f00.mp4



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
 * As I had no 10KOhm resistors I have used 5 56KOhm resistors in parallel to get an effective resistance of 11.2KOhm which seems to serve the purpose.
 * Ldr resistance will decrease as the incident light increases
 * The analogread() varies from 0 to 1023 
 * analogWrite() varies from 0 to 255 (1/4 th)
## OUTPUT
When light falls on the LDR ,the analog value is read and displayed on the serial monitor.
## OUTPUT VIDEO


https://user-images.githubusercontent.com/85242299/167548512-509141db-dfbf-4538-9dfc-2af0b1144013.mp4




https://user-images.githubusercontent.com/85242299/167556840-0191e6a5-3918-4a80-8c1e-13076a0d1c41.mp4











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

# EXP-10 IR Remote Control Using TSOP

## IR 
The signal from the infrared remote controller is a series of binary pulse code. To avoid the other infrared signal interference during the wireless transmission, the signal is pre-modulated at a specific carrier frequency and then send out by an infrared emission diode. The infrared receiving device needs to filter out other waves and receive signals at that specific frequency and to modulate it back to binary pulse code, known as demodulation.

## WORKING
IR remote controls, as the name would imply, make use of pulses of infrared light to send signals to a receiving device such as a television or sound system. Each button on the remote control sends out a unique pattern of pulses which are decoded by the receiver so that the appropriate action is performed.

## COMPONENTS REQUIRED
* Arduino Uno Board
* Infrared Remote Controller
* Infrared Receiver 
* LED
* 220ΩResistor
* Breadboard Wire
* USB cable
## CIRCUIT DIAGRAM
![Exp10](https://user-images.githubusercontent.com/85242299/167536671-85390198-7e54-44ed-b394-eb005249aab2.JPG)

## CODE

```
#include <IRremote.h>
const int RECV_PIN = 4;
const int redPin = 3; 
const int yellowPin = 2;

// Define integer to remember toggle state
int togglestate1 = 0;
int togglestate2 =0;

// Define IR Receiver and Results Objects
IRrecv irrecv(RECV_PIN);
decode_results results;


void setup(){
  // Enable the IR Receiver
  irrecv.enableIRIn();
  // Set LED pins as Outputs
  pinMode(redPin, OUTPUT);
  pinMode(yellowPin, OUTPUT);
}


void loop(){
    if (irrecv.decode(&results))
    {

        switch(results.value){
          case 0x1FE48B7: //power buton of my remote
        if(togglestate1==0)
           {
        digitalWrite(yellowPin, HIGH);
        togglestate1=1;
        }
        else {
        digitalWrite(yellowPin, LOW);
        togglestate1=0;
        };
        break;
   
          case 0x1FE50AF: //digit one of my remote
        // Toggle LED On or Off
        if(togglestate2==0){
        digitalWrite(yellowPin, HIGH);
        togglestate2=1;
        }
        else {
        digitalWrite(yellowPin, LOW);
        togglestate2=0;
        }
        break;
        
    }
    irrecv.resume(); 
  }

}

```
## OUTPUT
The leds are turned on as buttons 1-6 of IR(tv) remote is pressed.They are all turned off when button 7 is pressed. 
## OUTPUT VIDEO





https://user-images.githubusercontent.com/85242299/167557138-2770ba05-d7c1-4b81-96b8-792ea829cc40.mp4








# EXP-11 POTENTIOMETER ANALOG VALUE READING

## Potentiometer working principle 
the potentiometer will act as a variable resistor. When you turn the knob, the resistor will increase or decrease, which will also increase or decrease the voltage on the analog pin to which the potentiometer is connected.Arduino Uno has a max voltage of 5V. The voltage on pin A0 will vary from 0V to 5V when you turn the knob.
## Components required 
*Arduino Uno 

*10K Potentiometer

*Breadboard

*Breadboard Jumper Wire

*USB cable
## Circuit diagram
![Exp11](https://user-images.githubusercontent.com/85242299/167537601-25204c40-333d-4218-a833-1621673ee833.JPG)

## Code
```
int potpin=0;// initialize analog pin 0
int ledpin=13;// initialize digital pin 13
int val=0;// define val, assign initial value 0
void setup()
{
pinMode(ledpin,OUTPUT);// set digital pin as “output”
Serial.begin(9600);// set baud rate at 9600
}
void loop()
{
digitalWrite(ledpin,HIGH);// turn on the LED on pin 13
delay(50);// wait for 0.05 second
digitalWrite(ledpin,LOW);// turn off the LED on pin 13
delay(50);// wait for 0.05 second
val=analogRead(potpin);// read the analog value of analog pin 0, and assign it to val 
Serial.println(val);// display val’s value
}

```



## OUTPUT
The data from the potentiometer is displayed on the serial monitor.
## OUTPUT VIDEO


https://user-images.githubusercontent.com/85242299/167548546-cc522347-0bfb-43f3-8e17-61422f36c931.mp4




https://user-images.githubusercontent.com/85242299/167557288-958dd70b-e88d-4a81-8d02-015911fa6728.mp4






# EXP-12 7 SEGMENT DISPLAY

There are two types of seven-segment displays: common anode and common cathode. The Internal structure of each of these types is nearly the identical. However, the polarity of the LEDs and common terminal are different. In most standard cathode seven-segment displays (the one we used in the experiments), all seven LEDs, in addition to a dot LED, have the cathodes connected to pins 8 and pin 3. To use this display, we must connect GROUND to pin 3 and pin 8, then connect +5V to the other pins and make each of the individual segments light up
## Components required
* Arduino Uno Board
* 1-digit LED Segment Display
* 220Ω Resistor
* Breadboard
* Breadboard Jumper Wires
* USB cable


## Circuit diagram
![Exp12](https://user-images.githubusercontent.com/85242299/167537972-a52ffb41-7bdf-4650-87a6-443c460fb3d1.JPG)

## Working
![](https://user-images.githubusercontent.com/95708160/151671959-ccb0767f-dd9d-40ab-b24f-9c0df678d45c.gif)
## Circuit diagram
![](https://user-images.githubusercontent.com/95708160/151667411-61ffe689-8c8e-456f-ad90-0bf2f3145e9c.jpeg)

## Note
I had no 7 segment display with me,thus had to resort to tinkercad circuits simulator.

## Code

```

 int a=7;
int b=6;
int c=5
int d=10;
int e=11;
int f=8;
int g=9;
int dp=4
void digital_0(void) 
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,LOW);
digitalWrite(dp,LOW);
}
void digital_1(void) // display number 1
{
unsigned char j;
digitalWrite(c,HIGH);
digitalWrite(b,HIGH);// turn on segment b
for(j=7;j<=11;j++)// turn off other segments
digitalWrite(j,LOW);
digitalWrite(dp,LOW);// turn off segment dp
}
void digital_2(void) // display number 2
{
unsigned char j;
digitalWrite(b,HIGH);
digitalWrite(a,HIGH);
for(j=9;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
digitalWrite(c,LOW);
digitalWrite(f,LOW);
}
void digital_3(void) // display number 3
{digitalWrite(g,HIGH);
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(dp,LOW);
digitalWrite(f,LOW);
digitalWrite(e,LOW);
}
void digital_4(void) // display number 4
{digitalWrite(c,HIGH);
digitalWrite(b,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
digitalWrite(a,LOW);
digitalWrite(e,LOW);
digitalWrite(d,LOW);
}
void digital_5(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b, LOW);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void digital_6(void) // display number 6
{
unsigned char j;
for(j=7;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(c,HIGH);
digitalWrite(dp,LOW);
digitalWrite(b,LOW);
}
void digital_7(void) // display number 7
{
unsigned char j;
for(j=5;j<=7;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
for(j=8;j<=11;j++)
digitalWrite(j,LOW);
}
void digital_8(void) // display number 8
{
unsigned char j;
for(j=5;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
}
void digital_9(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void setup()
{
int i;// set variable
for(i=4;i<=11;i++)
pinMode(i,OUTPUT);// set pin 4-11as “output”
}
void loop()
{
while(1)
{
digital_0();
delay(1000);
digital_1();
delay(1000);
digital_2();
delay(1000); 
digital_3();
delay(1000);
digital_4();
delay(1000); 
digital_5();
delay(1000); 
digital_6();
delay(1000); 
digital_7();
delay(1000); 
digital_8();
delay(1000); 
digital_9()
delay(500); 
}}

```
## OUTPUT
![](https://user-images.githubusercontent.com/95708160/152190589-b23a24fe-9a7a-4275-ac79-c2042036624a.png)


# ASSIGNMENT 1-Night lamp with LDR and LED

## Working
when the lights fade out the LED should automatically fix the light 

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
![Exp7](https://user-images.githubusercontent.com/85242299/167537990-11dfaccb-0521-44ec-ad4d-9b4d3903d376.JPG)

## CODE
```
int potpin=0;// initialize analog pin 0, connected with photovaristor
int ledpin=11;// initialize digital pin 11, 
int val=0;// initialize variable val
void setup()
{
pinMode(ledpin,OUTPUT);// set digital pin 11 as “output”
Serial.begin(9600);// set baud rate at “9600”
}
void loop()
{
val=analogRead(potpin);// read the value of the sensor and assign it to val
Serial.println(val);// display the value of val
if(val>=1000)
{
  val = 255;
}
else if(val<=990)
  val = 5;
analogWrite(ledpin,val);// set up brightness（maximum value 255）
delay(10);// wait for 0.01 
}
```
## OUTPUT VIDEO






https://user-images.githubusercontent.com/85242299/167557710-d604e18b-1fc1-4094-8255-0b6a9e39a4a0.mp4








# ASSIGNMENT 2-Digital dice using button and 6 LEDs


## Components Required
* Arduino Uno
* 6-LEDs
* push button Switch
* 10K Ohm Resistor
* Connecting Wires
* 6-220K Ohm Resistor

## Connection Setup
![Assign2](https://user-images.githubusercontent.com/85242299/167541050-f24bd9c8-1846-4977-a5c4-3ef96f427490.JPG)



## Code
```
int led1 = 12;
int led2 = 11;
int led3 = 10;
int led4 = 9;
int led5 = 8;
int led6 = 7;
int button = 6;
int val;
int randNum = 0;
void setup() {
  // put your setup code here, to run once:
  randomSeed(analogRead(0));

  pinMode(button,INPUT);

  pinMode(led1,OUTPUT);
  pinMode(led2,OUTPUT);
  pinMode(led3,OUTPUT);
  pinMode(led4,OUTPUT);
  pinMode(led5,OUTPUT);
  pinMode(led6,OUTPUT);

}

void loop() {
  // put your main code here, to run repeatedly:
  val = digitalRead(button);
  if(val==HIGH)
  {
    randNum = random(7,13);
    digitalWrite(randNum,HIGH);
    delay(2000);
    digitalWrite(randNum,LOW);
  }
}


```
## Output VIDEO






https://user-images.githubusercontent.com/85242299/167557951-458e66fa-118c-4199-971e-f76ccd41a442.mp4








