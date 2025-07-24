Gesture Controlled Robot

A gesture controlled robot. Sounds like a budget sci-fi movie device, existing in a plethora of movies, yet it can exist in our very real world. When I was offered to try and tackle the challenges to create a gesture controlled robot, I knew I had to take the chance. The learning experiences it would provide me would be insanely valuable, so I prepared myself to take the challenge head on. The project consisted of two simple components: a chassis and hand component, yet the hardest part for me was understanding the wiring! It turns out the curse of confusing wiring from Robotics was back to haunt me again.
As I made attempts to perfect the wiring, energy became a new issue, overloading my motor drivers and circuits. Even though these issues had me hitting my head against a wall, I persisted, using different variations to find a wiring more effective for me. After almost a week of trying, I finally knew I found it. Once the base project was complete, I was given the opportunity to look for modifications. To really wrap up this project, I decided acceleration and brake lights were the best way to make this project my own.


You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Arjit S | Issaquah Highschool | Electrical Engineering | Incoming Sophomore

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For this final milestone, I had my eyes set on the code and my modifications. I was right at the end of the tunnel, ready to embrace a completely personal, working project. To start, I decided that it was time to really get the code working. I tested the accelerometer, making sure it was reading the correct coordinates and giving back the correct commands, such as 'f' for forward. Once I was confident it was functional, I looked towards the BlueTooth signaling, tinkering with it to send commands at a steady rate so the robot's Arduino wouldn't go crazy. After making sure it was working, I paired up the two parts and started moving the robot, which worked! 
I was so excited until I realized that my wheels were spinning in incorrect directions. I thought it would be an easy fix: just move the wires connected to the motor drivers, yet it was so much more than that. Days went by where the robot kept making erratic movements, incorrect wheel movement, or even just not working at all, so I knew I needed to really break it down. I took the motor drivers off and tested them rigorously, checking each one to make sure that they were fully functional. It was a breath of fresh air once I knew they were functional, so I decided that I would scrap my Breadboard "substation" idea, giving each motor driver pin their own Arduino pin. This slightly complicated the code, but it worked. My motor drivers were finally functional, so I decided now would be the best time to start my modifications: acceleration and brake lights. The lights were relatively straightforward. I took one of my breadboards and used my final 2 Arduino pins to separate the left lights and right lights, allowing me to add turn indicators (I could flash them on and off when I call a turn function!). For acceleration, however, I needed to look more at my code. 
The reason acceleration is code related is because the motors really only operate at 5V and 0V (On and Off). To bypass this, I used Pulse with Modulation (PWM) to basically turn the motor on and off extremely quickly. This essentially allowed me to slow the motors even more, which made it move slower based on certain commands. I used analog write to enable the PWM, and that would wrap up the project for me!
I have learned a lot from this project, such as coding up Arduinos, BlueTooth connections via HC-05, wiring, and even smaller things like grounding two different power supplies together. It was a great experience to face all these challenges and learn essential debugging skills, while also learning valuable lessons about wiring and proper management of code and Arduino connections. 


# Second Milestone

<iframe width="879" height="494" src="https://www.youtube.com/embed/L-6tVIwTw7c" title="Arjit S Milestone 2" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


In this milestone, I decided that there were two main components I wanted to complete for it: the gesture component and the BlueTooth module pairing. Arguably, the BlueTooth module pairing is the most significant, as it is a huge part in the communication between the gesture component and the robot. To create the gesture control portion, I wired up all the components together to make them work. Once I plugged in the batteries, I knew that my wiring was successful because of the red glow of the LED's. Now, this is where the complicated stuff came into place. BlueTooth wiring. 
First, I had to correctly wire the BlueTooth modules (Specifically RX and TX pins --- related to transmission and receival of digital signals) to the Arduino Nano and Uno, forcing me to change my wiring. I struggled to fit my fingers through the gaps of all my other wiring, shoving Ohms resistors into the correct pins to have a good voltage for the BlueTooth module. I even had to demolish my gesture component and move it to a longer breadboard, since the one I wanted to use it on was too tiny to fit the correct wiring for the BlueTooth module. 
After getting the base wiring complete, I needed to figure out why my BlueTooth modules weren't remaining in AT command mode, which was essential to move forward with my pairing. It turns out, however, I needed to adjust my wiring of the BlueTooth module connected to my Arduino Uno, because the ground voltage for the power module and the Uno were actually slightly different, creating discrepancies in power that was received. Once I made that fix, the BlueTooth module started flashing properly, signaling a correct connection. After confirming correct wiring and code, I managed to synthesize a proper connection between the modules, confirming it with the simple message "hi" displaying in the opposite Serial Monitor! For my final milestone, I really want to complete my code and modifications, since they are the last remaining steps for me to take before I can truly call this project complete.


