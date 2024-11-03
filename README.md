<img width="1280" alt="readme-banner" src="https://github.com/user-attachments/assets/35332e92-44cb-425b-9dff-27bcf1023c6c">

# [Automated parking] 🎯


## Basic Details
### Team Name: [Colxy]


### Team Members
- Team Lead: [Rahul Manoj K T] - [NSS COLLEGE OF ENGINEERING]
- Member 2: [Diya Rahmath] - [""]
- Member 3: [Anshad A] - [""]

### Project Description
[Automatic gate opening and motion detection controlled light and vehicle counter ]

### The Problem (that doesn't exist)
[lack of employees]

### The Solution (that nobody asked for)
[Automated system ]

## Technical Details
### Technologies/Components Used
For Software:
- [C++]
- [Frameworks used]
- [Wire.h,Servo.h]
  

For Hardware:
- [Arduino Uno,servo,led, ultrasonic sensor,]
  
### Implementation
For Software:#include<Servo.h>
#include <Wire.h>  // Comes with Arduino IDE
#define echoPin 7 // Echo Pin
#define trigPin 8 // Trigger Pin
#define SERVO_PIN 9
#define echopin1 2
#define trigpin1 3
int led1=4; 
int led2=5;
int led3=6;
const int ledPin = 13; 
Servo servo;// the pin that the LED is attached to



long duration, distance; // Duration used to calculate distance
int sensorCounter = 0;   // counter for the number of button presses
int lastsensorDistance = 0;
int setCounter = 20;
int incomingByte;
int hi=sensorCounter;

void setup() {
 Serial.begin (9600);

 pinMode(trigPin, OUTPUT);
 pinMode(echoPin, INPUT);
pinMode(ledPin, OUTPUT);
 pinMode(trigpin1, OUTPUT);
 pinMode(echopin1, INPUT);
pinMode(led1, OUTPUT);
pinMode(led2, OUTPUT);
pinMode(led3, OUTPUT);

servo.attach(SERVO_PIN);   // attaches the servo on pin 9 to the servo object
servo.write(0);
}

void loop() {
if (Serial.available() > 0) {            // see if there's incoming serial data:
  incomingByte = Serial.read();            // read the oldest byte in the serial buffer:
  if (incomingByte == 'R') {              // if it's a capital R, reset the counter
      Serial.println("Reset");
      sensorCounter = 20;

    }
  }

 /* The following trigPin/echoPin cycle is used to determine the
 distance of the nearest object by bouncing soundwaves off of it. */ 
 digitalWrite(trigPin, LOW); 
 delayMicroseconds(2); 

 digitalWrite(trigPin, HIGH);
 delayMicroseconds(10); 

 digitalWrite(trigPin, LOW);
 duration = pulseIn(echoPin, HIGH);

 //Calculate the distance (in cm) based on the speed of sound.
 distance = duration/58.2;
 digitalWrite(trigpin1, LOW); 
 delayMicroseconds(2); 

 digitalWrite(trigpin1, HIGH);
 delayMicroseconds(10); 

 digitalWrite(trigpin1, LOW);
 duration = pulseIn(echopin1, HIGH);

 //Calculate the distance (in cm) based on the speed of sound.
 distance = duration/58.2;
 if ( distance <= 5 )
  {
    digitalWrite(led1, HIGH);
  }
  else
  {
    digitalWrite(led1, LOW);
  }
    if ( distance>5 && distance <= 15)
  {
    digitalWrite(led2, HIGH);
  }
  else
  {
    digitalWrite(led2, LOW);
  }
   if ( distance>15 && distance <= 20)
  {
    digitalWrite(led3, HIGH);
  }
  else
  {
    digitalWrite(led3, LOW);
}
 
 if (distance <= 20 && lastsensorDistance >= 40){
      sensorCounter++;
    Serial.print("number of counts:  ");
    Serial.println(sensorCounter);
   Serial.println(distance);
   if(hi=hi+1)
  {
    servo.write(90);
 delay(5000);
 servo.write(0);
 
  }
   }
   
 else {
  
  //Serial.println("off");   not needed.

  }


  lastsensorDistance = distance;
  delay(200); 


   // turns on the LED when counter is at setCounter 
  if (sensorCounter >= setCounter) {
    digitalWrite(ledPin, HIGH);
    Serial.println("off");
  } else {
   digitalWrite(ledPin, LOW);
  }


# Run


### Project Documentation
For Software:

# Screenshots (Add at least 3)
![Screenshot1](https://drive.google.com/file/d/1M8cys35MOcZDChmFMa9l_46nH6r3vkSd/view?usp=drivesdk)
Hardworking for the project

![Screenshot2]([Add screenshot 2 here with proper name](https://drive.google.com/file/d/1M8cys35MOcZDChmFMa9l_46nH6r3vkSd/view?usp=drivesdk))
*Add caption explaining what this shows*

![Screenshot3]([Add screenshot 3 here with proper name](https://drive.google.com/file/d/1M8cys35MOcZDChmFMa9l_46nH6r3vkSd/view?usp=drivesdk))
*Add caption explaining what this shows*

# Diagrams
![Workflow](Add your workflow/architecture diagram here)
*Add caption explaining your workflow*

For Hardware:

# Schematic & Circuit
![Circuit](Add your circuit diagram here)
*Add caption explaining connections*

![Schematic](Add your schematic diagram here)
*Add caption explaining the schematic*

# Build Photos
![Components](Add photo of your components here)
*List out all components shown*

![Build](Add photos of build process here)
*Explain the build steps*

![Final](Add photo of final product here)
*Explain the final build*

### Project Demo
# Video
[https://youtube.com/shorts/7zs3t12E7I4?si=S8Wql7KKwe6i0XBs]
*Explain what the video demonstrates*

# Additional Demos
[Add any extra demo materials/links]

## Team Contributions
- [Name 1]: [Specific contributions]
- [Name 2]: [Specific contributions]
- [Name 3]: [Specific contributions]

---
Made with ❤️ at TinkerHub Useless Projects 

![Static Badge](https://img.shields.io/badge/TinkerHub-24?color=%23000000&link=https%3A%2F%2Fwww.tinkerhub.org%2F)
![Static Badge](https://img.shields.io/badge/UselessProject--24-24?link=https%3A%2F%2Fwww.tinkerhub.org%2Fevents%2FQ2Q1TQKX6Q%2FUseless%2520Projects)



