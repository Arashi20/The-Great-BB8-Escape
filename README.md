# The Great BB8 Escape

Tamar Mans (u799512), Arash Mirshahi (u719136), Noa Mollee (u202196) & Tessa Ooms (u873248)

## Introduction
For our project, we will improve the performance of the pit-escape task of Robot Benchmark. In this simulation, our BB-8 agent has to autonomously escape a pit, as quickly as possible. To achieve this, we utilized and tweaked the different sensors and actuators on the agent to determine when to turn the motor on and off to improve its performance.

We used the body accelerometer in our BB8 agent to determine when it reaches its highest point in the pit of the corresponding movement and starts to fall back in the pit. At this point, we will let the pitch motor accelerate in the other direction. This way, our robot keeps as much of its momentum as possible, and can, finally, escape the pit.

In the end, our agent successfully escaped the pit in about 22 seconds, with a performance of 81.28%

## Components of Autonomous Behavior

Our simulated agent consists of two main parts: a spherical body and an hemispherical head.

Our simulated agent uses three different types of motor: a body pitch motor, body yaw motor and a head yaw motor. The body pitch motor can rotate the spherical body of the agent vertically, while the body yaw motor can rotate it horizontally. The head yaw allows the head to move around horizontally. To complete the pit-escape task, we only utilized the agent’s body pitch motor.

As for sensors, our agent measures both the acceleration and angular velocity. To measure the acceleration, the agent uses a body accelerometer, and head accelerometer, which measure the acceleration of the body and head respectively. The counterweight inside the body of the robot ensures it stays balanced and upright, and also helps keep the wheels inside BB8 against the lower half of its body (Sánchez, n.d.). This counterweight is the center of mass of the robot, and its acceleration and angular velocity gives us insight into the balance of the robot. To measure the acceleration of the counterweight, a counterweight accelerometer is also included in the robot. 

To detect the angular velocity, our agent uses a body gyro, counterweight gyro and head gyro. The body gyro measures the rate of rotation of the body, while the head gyro measures that of the head. Similar to the counterweight accelerometer, the robot also contains a counterweight gyro. The counterweight gyro measures the angular velocity of the center of mass, which can give us insight into how fast the bottom of the robot is rotating.

All of the accelerometers and gyros on the agent measure three dimensions: the x-axis, the y-axis and the z-axis.

Our agent has two types of controllers. The main controller ensures that the agent can move back and forward, given a time interval. The other controller is meant to keep the robot balanced (Sánchez, nd).

The simulated environment is a pit, in which our agent is placed. The pit starts steep, and slowly gets less steep. Our agent has to get out of this pit as quickly as possible. The task is finished when the agent either escapes the pit, or takes more than one minute to escape. Performance is either based on the speed in which the robot was able to escape the pit, or how close it was to escaping.

## Video of the agent completing the task (clicking the link will redirect you to the video recording of the pit escape in OneDrive)

https://1drv.ms/v/s!AivNv6z-gRHAgccVEIDetlhVlpWPog?e=S8BLka

## Source code

The source code of our agent can be found in this repository under the name "Source_code_BB8.ipynb".


## Experience with an actual and simulated agent
Working with the Arduino kit for creating the autonomous agent was a fun experience and a great introduction to hardware. Not only did we learn to work with basic components of an autonomous agent, we also had to put our creative minds to work. Overall, we really enjoyed this project, even though it was challenging.

The simulation project is a nice opportunity to get some experience with an autonomous and simulated agent, in a way that we have not yet seen in other courses. This way we got to see how our programming skills learned during our study can be used in real-life applications.

We sadly had some difficulties with the simulation project. We felt our lack of a physics course made it quite hard to find a logical, physics-based solution for the problem.
Despite this lack of knowledge, we still tried our hardest to reason our way out of it (rather than just using trial and error). We tried to do this using real-world knowledge of the movement of objects, and to allow our program to set automatic threshold values.
Unfortunately, we are not completely certain our reasoning is completely sound according to physics. Perhaps it might be nice to give a little more help on how to approach these kinds of problems during the practical sessions in the future of this course.





## Author contributions

Introduction: Noa

Components description: Noa and Tamar

Video recording: Tamar

Source code: Tessa and Arash

Experience description: Everyone


## Resources

Sánchez, C. (n.d.). How Does BB-8 Work? How Does BB-8 Work? Retrieved 18 May 2023, from http://www.howbb8works.com

Webots documentation: Sphero’s BB-8. (n.d.). Retrieved 18 May 2023, from https://cyberbotics.com/doc/guide/bb8




        


