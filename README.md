# Arduino Human-Following Car 

An autonomous mobile robot designed to track and follow a human target dynamically using ultrasonic and infrared proximity sensors.

##  Project Overview
This project uses an Arduino-compatible motor driver shield to control a 4-wheel drive (4WD) chassis. By processing distance and directional inputs from sensors mounted on the front, the car maintains a safe, consistent distance while trailing a moving target.

## 🛠️ Components Used
* **Microcontroller / Motor Driver:** Arduino Motor Driver Shield (L298N-based architecture)
* **Chassis:** 4WD Smart Robot Car Chassis with 4 DC Motors (`MOTOR1`, `MOTOR2`, `MOTOR3`, `MOTOR4`)
* **Distance Sensor:** HC-SR04 Ultrasonic Sensor
* **Tracking Sensors:** Dual Infrared (IR) Proximity Sensors (`RIGHT SENSOR`, `LEFT SENSOR`)
* **Steering / Sensor Mount:** Standard Servo Motor
* **Power Source:** 7.4V - 9V Battery Pack with a master toggle switch

##  Circuit Diagram
The physical wiring layout connecting the motors, sensors, servo, and power supply to the motor driver shield is illustrated below:

![Circuit Diagram](Circuit%20Diagram%20(1).jpg)

##  Working Principle
1. **Obstacle Detection:** The HC-SR04 ultrasonic sensor constantly pings the space ahead to measure the distance to the target.
2. **Directional Steering:** The left and right IR sensors help fine-tune alignment, ensuring the car steers correctly toward the center of the target.
3. **Motion Control:** The dual H-bridge motor driver regulates speed and direction across all four wheels via the microcontroller logic.

## 🚀 Getting Started
1. Assemble the 4WD chassis and secure the DC motors to the motor driver channels (`M1`, `M2`, `M3`, `M4`).
2. Wire the HC-SR04 ultrasonic module, IR sensors, and servo motor according to the circuit diagram above.
3. Upload your control script to the Arduino board and power the system using the 7.4V–9V battery supply.
