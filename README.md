# Hi, we are KufiyaTech team , representing our beloved country , Palestine!
![image](https://github.com/KufiyaTech/WRO2024/assets/172860664/dadcaba7-8023-4e38-a5b0-0115967261ec)  ![image](https://github.com/KufiyaTech/WRO2024/assets/172860664/f204697d-a67c-4bb1-8258-b94a9ba9a639)





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

# Overview 
Our rear-wheel-drive car used three ultrasonic sensors to avoid obstacles and the internal and external walls of the track. In addition, we applied a PID controller. We used a Pixy2 camera to detect red and green traffic signs. A color sensor was used to verify the color of the lines on the map, and based on the color, the robot determined its direction: if the sensor detected a blue line, the robot moved counterclockwise, and if the sensor detected an orange line, the robot moved clockwise. We used an IMU to obtain the coordinates of the car's location, a servo motor to steer the car in the steering system, and a DC motor connected to a motor driver to control the car's forward and backward movement, providing propulsion. A 12V battery with a voltage regulator was used to distribute the necessary voltage to all components.

## Materials : 
| Quantity | Status                             | Description                                                                                                                                             |
| ---------| ---------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1        | Raspberry Pi 4 Model B             |https://www.raspberrypi.com/products/raspberry-pi-4-model-b/                   |
| 1        | *Arduino Uno:          | https://store.arduino.cc/products/arduino-uno-rev3              |
| 1        | The L298N Motor Driver:                     | https://components101.com/modules/l293n-motor-driver-module                         |
| 1       | Servo motor MG995          | https://components101.com/motors/mg90s-metal-gear-servo-motor |
| 1 | pixy2 camera| https://pixycam.com/pixy2/   |
| 1      | MPU-9250       |https://learn.sparkfun.com/tutorials/mpu-9250-hookup-guide/all         |
| 3        | *HC-SR04 Ultrasonic Sensor  | https://www.sparkfun.com/products/15569 |
|1      | TCS3200 Sensor        | https://www.adafruit.com/product/1334   |




## Behind the Scenes: Tackling Technical Hurdles in Our Robot Project:

## The Hurdles:
1- While trying to find a solution for the obstacle challenge round, we needed to program the robot to recognize red and green traffic signs. What should we do? We researched and read a lot about the OpenCV library and decided to use it to enable the robot to perform color detection. This was our first experience with image processing. However, we faced many difficulties when using OpenCV; the detection was not accurate. We tried multiple times to fix the issue but eventually decided to abandon OpenCV and use the Pixy2 camera, which is specifically designed for color recognition.

2- Since the mechanism was made of LEGO, we faced issues regarding the sturdiness of the steering and the initial turning angle. When the car hit something, the wheels would fall off. Therefore, we decided to modify the mechanism and used a LEGO kit to make it more robust.

3- Due to the numerous components that needed to be connected to the Arduino, wiring them in a way that prevents interference and arranging and securing them to avoid disconnections was a challenge.
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
 ![image](https://github.com/KufiyaTech/WRO2024/assets/172860664/17ccce49-5632-41f0-b007-5583dd16745b) ![image]

# Differential Gearbox

We opted to use a differential gearbox for the rear wheels of the robot , A differential gearbox is a crucial component in vehicles, enabling wheels on the same axle to rotate at different speeds. This functionality is vital during cornering, as it allows the outer wheel to travel a greater distance than the inner wheel, enhancing traction and handling. The device operates through a set of gears that balance the torque distribution between the wheels, ensuring smooth and efficient power transmission. Differential gearboxes are essential in various vehicles, from cars to heavy machinery, optimizing performance and safety.

![image](https://github.com/KufiyaTech/WRO2024/assets/172860664/0ee09c0b-852b-486b-8228-b37931adc5ea)







# KufiyaTech's Engineering Masterpiece: The Chassis Design Story

The design of our robot has evolved over time, and here is how our designs have developed through this journey:


# Steering System:

As we mentioned before, We chose the Ackerman Steering.
# First design:

Our initial steering system was effective in terms of functionality, but we faced challenges when it came to supporting and securing all the components on top of it

![image](https://github.com/KufiyaTech/WRO2024/assets/172860664/b4ffc615-b223-4875-a704-f96b63dd2298)

# Second design:

Opting for this steering system proved to be a better choice initially, but the system was based on ready-to-print files sourced from the internet, which presented us with a dilemma: adhere to the predefined dimensions that we couldn't alter, or undertake the challenge of designing it entirely from scratch.
https://cults3d.com/en/3d-model/gadget/3d-printed-rc-car-with-brushless-motor-lee3d999

# third design:

Unlike our previous designs, this iteration didn't require 3D printing because we utilized the EV3 LEGO kit for the mechanism. This approach saved us time and effort, allowing us the flexibility to modify and control it easily. The LEGO kit provided a reliable steering solution that we could test quickly, contrasting with the longer process required by our previous designs.
                                                                                                                                  


# First design:

Our initial choice was similar to the second option in terms of using ready-to-print files for the steering system. However, we encountered familiar challenges, compounded by an additional difficulty: the inability to locate suitable shafts or bearings within our allotted timeframe.

https://cults3d.com/en/3d-model/gadget/3d-printed-rc-car-with-brushless-motor-lee3d999


# Second design:
In this instance, we opted to utilize the EV3 LEGO system to design and construct our steering mechanism, marking a departure from our previous approaches. This choice offered the same advantages as our third steering system design, particularly in terms of ease of management and reliability

# Chassis:

First design:
Our initial design phase was the most time-consuming. Being our first attempt, we grappled with defining the shape of our robot and determining how it would accommodate all intended components, including five ultrasonic sensors. This constrained our design options significantly. Our primary objective was to create a chassis capable of housing all components, prioritizing functionality over minimizing size. We positioned the camera at the rear without adhering to standard engineering principles. Initially, our plan was to utilize a 3D printer for manufacturing.


# Second design:

Our second design was the first one we brought to life by printing it using a 3D printer. This design incorporated our chosen mechanism, but upon completion, we discovered it was too compact to meet our established standards

# | first design| Second design| 
| ![image](https://github.com/KufiyaTech/WRO2024/assets/172860664/880ac769-6f3d-44d7-a4ef-9e1b801f6266)  |     
| ![image](https://github.com/KufiyaTech/WRO2024/assets/172860664/1bd015c1-421a-4a30-905c-2772ba682bd6)   | 


# third design:

Before proceeding with the computer-aided design, we opted to sketch our third design on paper. We then crafted a prototype using compressed cork to evaluate its dimensions. Our aim was to slightly increase its size while accommodating our chosen mechanisms. However, due to limitations with our printer, we were compelled to design two separate bases (chassis) and join them together. During testing, we discovered a potential vulnerability: the structure could potentially break apart under specific weight conditions.

                                                                                                                                           |
| ---------| ---------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![image](https://github.com/KufiyaTech/WRO2024/assets/172860664/a5f15b99-cfae-4cd8-bba8-e09ab30f1281)     | ![image](https://github.com/KufiyaTech/WRO2024/assets/172860664/e78e858e-036b-499c-a5f9-99556fc64504)                   | ![image](https://github.com/KufiyaTech/WRO2024/assets/172860664/c8822e1b-69e6-4e3f-ad21-80fed76dd14e)
| ![image](https://github.com/KufiyaTech/WRO2024/assets/172860664/3407ff2e-6af5-4a1a-9452-e8134866ccaf)       | 


 # fourth design:
 
We decided to shift from using a 3D printer to a CNC machine for bringing our designs to reality. This allowed us to create a single, connected chassis capable of supporting more weight. Our design continued to evolve due to changes in our mechanism and component choices. A significant change was opting for smaller LEGO wheels to improve steering, which took some time to perfect. Another challenge we faced was managing space constraints relative to the size of our mechanisms. However, with the guidance and support of our great coach, we were able to find better solutions and overcome these obstacles.
After deciding to use a CNC machine, we encountered several challenges in selecting the ideal material to meet our needs. Initially, we chose acrylic, but it proved too brittle and broke easily. We then searched for a more suitable material and ultimately selected wood, which met our goals and requirements perfectly.

![image](https://github.com/KufiyaTech/WRO2024/assets/172860664/8d3b3f33-9369-4ae3-a089-77990af68bc5)

![image](https://github.com/KufiyaTech/WRO2024/assets/172860664/27b721c8-c8ca-469b-8199-d90283b693bb)

 













## Open challenge:





## Obstacle avoidance:
<table>
