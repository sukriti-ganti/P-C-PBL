# Embedded Control System for Smart Mining Helmet
## Project Overview
This project focuses on designing an embedded control system for a Smart Mining Helmet using the **8051 Microcontroller**, with an expansion vision toward **ARM Cortex-M (STM32)** platforms.  
The helmet integrates multiple safety sensors, processes their readings in real-time, and triggers alerts when hazardous conditions are detected. This serves as both a practical implementation of microcontroller-based systems and a platform for transitioning to advanced processors.

## Problem Statement
Mining environments pose serious risks due to toxic gases, physical impacts, and harsh working conditions. A safety system that can monitor environmental parameters and miner movement, while triggering timely alerts, is essential to prevent accidents.  
This project aims to develop such a system using affordable microcontroller hardware, scalable to higher-performance ARM platforms for industrial deployment.

## Objectives
1. Interface and control **MQ2 gas sensor**, vibration sensor, and optional temperature sensor using the 8051 MCU.
2. Implement **real-time alerts** via buzzer/LED when sensor thresholds are exceeded.
3. Transmit sensor data to a PC via **UART serial communication**.
4. Demonstrate **interrupt-based** event handling for fall detection.
5. Simulate and verify the design using **MCU8051 IDE/KEIL** and **Proteus**.
6. Plan migration to **STM32/ARM Cortex-M4** for scalability and IoT features.

## System Architecture
### Signal Flow:
* Sensors (Gas, Motion, Temperature) → MCU (8051) → Alert System (LED/Buzzer)  
* Data Transmission via UART → PC for monitoring/logging  
* Optional: Expansion to STM32 for advanced processing & connectivity

## Block Diagram
*(Insert schematic or block diagram here — e.g., Sensors → MCU → Alerts & UART → PC)* 

## List of Materials
| Component           | Quantity | Role                                   |
| ------------------- | -------- | -------------------------------------- |
| 8051 MCU Board      | 1        | Core control and processing unit       |
| MQ2 Gas Sensor      | 1        | Detects harmful gases                  |
| Vibration Sensor    | 1        | Detects miner fall or impacts          |
| Temperature Sensor  | 1        | Monitors ambient temperature           |
| ADC0808             | 1        | Analog-to-digital conversion           |
| LED + Buzzer        | 1 each   | Visual and audible alerts              |
| Resistors, Wires    | -        | Circuit connections                    |
| Power Supply (5V)   | 1        | Powers MCU and peripherals             |

## Tools & Technologies
* **MCU8051 IDE / KEIL** – Programming and simulation
* **Proteus** – Circuit design & simulation
* **UART Terminal (RealTerm, PuTTY)** – Data monitoring
* **ADC0808** – External analog data acquisition

## Working Principle
The helmet’s sensors feed data into the 8051 MCU. If readings exceed defined safety thresholds:
* GPIO triggers LED/buzzer alerts in real time.
* Data is transmitted to a PC over UART for monitoring.
* External interrupts handle sudden events like miner falls.
Simulation in Proteus validates the design before hardware deployment.

## Simulation & Testing
* Simulated in **Proteus** with realistic component models.
* ALP/C code tested in **MCU8051 IDE**.
* Verified UART data logging on PC.
* Threshold testing performed for gas and vibration sensors.

## Results
* System successfully detects hazardous gas levels and miner falls.
* Real-time alerts (LED/buzzer) operate reliably.
* Serial data logging allows remote monitoring.

## Challenges & Learnings
* Handling analog sensor inputs via external ADC.
* Managing multiple sensor inputs while maintaining fast response time.
* Learning interrupt handling for safety-critical systems.

## Future Scope
* Integration with **GSM Module** for SMS alerts.
* BLE/LoRa connectivity for IoT deployment.
* Full migration to **STM32/ARM Cortex-M** for advanced features.

## References
* 8051 Microcontroller Datasheet
* ADC0808 Datasheet
* STM32 Cortex-M4 Reference Manual
* UART Communication Protocol Documentation