# First Milestone

<iframe width="879" height="494" src="https://www.youtube.com/embed/O0JBTSoajUw" title="Arjit S Milestone 1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

As I started trying to comprehend the massive project I chose, I decided to set my first milestone to something simple: build my robot. I gathered up the courage to lift open the lid to the medium size box, revealing the chassis just waiting for me to assemble it. I grabbed the two bases and poured out all the shafts, screws and wheels. It seemed so simple, yet it took me almost 2 hours just to assemble it. 
I started by first getting the motors on, but after I did that, I realized I used the wrong motors. They didn't have wires that I could connect to my motor drivers. I disassembled the pieces holding the motors one by one, glad my teacher helped me catch this mistake before I essentially closed off that area of the chassis. Another small issue I faced after the motor disaster was the 2nd base of the chassis. I put it the wrong way, almost cracking the plastic, before realizing that I had it flipped. 
I noticed this because I saw 4 holes on the left side, whereas there were 3 on the right, signs that suggested the correct way to assemble it. After getting over the kinks, I started placing my Arduino Uno, breadboards, and motor drivers, using my past experiences with wiring in FTC Robotics to avoid poor wire management. After getting the Arduino set up, I decided to tackle the task of wiring the BlueTooth module and the motor drivers. After much trial and error of moving around components for ease of mind, I decided on a layout that placed the Arduino and breadboard on opposite sides, while the motor drivers stayed on the sides. After wiring up everything, I ran the code and saw that my wiring had been successful in moving the motors! I decided that the next logical step for me would be to start building the gesture component and managing the BlueTooth connections between modules.

# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 
*Wiring for the BlueTooth module for the hand component*
<img width="964" height="810" alt="image" src="https://github.com/user-attachments/assets/50157b3b-4a64-4ea9-bf40-5e3a4edec45e" />
*Wiring of the Arduino Uno, the BlueTooth module, and the motor driver(s). The motor driver in the image is essentially two L9110 H-Bridge as one*
<img width="1281" height="872" alt="image" src="https://github.com/user-attachments/assets/0c22f59a-6e74-4466-b03f-b9b014da53c0" />
*Wiring of the HC-05 BlueTooth Module to the Arduino Uno to enable the connection*
<img width="1641" height="1080" alt="image" src="https://github.com/user-attachments/assets/8bc0f7a6-9c2c-43e4-b8f5-dd75a96c2eba" />
*Wiring of the HC-05 BlueTooth Module to the Arduino Nano to enable the connection*
<img width="1672" height="1022" alt="image" src="https://github.com/user-attachments/assets/2273af2c-88d4-4278-b5b5-eee5c319ae0c" />



