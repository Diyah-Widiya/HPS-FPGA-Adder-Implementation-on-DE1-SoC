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

## 3. Repository Structure
📂 hps-fpga-adder-de1soc
│
├── 📁 fpga/
│   ├── adder.v                # Verilog adder module
│   ├── top_level.v            # Top-level module and memory mapping
│   ├── system.qsys            # Platform Designer file
│   └── pin_assignment.qsf     # Pin assignments for DE1-SoC
│
├── 📁 hps/
│   ├── adder_hps.c            # C code running on HPS
│   ├── Makefile               # Build script for HPS
│
├── 📁 docs/
│   ├── block_diagram.png      # System architecture illustration
│   ├── memory_map.md          # Register map documentation
│   └── workflow.png           # Design workflow
│
└── README.md                  # You are reading this file

