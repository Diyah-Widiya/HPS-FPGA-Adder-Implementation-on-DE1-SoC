# HPS–FPGA Adder Implementation on DE1-SoC
## 1. Project Overview
This project demonstrates a hardware–software co-design system on the **DE1-SoC FPGA development board**, where:

- The **Adder module** is implemented in the FPGA fabric using **Verilog**.
- The **HPS (ARM Cortex-A9)** executes a C program to send two integers to the FPGA.
- The FPGA performs the addition and returns the result through a memory-mapped interface.

This project is intended as an introductory SoC design example for students learning embedded systems, digital logic, and FPGA–HPS integration.
---
## 2. Features

- ✔ FPGA-based 32-bit adder  
- ✔ HPS communicates with FPGA through the Lightweight AXI Bridge  
- ✔ Simple memory-mapped register interface  
- ✔ Fully verified on DE1-SoC board  
- ✔ Includes Verilog, C code, and Platform Designer system  

---
## 3. System Architecture

### Block Diagram

+-----------------+ AXI-Lite +----------------+
| | ---------------------> | |
| HPS | Write input A | FPGA |
| (Cortex-A9) | ---------------------> | Adder Logic |
| | <--------------------- | |
+-----------------+ Read SUM +----------------+
