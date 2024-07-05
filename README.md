Engineering materials
====

This repository contains engineering materials of a self-driven vehicle's model participating in the WRO Future Engineers competition in the season 2024.

## Content

* `t-photos` contains 2 photos of the team (an official one and one funny photo with all team members)
* `v-photos` contains 6 photos of the vehicle (from every side, from top and bottom)
* `video` contains the video.md file with the link to a video where driving demonstration exists
* `schemes` contains one or several schematic diagrams in form of JPEG, PNG or PDF of the electromechanical components illustrating all the elements (electronic components and motors) used in the vehicle and how they connect to each other.
* `src` contains code of control software for all components which were programmed to participate in the competition
* `models` is for the files for models used by 3D printers, laser cutting machines and CNC machines to produce the vehicle elements. If there is nothing to add to this location, the directory can be removed.
* `other` is for other files which can be used to understand how to prepare the vehicle for the competition. It may include documentation how to connect to a SBC/SBM and upload files there, datasets, hardware specifications, communication protocols descriptions etc. If there is nothing to add to this location, the directory can be removed.

## Introduction
## Team Members:
Sara Jawaada,designer, software developer -email:sarajawaada906@gmail.com

Amro Duhaidi ,software developer -email:amro.duaidi@gmail.com

Tala Daraghmeh ,software developer, social media manager -email:taladaraghmeh836@gmail.com
## coach name:
Eng.Mohammad Muamar

moh.mummar@gmail.com

A Palestinian engineer and graduate of Palestine Polytechnic University in Hebron, We take pride in being a student of esteemed professors who hold Palestinian degrees and offer expertise of global standards. Our heartfelt gratitude goes to our teacher and mentor, Mohammad Muammar, for his unwavering efforts and support throughout our journey in this competition.
# KufiyaTech team's social accounts

https://linktr.ee/kufiyatech
# Description:
From the heart of the land of olives and resilience, our ambition and passion as Palestinian students have flourished. We aspire to represent our country in the best light possible. This is our compass, this was our goal, and this is what aided us in achieving it at the purpose academy, specializing in robotics and artificial intelligence, located in the economic capital of Palestine, Ramallah.
Welcome to our journal. Here, you will journey with us as we construct our robot from scratch. We are three Palestinian students (Tala, Sarah, Amro), brought together by our shared passion for technology. Our aim is singular: to integrate artificial intelligence, 3D design, programming, and more into a single robot. Under the guidance and training of Engineer Mohammed Maumar, Palestinian efforts over three months came together to build this robot.
# Overview 

Our rear-wheel-drive car used three ultrasonic sensors to avoid obstacles and the internal and external walls of the track. In addition, we applied a PID controller. We used a Pixy2 camera to detect red and green traffic signs. A color sensor was used to verify the color of the lines on the map, and based on the color, the robot determined its direction: if the sensor detected a blue line, the robot moved counterclockwise, and if the sensor detected an orange line, the robot moved clockwise. We used an IMU to obtain the coordinates of the car's location, a servo motor to steer the car in the steering system, and a DC motor connected to a motor driver to control the car's forward and backward movement, providing propulsion. A 12V battery with a voltage regulator was used to distribute the necessary voltage to all components.

## Parts list
## *Raspberry Pi 4:
https://www.raspberrypi.com/products/raspberry-pi-4-model-b/

The Raspberry Pi 4 is a versatile single-board computer equipped with a quad-core Cortex-A72 processor, up to 8GB of RAM, dual HDMI ports, USB 3.0 and USB 2.0 ports, and Gigabit Ethernet. It includes a 40-pin GPIO header for connecting various peripherals and built-in Wi-Fi and Bluetooth for wireless communication, making it ideal for numerous applications in education, robotics, and DIY projects.
## *Arduino Uno:
https://store.arduino.cc/products/arduino-uno-rev3

