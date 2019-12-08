# Robo-Car

In this project, I will show you how to design and develop a Bluetooth Controlled Robot using Arduino, HC-05 Bluetooth Module and L298N Motor Driver Module. On the other end of the Bluetooth Communication, I will be using a Smart Phone and a simple Android App to control the Robotic Car.

Bluetooth Controlled Robot using Arduino Image 1

  

Table of Contents

    Introduction
    Prerequisites for Bluetooth Controller Robot
        HC-05 Bluetooth Module
        L298N Motor Driver Module
    Circuit Diagram of Bluetooth Controlled Robot
        Components Required
        Circuit Design
    Code
    Android App
    Working
    Limitations
    Applications

Introduction

Robots are always a fancy topic for students, hobbyists and DIYers. If you are beginner, then building a robot (like a car or an arm) is probably one of the important projects to do after learning about the basics.  

If you remember the earlier tutorial, I have discussed about HC-05 Bluetooth Module and how to interface one with Arduino. Also, I have provided a simple Bluetooth Controller App, which can be installed on your Android Phone and start transmitting the data.

  

As a continuation to that project, I will be implementing Bluetooth Controlled Robot using Arduino and a few other components and build a simple robotic car that can be controlled using an Android Phone (through an App) over Bluetooth Communication.
Prerequisites for Bluetooth Controller Robot

Apart from Arduino, which is the main controlling module of the project, there are two other important modules that you have to be familiar with in order to implement the Bluetooth Controlled Robot project.

They are the HC-05 Bluetooth Module and the L298N Motor Driver Module.
HC-05 Bluetooth Module

HC-05 Bluetooth Module

The HC-05 Bluetooth Module is responsible for enabling Bluetooth Communication between Arduino and Android Phone.

For more information on HC-05 Bluetooth Module, refer to HC-05 BLUETOOTH MODULE.
L298N Motor Driver Module

Arduino DC Motor Control using L298N Motor Driver Module

The L298N Motor Driver Module is responsible for providing the necessary drive current to the motors of the robotic car. I have provided information about L298N Module in an earlier project called Arduino DC Motor Control using L298N.

So, refer to ARDUINO DC MOTOR CONTROL USING L298N for more information on interfacing L298N with Arduino.

NOTE: I strongly recommend you to refer to the above mentioned two projects before proceeding further.
Circuit Diagram of Bluetooth Controlled Robot

The following is the circuit diagram of Bluetooth Controlled Robot using Arduino, L298N and HC-05.

Bluetooth Controlled Robot using Arduino Circuit Diagram
Components Required

    Arduino UNO  
    L298N Motor Driver Module 
    HC-05 Bluetooth Module  
    Robot Chassis  
    4 x 5V Geared Motors  
    Connecting Wires  
    Battery Holder
    Power Supply 
    Android Phone 
    Bluetooth Controller App 

NOTE: I have used L298N Motor Driver Module to drive the motors of the robot. You can use either this one or L293D Motor Driver Module. If you are using L293D, then check out for the connections.
Circuit Design

I wouldn’t go into the details of the construction of the robot as your robot chassis might be different from mine and you can easily figure it out how to build the robot from the available parts and possible cable management for making the robot more appealing.

Coming to the design of the circuit, first is the HC-05 Bluetooth Module. The +5V and GND pins of the Bluetooth Module are connected to +5V and GND of Arduino.

Since I will be only transmitting data related to the Robot’s movement from Android Phone to Bluetooth Module and do not intend to receive any data from Arduino, I will connect only the TX pin of the Bluetooth Module to RX Pin of Arduino.

This RX pin of Arduino is based on SoftwareSerial library (Pin 2 and Pin 3 are configured as RX and TX on Arduino). The RX pin of the Bluetooth is left open.

Bluetooth Controlled Robot using Arduino Circuit Design

Now, the L298N Motor Driver Module. Digital I/O Pins 9 through 12 of Arduino are configured as Input pins of the Motor Driver and are connected to IN1 through IN4 of the L298N Motor Driver Module. Both the Enable Pins are connected to 5V through provided jumper.

The robot chassis which I am using in this Bluetooth Controlled Robot Car project is supplied with 4 geared motors. Since L298N has slots for only two motors, I have joined the left side motors as one set and the right side motors as other set and connected both these sets to the output of L298N Module.
