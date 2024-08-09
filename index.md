# Robotic Arm Project
My name is Ishaan and the project I chose was the three-joint robotic arm. Though I had a lot of fun with this project, I faced many challenges throughout building it. For example, while I was building the robotic arm itself, I noticed that the pieces were extremely loose which led to some of the parts falling, disconnecting, etc. However, once I was finally able to complete the base project for my robotic arm, I was able to add two modifications that enhanced my project including a joystick controller and an LCD screen. Despite facing many struggles throughout this project, I was able to get it done just in time and I learned that it is important to never give up even when things might get a bit frustrating. 


You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Ishaan A | Windemere Ranch Middle School | Electrical Engineering | Incoming Freshman

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/LeKKpqejkKc?si=Dfd6N0n9nw5zgl0p" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- Since my previous milestone, the two main things I was able to accomplish include adding a joystick controller and an LCD screen. Both of these are important parts of my project for different reasons. The joystick controller allows me to control the movements of the robotic arm, making it more useful, while the LCD screen adds a necessary aesthetic aspect to my project while acting as a label for it by printing "Ishaan's Robotic Arm 'u'. "
- The biggest challenges I faced a BlueStamp Engineering included making sure I didn't damage any parts of my project and learning how the different aspects and code of my project work.
- The key topics I learned about since the beginning of this project include wiring, a bit of coding, more about servos, and about Arduino in general.
- After everything I have learned at BlueStamp Engineering, I hope to learn more about coding and AI in the future so that I can combine all of these concepts that I have learned and make a project that will be extremely useful to people or our planet as a whole.



# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/j7r1Ijh0hOo?si=aYQR6ZgbX4iHHk58" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- I was able to complete the base project for my robotic arm despite many frustrating moments. Additionally, using Arduino, I was able to code the robotic arm to perform specific movements in a loop. These movements include having the arm move up and down, left and right, forward and backward, and having the claw open and close.
- What has been surprising about the project so far
- One of the previous challenges that I was able to overcome before this milestone include fixing the positioning of the servos and making sure they are tightened. Additionally, I was able to understand what both of the programs do in detail: Lesson 4 code: sets the servos to 90º; Lesson 5 code: has the arm do specific movements in a loop.
- Before my final milestone, I intend to add two modifications to my project which include a joystick controller and an LCD screen.

# First Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/LV171ZL6n2w?si=rpEOUrYEaxE-9ucd" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For your first milestone, describe what your project is and how you plan to build it. You can include:
- So far I have connected 4 servos to my Arduino. 3 of my servos are loosely connected to the Arduino while one of them is connected to 
 the Arduino and another part of my board. By using the Arduino coding platform, I connected the Arduino to my computer with a USB so that the code is implemented into my robotic arm. This code aligns the servos by turning them to a 90º position.
- I have attached my Arduino to the board and the base of my robotic arm. To this base, I have attached a servo which connects to the Arduino. Additionally, there are 3 servos that are not attached to anything and are also connected to the Arduino. By connecting my Arduino to my laptop which has the written code, the servos are aligned by being turned to a 90º position.
- Challenges that I will solve as I move on with my project: handling the loose servos, understanding what the code does in detail, understanding how the new servos will be useful to my robotic arm.
- My plan to complete this project:
  After 2 more days (July 31) I will have completed my robotic arm. Then, for the rest of the week, I will work on brainstorming and implementing my own adjustments to my project. Finally, I will fix any pending issues and prepare for the final milestone.
# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
#include <Servo.h> // add the servo libraries
#include <LiquidCrystal_I2C.h>
#include  <Wire.h>
Servo myservo1; // create servo object to control a servo
Servo myservo2;
Servo myservo3;
Servo myservo4;
int pos1=90, pos2=90, pos3=90, pos4=90; // define the variable of 4 servo angle,and assign the initial value (that is the boot posture
//angle value)
const int right_X = A2; // define the right X pin to A2
const int right_Y = A1; // define the right Y pin to A5
const int right_key = 7; // define the right key pin to 7（that is the value of Z）
const int left_X = A3; // define the left X pin to A3
const int left_Y = A0; // define the left X pin to A4
const int left_key = 8; //define the left key pin to 8（that is the value of Z）
int x1,y1,z1; // define the variable, used to save the joystick value it read.
int x2,y2,z2;
LiquidCrystal_I2C lcd(0x27,  16, 2);
void setup()
{
// boot posture
myservo1.write(pos1);
delay(1000);
myservo2.write(pos2);
myservo3.write(pos3);
myservo4.write(pos4);
delay(1500);
pinMode(right_key, INPUT); // set the right/left key to INPUT
pinMode(left_key, INPUT);
Serial.begin(9600); // set the baud rate to 9600
lcd.init();
// turn on the backlight
lcd.backlight();
delay(1000);
lcd.setCursor(3,0);
  // tell the screen to write “hello, from” on the top  row
  lcd.print("Ishaan's   \"");
  // tell the screen to write on the bottom  row
  lcd.setCursor(2,1);
  // tell the screen to write “Arduino_uno_guy”  on the bottom row
  // you can change whats in the quotes to be what you want  it to be!
  lcd.print("Robotic Arm U");

}
void loop()
{
myservo1.attach(3); // set the control pin of servo 1 to D3  dizuo-servo1-3
myservo2.attach(5); // set the control pin of servo 2 to D5  arm-servo2-5
myservo3.attach(6); //set the control pin of servo 3 to D6   lower arm-servo-6
myservo4.attach(9); // set the control pin of servo 4 to D9  claw-servo-9
x2 = analogRead(right_X); //read the right X value
y2 = analogRead(right_Y); // read the right Y value
z2 = digitalRead(right_key); //// read the right Z value
x1 = analogRead(left_X); //read the left X value
y1 = analogRead(left_Y); //read the left Y value
z1 = digitalRead(left_key); // read the left Z value
//delay(5); // lower the speed overall

// claw
claw();

// rotate
turn();

// upper arm
upper_arm();

//lower arm
lower_arm();


}



//***************************************************
//claw
void claw()
{
//claw
if(x1<50) // if push the left joystick to the right
{
pos4=pos4+3; 
myservo4.write(pos4); //servo 4 operates the motion, the claw gradually opens. 
delay(5);

if(pos4>120) //limit the largest angle when open the claw 
{
pos4=120;
}
}

if(x1>1000) ////if push the right joystick to the left 
{
pos4=pos4-3; 
myservo4.write(pos4); // servo 4 operates the action, claw is gradually closed.
delay(5);
if(pos4<45) // 
{
pos4=45; //limit the largest angle when close the claw
}

}
}



//******************************************************/
// turn
void turn()
{
if(x2<50) //if push the right joystick to the let 
{
pos1=pos1+3; 
myservo1.write(pos1); // arm turns left
delay(5);
if(pos1>180) //limit the angle when turn right 
{
pos1=180;
}

}

if(x2>1000) // if push the right joystick to the right
{
pos1=pos1-3; 
myservo1.write(pos1); //servo 1 operates the motion, the arm turns right. 
delay(5);
if(pos1<1) // limit the angle when turn left
{
pos1=1;
}
}
}




//**********************************************************/
// lower arm
void lower_arm()
{
if(y2>1000) // if push the right joystick downward
{
pos2=pos2-2;
myservo2.write(pos2); // lower arm will draw back
delay(5);
if(pos2<25) // limit the retracted angle
{
pos2=25;
}
}

if(y2<50) // if push the right joystick upward
{
pos2=pos2+2;
myservo2.write(pos2); // lower arm will stretch out
delay(5);
if(pos2>180) // limit the stretched angle
{
pos2=180;
}
}
}





//*************************************************************/

//upper arm
void upper_arm()
{
if(y1<50) // if push the left joystick downward
{
pos3=pos3-2;
myservo3.write(pos3); // upper arm will go down
delay(5);
if(pos3<1) //  limit the angle when go down 
{
pos3=1;
}
}
if(y1>1000) // if push the left joystick upward
{
pos3=pos3+2;
myservo3.write(pos3); // the upper arm will lift
delay(5);

if(pos3>135) //limit the lifting angle 
{
pos3=135;

}
}
}
```

# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