The Arduino Uno is a popular microcontroller board based on the ATmega328P. It features 14 digital input/output pins, 6 analog inputs, a USB connection, a power jack, and a reset button. Ideal for beginners and experienced developers, it's widely used for creating interactive projects and prototypes.
## *The L298N Motor Driver:
https://components101.com/modules/l293n-motor-driver-module

The L298N Motor Driver module facilitates bidirectional control of DC motors or stepper motors with four input pins for direction and two enable pins for speed regulation via PWM. It's popular in robotics and DIY projects for its built-in protection diodes and wide motor voltage compatibility (7V to 35V), ensuring robust and flexible motor control solutions.
## *Servo motor MG995:
https://components101.com/motors/mg90s-metal-gear-servo-motor

The MG995 Servo Motor is renowned for its precise angular position control using PWM signals. Operating between 4.8V to 7.2V, it delivers significant torque, making it ideal for robotics and mechanical applications requiring accurate and controlled movements.
## *pixy2 camera:
https://pixycam.com/pixy2/

Pixy2 is smaller, faster and more capable than the original Pixy.  Like its predecessor, Pixy2 can learn to detect objects that you teach it, just by pressing a button.  Additionally, Pixy2 has new algorithms that detect and track lines for use with line-following robots.  The new algorithms can detect intersections and “road signs” as well. The road signs can tell your robot what to do, such as turn left, turn right, slow down, etc.  And Pixy2 does all of this at 60 frames-per-second, so your robot can be fast, too.
## *MPU-9250:
https://learn.sparkfun.com/tutorials/mpu-9250-hookup-guide/all

The MPU-9250 is an integrated motion-tracking sensor module that combines a gyroscope, accelerometer, and magnetometer. It is widely used for precise measurement of orientation, acceleration, and magnetic fields in applications ranging from drones and robotics to wearable devices.
## *HC-SR04 Ultrasonic Sensor:
https://www.sparkfun.com/products/15569

The HC-SR04 Ultrasonic Sensor uses ultrasonic waves to determine distances by measuring the time taken for the waves to reflect back from an object. It's widely employed in robotics for precise obstacle detection and distance measurement tasks due to its reliability and straightforward interfacing capabilities with microcontrollers, we used 5 ultrasonic sensors , 3 in the front , one on the right side of the robot and one on the left side of the robot.
## *TCS3200 Sensor:
https://www.adafruit.com/product/1334

The TCS3200 is a high-precision RGB color sensor used for accurate color measurement. It utilizes a matrix of photodiodes and color filters to detect light across the visible spectrum. Applications include robotics, smart lighting systems, and medical devices.



## Behind the Scenes: Tackling Technical Hurdles in Our Robot Project:
Despite being an unforgettable experience, like any other journey, it was filled with obstacles. We cannot deny that the resilience ingrained in us by our Palestinian heritage helped us overcome these challenges. This competition was our first experience in building and programming a robot. None of the team members had ever participated in such an event before. This was our first hurdle: three of us venturing into the unknown. Many questions plagued us and we faced a lot of hardship during our quest for answers. How do we build and design a robot from scratch? What do we need? How do we make this robot overcome obstacles? What is the best way to make this robot recognize colors? Many questions needed answers, and the journey to find them was arduous. But as Palestinians, we do not know the meaning of surrender.
## The First Hurdle:
While trying to find a solution for the obstacle challenge round, we needed to program the robot to recognize red and green traffic signs. What should we do? We researched and read a lot about the OpenCV library and decided to use it to enable the robot to perform color detection. This was our first experience with image processing. However, we faced many difficulties when using OpenCV; the detection was not accurate. We tried multiple times to fix the issue but eventually decided to abandon OpenCV and use the Pixy2 camera, which is specifically designed for color recognition.
## From Concept to Creation: Innovating Our Robot with Artistry
The WRO rules allowed us to use a ready-made robot structure, but Team Kufiyatech refused the easy route. As we are Equipped with specialized training from the Purpose Academy in FreeCAD design platform, we decided to take the challenging path. We embarked on designing our robot from scratch and 3D-printing it. This journey required meticulous attention and focus; we had to redesign several times until we found the perfect design. This step consumed considerable time and effort from our team, with special thanks to Sara Jawaada, our team member responsible for the design. 
# Mechanism
Your vehicle’s drivetrain works with the engine to deliver power to the wheels. The most common types of drivetrains are front-wheel drive (FWD), rear-wheel drive (RWD), four-wheel drive (4WD) and all-wheel drive (AWD), Our car utilized a rear-wheel drive system.

