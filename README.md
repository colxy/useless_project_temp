<img width="1280" alt="readme-banner" src="https://github.com/user-attachments/assets/35332e92-44cb-425b-9dff-27bcf1023c6c">

# parking assistance 🎯


## Basic Details
### Team Name: colxy


### Team Members
- Team Lead: [rahul manoj kt] - [nssce]
- Member 2: [diya rahmath] - [nssce]
- Member 3: [anshad a] - [nssce]

### Project Description
auto gate open with automatic light
### The Problem (that doesn't exist)
power saving
### The Solution (that nobody asked for)
[automated light and gate open system]

## Technical Details
### Technologies/Components Used
For Software:
- [c++]
- [esp32]
- [arduino ide]

For Hardware:
- [esp 32]
- ultrasonic sensor 
- [arduino ide]

### Implementation
For Software:
# Installation
[#include<Servo.h>
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
]


### Project Documentation
For Software:

# Screenshots (Add at least 3)
![Screenshot1](Add screenshot 1 here with proper name)
*Add caption explaining what this shows*

![Screenshot2](Add screenshot 2 here with proper name)
*Add caption explaining what this shows*

![Screenshot3](Add screenshot 3 here with proper name)
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
[Add your demo video link here]
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



