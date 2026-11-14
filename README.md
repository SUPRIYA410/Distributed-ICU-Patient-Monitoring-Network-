# Distributed ICU Patient Monitoring Network

## 📌 Project Overview

The **Distributed ICU Patient Monitoring Network** is an embedded systems-based project designed to monitor multiple patient parameters using sensors and communicate the collected data to a centralized server through the Controller Area Network (CAN) protocol.

The system uses two nodes (Node A and Node B) for sensor data acquisition and communication. Node A collects patient parameters using sensors and transmits the acquired data to Node B through the CAN interface. Node B communicates with the computer (server) through the UART interface, where the patient's monitoring information is displayed.

This system helps healthcare professionals monitor important patient parameters from a centralized location.

## 🎯 Objectives

- Monitor multiple patient parameters in real time.
- Acquire sensor data using ADC channels.
- Establish communication between distributed nodes using the CAN protocol.
- Transfer patient monitoring data to a centralized computer.
- Display the collected sensor values on the server.

## 🔧 Hardware Components

    Component             :        Purpose 
 Microcontroller          - Controls sensor data acquisition and communication. 
 Temperature Sensor       - Measures the patient's body temperature. 
 SpO2 Sensor              - Monitors blood oxygen saturation level. 
 LDR Sensor               - Measures light intensity in the patient's environment. 
 CAN Transmitter/Receiver - Enables communication between Node A and Node B. 
 UART Interface           - Transfers data from Node B to the computer. 
 Computer (Server)        - Receives and displays patient monitoring information. 

## 📡 Communication Protocols

### 1. CAN (Controller Area Network)

- Used for communication between Node A and Node B.
- Supports reliable communication between distributed embedded nodes.
- Allows sensor data to be transmitted between nodes using CAN message frames.
- Reduces the need for separate communication connections between nodes.

### 2. UART (Universal Asynchronous Receiver Transmitter)

- Used for communication between Node B and the computer.
- Transfers the received patient data to the server.
- Enables monitoring of sensor values through a serial communication interface.

## ⚙️ Working Principle

1. The temperature, LDR, and SpO2 sensors are connected to Node A.
2. Sensor outputs are acquired through the microcontroller's ADC channels.
3. Node A processes the acquired sensor values.
4. The processed data is transmitted to Node B through the CAN interface.
5. Node B receives the CAN messages and forwards the patient data to the computer using UART communication.
6. The computer acts as a centralized server and displays the patient monitoring parameters.

## 📊 Parameters Monitored

The system monitors the following parameters:

| Parameter | Sensor | Sample Display Value |
|---|---|---|
| Temperature | Temperature Sensor | 28°C |
| Light Intensity | LDR Sensor | 60% |
| Oxygen Level | SpO2 Sensor | 99% |

*Note: The above values are sample readings shown in the project block diagram.*

## 🏗️ System Architecture

The project consists of two main nodes:

**Node A – Sensor Acquisition Node**
- Interfaces with temperature, LDR, and SpO2 sensors.
- Acquires sensor data through ADC channels.
- Transmits the collected data through the CAN interface.

**Node B – Receiver and Server Interface Node**
- Receives sensor data from Node A through CAN communication.
- Transfers the received information to the computer through UART.
- Acts as an interface between the CAN network and the centralized server.

## 🛠️ Technologies Used

- Embedded C
- ARM Microcontroller Programming
- ADC Interfacing
- CAN Protocol
- UART Communication
- Sensor Interfacing
- Embedded Systems

## 🌟 Key Features

- Distributed sensor monitoring architecture.
- Multi-sensor data acquisition.
- CAN-based communication between embedded nodes.
- UART-based communication with the centralized server.
- Centralized display of patient monitoring parameters.
- Modular architecture that can be extended with additional monitoring nodes.

## 🚀 Applications

- ICU patient monitoring systems.
- Hospital patient monitoring networks.
- Remote healthcare monitoring.
- Embedded medical monitoring systems.

## 🔮 Future Enhancements

- Add more patient monitoring nodes.
- Integrate heart rate and additional vital-sign sensors.
- Develop a graphical user interface for real-time monitoring.
- Implement wireless communication for remote patient monitoring.
- Add alert notifications when monitored parameters cross configured thresholds.

## 👨‍💻 Project Type

**Major Project | Embedded Systems | ARM | CAN Communication | Sensor Interfacing**
