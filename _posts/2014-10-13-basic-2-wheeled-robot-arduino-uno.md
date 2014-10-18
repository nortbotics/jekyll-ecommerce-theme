---
layout: post

title: "Make Your Own Basic 2-Wheeled Robot"
subtitle: "simple mobile robot, using an Arduino Uno"
cover_image: blog-cover.jpg
excerpt: "In this project I am creating a simple 2-wheeled robot using the arduino uno. I just want a basic, simple, mobile robot that can be used as a base, or platform, for later mobile robotics experiments."
category: arduino
image: small-mobile-robot.jpg
image-small: small-mobile-robot2.jpg

author_name: Joe Norton
---  
In this project I am creating a mobile robot platform that can be used as a test platform for later mobile robotics projects of mine. I just want a basic, simple, mobile robot. The brains of this little robot will be the Arduino UNO, and the bot will be driven by 2 continuous rotation servos (since I have them on hand, and there's no need to go the DC motor route).

###Parts:###
*  Arduino Uno
*  Sensor Shield  
*  2 Continuous Rotation Servos (Parallax)
*  2 Wheels (Parallax)
*  9 volt battery
*  3D Printed 'Mini-Mo' Small Mobile Robot body

This is an extremely simple project. The tricky part is sourcing an adequate 'robot body'. You can make your own at home, out of cardboard, or other common materials. I have done that, and it's okay as well.

I decided to 3D print my robot body here for this project. I found a nice 'small mobile robot' model on Thingiverse and made that. Side-note: I am working on a modified version, with advanced functionality and additional parts (codenamed 'Mini-Mo').  

<a href="http://www.thingiverse.com/thing:207522">Here is the 3D model on Thingiverse</a>  

Here is how my 3D printed body came out. Not perfect, but it will do.    
<img src="/images/small-mobile-robot-body.jpg">  

##Put it together##
This part really depends on your robot body. Essentially, here are the steps taking place:
1. Attach the 2 servos to the robot body.
2. Attach the Arduino Uno to the robot body.
3. Slap on that sensor shield to the top of the Arduino.
4. Plug in servos - into pins 9 and 10 - on the sensor shield.
5. Marvel at your cute little robot.

The last step here is actually plugging in the power. To do this, just plug the black wire coming off the battery into one of the GRND pins on the Sensor Shield, and put the red wire into the VIN pin on the sensor shield. This will turn ON the robot, so you will maybe want to work a switch in there to make it easier for you - but I'm leaving it out here for simplicity.

##Upload some code##

Here is some xample code for running simple differential drive on the arduino. All we are doing is declaring 2 servos, attached to pins 9 & 10, and then sending them difference coordinated sets of pulses depend on which way we want the wheels to turn.  
{% highlight c %}
/*
Simple Differential Drive Example
Created October 2014 by Joe Norton of NORTBOTICS
LICENSE: CC-BY-SA 4.0
 */

// include the servo library
#include <Servo.h>

Servo servoLeft;  // create a servo object for lefty
Servo servoRight;  // create a servo object for righty

void setup() {
  servoLeft.attach(9); // attaches the servo on pin 9 to the servo object 
   servoRight.attach(10); // attaches the servo on pin 10 to the servo object 
}

void loop() {            // Loop through motion tests
  forward();             // Example: move forward
  delay(2000);           // Wait 2000 milliseconds (2 seconds)
  reverse();
  delay(2000);
  turnRight();
  delay(2000);
  turnLeft();
  delay(2000);
  stopRobot();
  delay(2000);
}

// Motion routines for forward, reverse, turns, and stop
void forward() {
  servoLeft.write(0);
  servoRight.write(180);
}

void reverse() {
  servoLeft.write(180);
  servoRight.write(0);
}

void turnRight() {
  servoLeft.write(180);
  servoRight.write(180);
}
void turnLeft() {
  servoLeft.write(0);
  servoRight.write(0);
}

void stopRobot() { //if your servos keep rolling, it means they need
				// to be aligned
  servoLeft.write(90);
  servoRight.write(90);
}
{% endhighlight %}

Note:
If during the 'stop' phase of the program your servos continue rolling then that means you need to re-align the servos. On the bottom of hobby servos there is a little exposed phillips head recessed nob. You can turn this to fine-tune the servo. You want to turn the screw just enough that it STOPS during the time you at running the above 'stopRobot()'.

##Final Result## 
<a href="https://www.flickr.com/photos/126939770@N02/15345546159" title="mobile-bot by Joe Norton, on Flickr"><img src="https://farm6.staticflickr.com/5609/15345546159_5a2f808899_n.jpg" width="320" height="240" alt="mobile-bot"></a> 
All said and done, here is how the small mobile robot turned out. It's really not much of robot -- pretty much as dumb as a robot can get -- this is because it doesn't actually do any "sensing" of the environment. Now that we have a simple example of differential drive, we can start to incorporate sensory data to do obstacle avoidance and more in later projects.