# Code
```c++
HAND CODE:

#include <SoftwareSerial.h>
const int rx = 3;

const int tx =2;

char dir;


int distance = 0; 
SoftwareSerial BT_Serial(rx, tx);


//available (BT_Serial) - if there are bytes available on buffer ready to be processed to be sent to Arduino

#include <Wire.h> // I2C communication library

const int MPU = 0x68; // I2C address of the MPU6050 accelerometer
int16_t AcX, AcY, AcZ;

int flag=0;


void setup () {// put your setup code here, to run once

Serial.begin(38400); // start serial communication at 9600bps
BT_Serial.begin(38400); 

// Initialize interface to the MPU6050
Wire.begin();
Wire.beginTransmission(MPU);
Wire.write(0x6B);
Wire.write(0);
Wire.endTransmission(true);

delay(500); 
}

void loop () {
//BT_Serial.write('f');
Read_accelerometer(); // Read MPU6050 accelerometer
/*
if(AcX<70  && flag==0){flag=1; BT_Serial.write('f');}
if(AcX>130 && flag==0){flag=1; BT_Serial.write('b');}
      
if(AcY<60  && flag==0){flag=1; BT_Serial.write('l'); }
if(AcY>110 && flag==0){flag=1; BT_Serial.write('r');}
*/

if ((AcX > 35 && AcX < 70) &&flag == 0) {
  flag = 2; 
  BT_Serial.write('f');
  Serial.write('f');
  Serial.write('\n');
  delay(100);
} else if ((AcX > 0 && AcX <= 35) && flag == 2) {
  flag = 1; 
  BT_Serial.write('g'); // going fast
  Serial.write('g');
  Serial.write('\n');
  delay(100);
} else if ((AcX > 130 && AcX < 150) && flag == 0) {
  flag = 2; 
  BT_Serial.write('b');
  Serial.write('b');
  Serial.write('\n');
  delay(100);
} else if ((AcX >= 150) && flag == 2) {
  flag = 1; 
  BT_Serial.write('v'); // very backwards
  Serial.write('v');
  Serial.write('\n');
  delay(100);
} else if ((AcY > 35 && AcY < 60) && flag == 0) {
  flag = 2; 
  BT_Serial.write('l');
  Serial.write('l');
  Serial.write('\n');
  delay(100);
} else if ((AcY > 0 && AcY <= 35) && flag == 2) {
  flag = 1; 
  BT_Serial.write('k'); // hard left
  Serial.write('k');
  Serial.write('\n');
  delay(100);
} else if ((AcY > 110 && AcY < 130) && flag == 0) {
  flag = 2; 
  BT_Serial.write('r');
  Serial.write('r');
  Serial.write('\n');
  delay(100);
} else if ((AcY >= 130) && flag == 2) {
  flag = 1; 
  BT_Serial.write('q'); // quick right
  Serial.write('q');
  Serial.write('\n');
  delay(100);
} else if ((AcX > 90 && AcX < 120) && (AcY > 80 && AcY < 110) && (flag == 1 || flag==2)) {
  flag = 0;
  BT_Serial.write('s');
  
  Serial.write('\n');
  delay(100);  
}

}

void Read_accelerometer(){
      // Read the accelerometer data
Wire.beginTransmission(MPU);
Wire.write(0x3B); // Start with register 0x3B (ACCEL_XOUT_H)
Wire.endTransmission(false);
Wire.requestFrom(MPU, 6, true); // Read 6 registers total, each axis value is stored in 2 registers

AcX = Wire.read() << 8 | Wire.read(); // X-axis value
AcY = Wire.read() << 8 | Wire.read(); // Y-axis value
AcZ = Wire.read() << 8 | Wire.read(); // Z-axis value

AcX = map(AcX, -17000, 17000, 0, 180);
AcY = map(AcY, -17000, 17000, 0, 180);
AcZ = map(AcZ, -17000, 17000, 0, 180);
/*
Serial.print(AcX);
Serial.print("\t");
Serial.print(AcY);
Serial.print("\t");
Serial.println(AcZ); 
delay(100);
*/

}

ROBOT CODE: 

#include <SoftwareSerial.h>
const int rx = 3;

const int tx =2;

SoftwareSerial BT_Serial(rx, tx);

//BAUD RATE HAS TO BE 38400!!
//BT_Serial is for the connection between Arduino and BlueTooth
//Serial is Computer to Arduino

//#define enA 10//Enable1 L298 Pin enA 
#define in1 6 //MOTOR FRONT RIGHT (A) PIN (POSITIVE PIN) //FORWARDS PIN
#define in2 7 //MOTOR FRONT RIGHT (A) PIN (NEGATIVE PIN) //BACKWARDS PIN 

#define in3 8 //MOTOR FRONT LEFT (B) PIN (NEGATIVE PIN) //FORWARDS PIN
#define in4 9 //MOTOR FRONT LEFT (B) PIN (POSITIVE PIN) //BACKWARDS PIN

#define in5 10 //MOTOR BACK RIGHT (B) PIN (POSITIVE PIN) //FORWARDS PIN
#define in6 11 //MOTOR BACK RIGHT (B) PIN (NEGATIVE PIN) //BACKWARDS PIN

#define in7 4 //MOTOR BACK LEFT (A) PIN (NEGATIVE PIN) //FORWARDS PIN
#define in8 5 //MOTOR BACK LEFT (A) PIN (POSITIVE PIN) //BACKWARDS PIN

#define ledPinRight 12 //LED PIN ON THE RIGHT
#define ledPinLeft 13 //LED PIN ON THE LEFT

//#define enB 5 //Enable2 L298 Pin enB 

bool turning = false;
char bt_data = ""; // variable to receive data from the serial port
int Speed; //Write The Duty Cycle 0 to 255 Enable Pins for Motor Speed  

void setup() { // put your setup code here, to run once



Serial.begin(38400); // start serial communication at 9600bps
//BT_Serial.setTimeout(50);
BT_Serial.begin(38400); 

//pinMode(enA, OUTPUT); // declare as output for L298 Pin enA 
pinMode(in1, OUTPUT); // declare as output for L298 Pin in1 
pinMode(in2, OUTPUT); // declare as output for L298 Pin in2 
pinMode(in3, OUTPUT); // declare as output for L298 Pin in3   
pinMode(in4, OUTPUT); // declare as output for L298 Pin in4 
pinMode(in5, OUTPUT);
pinMode(in6, OUTPUT);
pinMode(in7, OUTPUT);
pinMode(in8, OUTPUT);
pinMode(ledPinRight, OUTPUT);
pinMode(ledPinLeft, OUTPUT);
/*
Serial.println("forward");
forward(255);
delay(5000);
Stop();
delay(255);
Serial.println("backward");
backward(255);
delay(5000);
Serial.println("right");
turnRight(255);
delay(5000);
Serial.println("left");
turnLeft(150);
delay(5000);
Stop();
Serial.println("stop");
*/
//delay(2550);
//backward();



//pinMode(enB, OUTPUT); // declare as output for L298 Pin enB 

delay(200);
}

void loop(){
     
  if(BT_Serial.available() > 0){  //if some date is sent, reads it and saves in state     
    bt_data = BT_Serial.read(); 
    Serial.println(bt_data);          
  }


  if(bt_data == 'f'){
    turning = false;
    forward(255); 
    ledsOff();
  }  // if the bt_data is 'f' the DC motor will go forward
  else if (bt_data == 'g'){
    turning = false;
    forward(255);
    ledsOff();
  }
  else if(bt_data == 'b'){
    turning = false;
    backward(255);
    ledsOff(); 
  }  // if the bt_data is 'b' the motor will Reverse
  else if(bt_data == 'v'){ 
    turning = false;
    backward(255); 
    ledsOff();
  } 
  else if(bt_data == 'l'){
    turning = true;
    leftLeds();
    turnLeft(255); 
  }   // if the bt_data is 'l' the motor will turn left
  else if(bt_data == 'k'){
    turning = true;
    leftLeds();
    turnLeft(255); 
  } 
  else if(bt_data == 'r'){
    turning = true;
    rightLeds();
    turnRight(255);
  } // if the bt_data is 'r' the motor will turn right
  else if(bt_data == 'q'){
    turning = true;
    rightLeds();
    turnRight(255); 
  } 
  else if(bt_data == 's'){
    turning = false;
    ledsOn();
    Stop(); 
  } 

// if the bt_data 's' the motor will Stop
//analogWrite(enA, Speed); // Write The Duty Cycle 0 to 255 Enable Pin A for Motor1 Speed 
//analogWrite(enB, Speed); // Write The Duty Cycle 0 to 255 Enable Pin B for Motor2 Speed 
delay(50);
}
/*
#define in1 6 //MOTOR FRONT RIGHT (A) PIN (POSITIVE PIN) //FORWARDS PIN
#define in2 7 //MOTOR FRONT RIGHT (A) PIN (NEGATIVE PIN) //BACKWARDS PIN 

#define in3 8 //MOTOR FRONT LEFT (B) PIN (POSITIVE PIN) //FORWARDS PIN
#define in4 9 //MOTOR FRONT LEFT (B) PIN (NEGATIVE PIN) //BACKWARDS PIN

#define in5 10 //MOTOR BACK RIGHT (B) PIN (POSITIVE PIN) //FORWARDS PIN
#define in6 11 //MOTOR BACK RIGHT (B) PIN (NEGATIVE PIN) //BACKWARDS PIN

#define in7 4 //MOTOR BACK LEFT (A) PIN (POSITIVE PIN) //FORWARDS PIN
#define in8 5 //MOTOR BACK LEFT (A) PIN (NEGATIVE PIN) //BACKWARDS PIN
*/
/*
void forward(){
  digitalWrite(in1, HIGH);
  digitalWrite(in2, LOW);
  //THIS MOTOR GOES OPPOSITE BUT WHY DOES IT WORK...?
  digitalWrite(in3, LOW);
  digitalWrite(in4, HIGH);

  digitalWrite(in5, LOW);
  digitalWrite(in6, HIGH);
  //THIS GOES OPPOSITE BUT WHY DOES IT WORK...?
  digitalWrite(in7, LOW);
  digitalWrite(in8, HIGH);
}

//THIS TURNS RIGHT
//void backward(){ //backword





//void turnRight(){
void turnRight(){ //turnRight
//LEFT MOTOR
  digitalWrite(in1, LOW);
  digitalWrite(in2, LOW);
//RIGHT MOTOR
  digitalWrite(in3, LOW);
  digitalWrite(in4, HIGH);
//LEFT MOTOR
  digitalWrite(in5, LOW);
  digitalWrite(in6, LOW);
//RIGHT MOTOR
  digitalWrite(in7, LOW);
  digitalWrite(in8, HIGH);
}

//THIS GOES FORWARD
//void turnLeft(){ //turnLeft

void turnLeft(){
  digitalWrite(in1, HIGH);
  digitalWrite(in2, LOW);
//RIGHT MOTOR
  digitalWrite(in3, LOW);
  digitalWrite(in4, LOW);
//LEFT MOTOR
  digitalWrite(in5, LOW);
  digitalWrite(in6, HIGH);
//RIGHT MOTOR
  digitalWrite(in7, LOW);
  digitalWrite(in8, LOW);
}


void Stop(){ //stop
digitalWrite(in1, LOW); //Right Motor forward Pin 
digitalWrite(in2, LOW); //Right Motor backward Pin 
digitalWrite(in3, LOW); //Left Motor backward Pin 
digitalWrite(in4, LOW); //Left Motor forward Pin
digitalWrite(in5, LOW); //Right Motor forward Pin 
digitalWrite(in6, LOW); //Right Motor backward Pin 
digitalWrite(in7, LOW); //Left Motor backward Pin 
digitalWrite(in8, LOW); 
}


void motorTest(){
  digitalWrite(in5, HIGH);
  digitalWrite(in6, LOW);
  digitalWrite(in7, HIGH);
  digitalWrite(in8, LOW);

}
*/

void forward(int speed) {
  // Front motors forward
  analogWrite(in1, speed);    digitalWrite(in2, LOW);   // FR
  digitalWrite(in3, LOW);     analogWrite(in4, speed);  // FL

  // Back motors reversed to go forward
  analogWrite(in5, LOW);    digitalWrite(in6, speed);   // BR reversed
  digitalWrite(in7, LOW);     analogWrite(in8, speed);  // BL reversed
}
/*
void backward(){
  digitalWrite(in1, LOW);
  digitalWrite(in2, HIGH);

  digitalWrite(in3, HIGH);
  digitalWrite(in4, LOW);

  digitalWrite(in5, HIGH);
  digitalWrite(in6, LOW);

  digitalWrite(in7, HIGH);
  digitalWrite(in8, LOW);
}
*/
void backward(int speed) {
  // Front motors backward
  digitalWrite(in1, LOW);     analogWrite(in2, speed);  // FR
  analogWrite(in3, speed);    digitalWrite(in4, LOW);   // FL

  // Back motors forward (inverted to match front)
  digitalWrite(in5, speed);     analogWrite(in6, LOW);  // BR
  analogWrite(in7, speed);    digitalWrite(in8, LOW);   // BL
}

void turnLeft(int speed) {
  // Right side forward
  analogWrite(in1, speed);    digitalWrite(in2, LOW);   // FR
  digitalWrite(in3, LOW);     digitalWrite(in4, LOW);   // FL off

  // Right side back reversed
  analogWrite(in5, LOW);    digitalWrite(in6, speed);   // BR reversed
  digitalWrite(in7, LOW);     digitalWrite(in8, LOW);   // BL off
}

void turnRight(int speed) {
  // Left side forward
  digitalWrite(in1, LOW);     digitalWrite(in2, LOW);   // FR off
  digitalWrite(in3, LOW);     analogWrite(in4, speed);  // FL

  // Left side back reversed
  digitalWrite(in5, LOW);     digitalWrite(in6, LOW);   // BR off
  digitalWrite(in7, LOW);     analogWrite(in8, speed);  // BL reversed
}

void Stop() {
  digitalWrite(in1, LOW); digitalWrite(in2, LOW);
  digitalWrite(in3, LOW); digitalWrite(in4, LOW);
  digitalWrite(in5, LOW); digitalWrite(in6, LOW);
  digitalWrite(in7, LOW); digitalWrite(in8, LOW);
}

void ledsOn(){
  digitalWrite(ledPinRight, HIGH);
  digitalWrite(ledPinLeft, HIGH);
}
void ledsOff(){
  digitalWrite(ledPinRight, LOW);
  digitalWrite(ledPinLeft, LOW);
}
void leftLeds(){
  digitalWrite(ledPinRight, LOW);
    digitalWrite(ledPinLeft, HIGH);
    delay(100);
    digitalWrite(ledPinLeft, LOW);
    delay(100);
    digitalWrite(ledPinLeft, HIGH);
    delay(100);
    digitalWrite(ledPinLeft, LOW);


}
void rightLeds(){
  digitalWrite(ledPinLeft, LOW);

    digitalWrite(ledPinRight, HIGH);
    delay(100);
    digitalWrite(ledPinRight, LOW);
    delay(100);
    digitalWrite(ledPinRight, HIGH);
    delay(100);
    digitalWrite(ledPinRight, LOW);
}
```

# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Arduino Uno | Runs the code from the Robot code and sends signals based on received commands | $27.60 | <a href="https://tinyurl.com/2s2zrzbj"> Link </a> |
| Arduino Nano | Runs the code for the Hand component | $25.70 | <a href="https://tinyurl.com/32v722dz"> Link </a> |
| HC-05 BlueTooth Module | Acts as communicator between the Robot and Hand Component | $9.99 | <a href="[[https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://shorturl.at/kUeho)](https://www.amazon.com/DSD-TECH-HC-05-Pass-through-Communication/dp/B01G9KSAF6/ref=sr_1_4?crid=12F9GUCIPVERI&dib=eyJ2IjoiMSJ9.GVe7xTdQBd8ycP5WU8ZbidhD9NopmyDUD7WkBNR1188mQkgI8cLOSBabxDQpXHFsE7Mwg1CWAJ55vz6-95weGMg5HrbUY4-qtllrl23IgfqOJbNufodrZ4La_0qfwCNBeQNZtAJtYksnSQbKZZVjSfZ5HBJKbrrAcoTwyECOfByKJ1skxEPFS1FqjA6wZTQXGb15yI8qFdxegq8gi-KBUQ_Fsac1okAqspJBhV3zWxJOWzKA5uOK6JYEkl0jL8wK2ylysqMWnUPXG9_MYwezDAQzZVMtlmpYrVnDT7oHlSo.GwY9VEuvt0tBRBygpJ_tOdIrZJSWoUt-j8pq2a1oafY&dib_tag=se&keywords=HC05&qid=1753390476&s=toys-and-games&sprefix=hc05%2Ctoys-and-games%2C189&sr=1-4)"> Link </a> |
| Robot Base Chassis | The base needed to mount your Arduino Uno, breadboard (if necessary), BlueTooth Module, and Motor driver | $19.99 | <a href="[[https://tinyurl.com/2s2zrzbj](https://shorturl.at/zRonm)](https://www.amazon.com/perseids-Chassis-Encoder-Wheels-Battery/dp/B07DNXBFQN/ref=sr_1_10?crid=26TUUFVPI4E3P&dib=eyJ2IjoiMSJ9.b6A_uqlNY7c_XNSLuXfmFx3lnf3nSeLGG7KgC7ZRfC9FAK22FT6M83V1dTBEAvnkHgRE0NNpo0oADYqyV4P2HpY5BFGlLS5OXcRD4aEW4oZsKRGeNyx6VCcRs7hoENdwnlQ8hLuKGPpRNYNJns2n3xydphLJvzrAHjoARmRiwPmFpghbM1R-1qsX5oLcwUgeikl74r8tSpjraJ1ymDeFdq6Kf9PpSFMZnd112Ga4ex0Q4MCaQT605Nzcs1spfnEG27m1GZgqWH8y7CDjJa2srdlHjoSkiJWC8MTTn3ug0Zg.7oE32LVlD_UTGvu8buwQxem0Dpe5zyabMMu1Q39WiQs&dib_tag=se&keywords=robot%2Bchassis&qid=1715357415&s=toys-and-games&sprefix=robot%2Bchassi%2Ctoys-and-games%2C95&sr=1-10&th=1&qty=1&sbo=RZvfv%2F%2FHxDF%2BO5021pAnSA%3D%3D)"> Link </a> |
| Solderless Breadboard + Wires | Provides wires for component connection and a BreadBoard for additional space (if necessary) | $9.99 | <a href="[[https://tinyurl.com/2s2zrzbj](https://shorturl.at/WvhCy)](https://www.amazon.com/BOJACK-Values-Solderless-Breadboard-Flexible/dp/B08Y59P6D1/ref=sr_1_1_sspa?dib=eyJ2IjoiMSJ9.5Z5yTwL-oa1r18Ah_zf9OdziZtM7NtJzJKlf3z7Il1TC4ucBmVtlG0Sv0dLD90gXbMaEKYO4hjSdUtSisLE6JE2c7mHD8E6rCkNp3wSrDgL6m1mWCNCvVMRlWoqY0bIIebbeflSe8rm2h8YNMPydgZ4waCtMxzOe6MvanOMs54wa8YpNTlEU4Dw6nfDF3AXoQenVhZH0C3DSa7nZpOgeLfaurM45_Q6g-T4bsAIaUe4.g3R9ybfxC9NK_ckWS7BxW7IZognzcop7kcYAdf0aeyI&dib_tag=se&keywords=solderless+breadboard&qid=1753389935&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1)"> Link </a> |
| IMU (Inertial Measurement Unit) | Positioning (Angular) readings that are then translated to movement in the code | $10.99 | <a href="[[[https://tinyurl.com/2s2zrzbj](https://shorturl.at/irqai)](https://tinyurl.com/4hpejjkp)](https://www.amazon.com/HiLetgo-MPU-6050-Accelerometer-Gyroscope-Converter/dp/B00LP25V1A/ref=sr_1_3?crid=1YLYMACXT04PZ&dib=eyJ2IjoiMSJ9.G2nP10hLyx2tJvwVwHgV4YxUQ_Da48Puh43G4GcQltriJeG7UYsB1HIu_geL3ArDkoFDhfOxe7VLSmFLLfIzmG1sBliaSm8h5XoEI9vfsqyJsx_l1y3Ixa6p9w6NebxAirnCP-yB63dqeTs3IIQjOCDrRyzj_eQJllk853rk7PvDeXJC6il3UlAGh0XSvkv0Y5v8ZXF8BfPMGeB94ia6BOTRlii2AsyMpWgB_a4Fv3A.TuAe-MkvWQg3zjlCluD_SgiP49BRieLwtgV3vWLxYUM&dib_tag=se&keywords=IMU&qid=1753390030&sprefix=imu%2Caps%2C229&sr=8-3&th=1)"> Link </a> |
| 9V Batteries | Power for the hand and robot component | $12.69 | <a href="[[[https://tinyurl.com/2s2zrzbj](https://shorturl.at/OZk6w)](https://rb.gy/a4zt3e)](https://www.amazon.com/Amazon-Basics-Performance-All-Purpose-Batteries/dp/B00MH4QM1S/ref=sr_1_1_ffob_sspa?crid=1LG0CO2F61QYH&dib=eyJ2IjoiMSJ9.UTIEEJxrXzAacW7rXzP5bXFvszvSx_otce2PCabeOMsG5wY2C_hXLq0UV83evcYMB6ol80Eq3fm1lpKxVIW6Gi_Jx885pYHbU2qtR5wxy9RNON6NZo0ZsM2cA4mus06sQlMc8ti7WDyhAXVc9oKPzjbz4XsAw1lrPswtAEgdNiRG3M2aKAUwU1YrBUXBQjj4hnOaBFR5whZkVsJO0bhU2cwwrAAS35aadw1IMSh10jDxF0tmwOmV7SKujO3aB09lOgf-D8KZ6zJ4XinM_4vLRcgAFFXYia_P-goYljGv2PU.BwSrghlS7goydohdenx-Rh2iJu084v06ZQZKyCojUf0&dib_tag=se&keywords=9V%2BBattery&qid=1753390140&rdc=1&sprefix=9v%2Bbattery%2Caps%2C193&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1)"> Link </a> |
| USB A to B Wire | Connects the Arduino Uno to your computer with a USB port | $10.99 | <a href="[https://tinyurl.com/2s2zrzbj](https://www.amazon.com/Printer-Cable-Scanner-Canon-Lexmark/dp/B084TLQ6R6/ref=sr_1_1_sspa?crid=OTOJUCNWE16A&dib=eyJ2IjoiMSJ9.bCBJMqo5p_qtLjShMZULkMHBEqbL6KjSu_Qh9Abr2OnSan9yvYh09w10tmWfl9FtTJVU-9W30PfQrm7hrRNwYMEEjU1TwkDkyStaBRwNFfYwZ3RBTEAf3izQbMOy4eO8aHtxDqWejsci1vpJQcFc0WEP2VyLIh8lngCiGbGYjfBwXI35rEB71qiqHaKSqqjNHwwiB2uNjQcFvZrpyEr-KkbiPck8ijQJdc8RiL9riXr5h0NfVcnLY3BSG2UwcWsexLMw3RvVJa-ROcDgzcK8uqfnn8SIqQLv79vmeIiygXo.aNfHbSCLnMcAqwEzImG4R5sA7VxytsodJvk9JLbVCdQ&dib_tag=se&keywords=USB%2BA%2Bto%2BB%2Bwire&qid=1753390558&s=electronics&sprefix=usb%2Ba%2Bto%2Bb%2Bwire%2Celectronics%2C347&sr=1-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1)"> Link </a> |
| USB A to mini B Wire | Connects the Arduino Nano to your computer with a USB Port | $8.99 | <a href="[https://tinyurl.com/2s2zrzbj](https://www.amazon.com/Mini-USB-Cable-2-0-Compatible/dp/B08NZZ4WHM/ref=sr_1_2_sspa?dib=eyJ2IjoiMSJ9.fdyh4FhYioLnQ4T14m2BR4za5OtkprQ9-J-LL-oubA7RxPPNeiURnNttJV2n-2XBe_UNF4LqyhNsz-4u1HA2i52bMC7ZGUUeqd8kUE4rUL6XyZe-v67fSsAtSW6jFvh8gbmfkDNQz8BO9TJMLPvdkK97umlXsO9JgWMp6sz-wbd41bH1UZmg8UZRNk3lNrpbDeHJfxZGARsvC3qBgdyrwudXs_DgcRSZFF3iaJNiXH4.4hj379ositcmofT6clRKbwqyUmu2Afb3i-KsnVHLf60&dib_tag=se&keywords=USB%2BA%2Bto%2Bmini%2Bb&qid=1753390640&sr=8-2-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1)"> Link </a> |


