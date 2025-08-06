# Autonomous Robot – Modular Embedded System (TM4C123, Keil µVision5)

Bare-metal firmware for ARM Cortex-M4F TM4C123 microcontroller, developed and validated using Keil µVision5 debug environment.  
The project demonstrates modular embedded design for autonomous robot control, including motor control logic, sensor input handling, and interrupt-driven decision-making.

---

## 📌 Features
- **Interrupt Service Routines (ISR)** for obstacle detection, configured through NVIC.  
- **Control loop timing** managed via hardware timer configuration and SysTick.  
- **Bit manipulation & CMSIS register access** for GPIO setup and memory-mapped I/O.  
- **Keil Debug Mode validation** of firmware logic and register writes. *(No physical TM4C123 hardware used for hardware validation)*

---

## 🛠 Development Environment
- **IDE**: Keil µVision5  
- **Target MCU**: TM4C123GH6PM (ARM Cortex-M4F)  
- **Programming Language**: Bare-Metal Embedded C, ARM Assembly (startup)  
- **Libraries**: CMSIS  

---

## ⚙ Project Structure
/autonomous_r ├── /src         # C source files ├── /inc         # Header files ├── startup.s    # ARM startup assembly ├── project.uvprojx # Keil project file └── README.md

---

## 🚀 How to Open & Run in Keil
1. **Clone the repository**
   ```bash
   git clone https://github.com/eternalumin/autonomous_r.git

2. Open the .uvprojx file in Keil µVision5


3. Select Debug → Start/Stop Debug Session


4. Use step/run controls to trace code execution


5. Check core peripherals (NVIC, SysTick) in the Debug windows



(Note: GPIO/timer outputs will not reflect live hardware behavior; this validation focuses on control logic and interrupt flow.)


---

🧠 How It Works

ASCII Block Diagram

+-------------+       +-----------------+       +-------------------+       +----------------+
|   Sensors   | ----> |   NVIC & ISR    | ----> | Decision-Making   | ----> |  Motor Control |
| (Inputs)    |       | (Interrupts)    |       | Logic             |       | (Outputs)      |
+-------------+       +-----------------+       +-------------------+       +----------------+


---

📄 Notes

Developed without physical TM4C123 hardware.

Firmware is designed to run on actual TM4C123 boards without modification.

Debug validation was performed by monitoring register writes and stepping through code execution in Keil.
