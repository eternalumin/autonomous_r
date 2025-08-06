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
