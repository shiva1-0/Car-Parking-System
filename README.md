# Car-Parking-System
This project implements a Verilog-based Smart Car Parking System that automates the entry and exit process in a parking area using sensors and password authentication.
The system tracks the number of vehicles inside the parking lot, indicates availability using LEDs, and ensures secure entry through a password verification mechanism.

## Features
- Automatic entry detection using sensors
- Password-based vehicle authentication
- Dynamic vehicle counting (entry and exit)
- Real-time indication using Green and Red LEDs
- Display of parked and available spaces
- Simulation verified in Xilinx Vivado

## Flowchart
![flowchart](https://github.com/user-attachments/assets/bd7d5783-5b65-4677-b67b-569b71936887)

## Working Principle
The system follows a Finite State Machine (FSM) model as shown in the flowchart.
**1. Start**
The system initializes all registers, counters, and LED indicators.
**2. Input Cars**
The entry sensor detects the presence of a car at the parking entrance.
**3. Sensors_Entrance**
When a car approaches, the entry sensor triggers the system to check the password input.
**4. Password Confirmation**
The driver must enter the correct password.
- If Valid, the gate opens, and the car is allowed to enter.
- If Invalid, the red LED glows and the system denies entry.
**5. Valid Condition**
When the password is correct, the car is granted access, and the system increments the vehicle count (Count + 1) and decreases the available slot count.
**6. Sensor_Exit**
When a car exits, the exit sensor detects the movement and updates the counter.
**7. Count - 1**
The vehicle counter decrements, indicating a car has left the parking lot, and an available space is freed.
**8. End State**
The system loops back to the initial state, ready to detect the next vehicle.

##Tools & Technologies

- Hardware Description Language :	Verilog HDL
- Simulation Software :	Xilinx Vivado