# Raer-wheel drive(RWD):
![image](https://github.com/KufiyaTech/WRO2024/assets/172860664/97326854-3f39-4af9-92d1-6d75792b20d6)

It is a type of drivetrain system in vehicles where the engine's power is directed to the rear wheels. Rear-wheel drive vehicles have balanced weight distribution and higher control over the vehicle. The rear-wheel drive system consists of several main components: the drive shaft, the rear axle, and the differential gears, which in turn transmit the power to the axles and then to the wheels, Our car's mechanism was constructed using the LEGO EV3 kit.

https://www.amazon.com/Lego-Mindstorm-Ev3-Core-45544/dp/B00DEA55Z8?th=1
# Mastering Precision: Differential and Steering Dynamics:

# Ackermann steering geometry 

we used We used Ackerman steering , Ackermann steering geometry is a configuration designed to ensure that the wheels of a vehicle trace out circles with different radii during a turn, preventing tire slippage. It was invented by Georg Lankensperger and patented by Rudolph Ackermann. This geometry helps align the front wheels towards the turning center, providing improved handling and stability, especially at low speeds. It contrasts with other mechanisms like the Davis steering gear, offering simpler construction and fewer components susceptible to wear. Ackermann steering is commonly used in standard vehicles for its advantages in maneuverability and reduced tire wear​

# Differential Gearbox

We opted to use a differential gearbox for the rear wheels of the robot , A differential gearbox is a crucial component in vehicles, enabling wheels on the same axle to rotate at different speeds. This functionality is vital during cornering, as it allows the outer wheel to travel a greater distance than the inner wheel, enhancing traction and handling. The device operates through a set of gears that balance the torque distribution between the wheels, ensuring smooth and efficient power transmission. Differential gearboxes are essential in various vehicles, from cars to heavy machinery, optimizing performance and safety.



 ![image](https://github.com/KufiyaTech/WRO2024/assets/172860664/17ccce49-5632-41f0-b007-5583dd16745b) ![image](https://github.com/KufiyaTech/WRO2024/assets/172860664/87b4bee8-bcad-4ff9-bd33-1b79948e8d38)




# KufiyaTech's Engineering Masterpiece: The Design Story

# Introduction 

Building an RC for WRO Future Engineers from scratch has been a significant challenge, especially since it's our first time designing a robot. Although using a kit would have been an easier option, we insisted on building our own robot, leaving us with no other options. As we started gathering the necessary components, we focused on identifying the exact mechanisms required for our RC. Our goal was to solve the challenges presented in the two competition rounds as effectively and simply as possible. The design of our robot has evolved over time, and here is how our designs have developed through this journey:

# Steering System:

As we mentioned before, We chose the Ackerman Steering.

# First design:

Our initial steering system was effective in terms of functionality, but we faced challenges when it came to supporting and securing all the components on top of it.

# Second design:

Opting for this steering system proved to be a better choice initially, but the system was based on ready-to-print files sourced from the internet, which presented us with a dilemma: adhere to the predefined dimensions that we couldn't alter, or undertake the challenge of designing it entirely from scratch.

# third design:

Unlike our previous designs, this iteration didn't require 3D printing because we utilized the EV3 LEGO kit for the mechanism. This approach saved us time and effort, allowing us the flexibility to modify and control it easily. The LEGO kit provided a reliable steering solution that we could test quickly, contrasting with the longer process required by our previous designs.










## Open challenge:





## Obstacle avoidance:
