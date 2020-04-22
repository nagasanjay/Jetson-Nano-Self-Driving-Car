# Jetson-Nano-Self-Driving-Car
This is a project which uses deep Convolutional Neural Networks to steer a self driving car. It is powered by Jetson Nano and Arduino UNO.


<p align="center">
  <img width="300" height="275" src="https://user-images.githubusercontent.com/34810513/79965877-38c59100-84aa-11ea-9d23-f7f33091443c.jpeg">
</p>


Neural networks are universal function approximators which can be used for different kinds of problems(Classification, Regression, Segmentation, etc). In this self driving car prototype, I have used regression(I have tried classification too but regression is the way to go) to predict the steering angle of a car by using the video feed of the path as input to the neural network. Use this GitHub Repo to help build your own Self Driving Car. You can also alter the code slightly to use a car with Ackerman Steering and Servo Motors instead of using the classic Line Follower styled Chassis that I have used. With that being said, lets get started.


## The Self Driving Car Concept

This self driving car is a robot with four wheels powered by Arduino UNO, a Motor driver, a LIPO battery, 4 motors and wheels. The intelligent operations are carried out by NVIDIA's Jetson Nano board, which is a single board computer with GPU cores and CUDA support. The Jetson board processes the images obtained in real time from a web camera and feeds them into a Neural network with convolutional and fully connected layers. The neural network performs regression to predict the steering angle of the car and the angle is used to control the speed of the wheels of the robot, which makes it turn left, right or forward.

To understand this, consider a computer game where a user can drive a car by pressing the arrow keys. In order for an AI to drive the car, it should be able to predict the key to be pressed and the duration for which the key should be pressed based on the steering angle. To do this, it obtains a screen shot of the game for every fraction of a second and passes it through a neural network. The neural network predicts the steering angle at that instant and the AI presses the appropriate key. This keeps the car at the center of the road as shown below.

<p align="center">
  <img width="325" height="200" src="https://user-images.githubusercontent.com/34810513/79974333-c3ac8880-84b6-11ea-8b67-1ee88e75583c.jpeg">
</p>

Instead of making the AI drive the car in a computer game, we use real world data obtained from a robotic car prototype. The AI processes the real world feed and keeps the prototype at the center of the lane.

## Components And Connections

 We used the following components to build our prototype:
 
 1) Eagle high discharge LIPO Battery (11.1V, 35C) - 1 pc.
 2) IC-7805 regulators - 4pcs.
 3) L298N motor driver module - 1 pc.
 4) 300 RPM Motors - 4 pcs.
 5) Arduino UNO - 1 pc.
 6) NVIDIA Jetson Nano board - 1 pc.
 7) I-Ball Web Camera - 1 pc.
 8) Metal Chassis - 1 pc.
 9) Wheels - 4 pcs.
 10) Wires and Jumper Cables - as per required.
 11) Metal spacers - 4 pcs
 12) Perf Board - 1
 
 #### Custom regulator circuit
 
 
