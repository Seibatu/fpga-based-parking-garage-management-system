# 🅿️ FPGA-Based Parking Garage Management System 🚗
### 🚦 Smart Parking Management using Verilog HDL

## 📌 Project Overview
This project implements a **parking garage management system** on an **FPGA** development board.
The system:
- ✅ Controls the **entry gate** based on parking availability.
- ✅ Directs drivers to **available parking spots**.
- ✅ Uses **7-segment displays** to show parking information (space available).
- ✅ Uses **weight sensors** to detect occupied spaces.

## 🚘 How It Works
1️⃣ The driver **pays** or has a **valid permit** to enter.  
2️⃣ The system **checks for available parking spots**.  
3️⃣ The **gate opens** only if a spot is available.  
4️⃣ The system **assigns a parking floor & spot**.  
5️⃣ The **7-segment display** shows the parking **floor & spot number**.  

⚠️ **If the parking is full, the gate remains closed!**  

## 🔧 Hardware Requirements
| Component        | Description                         |
|-----------------|-------------------------------------|
| **FPGA Board**  | Nexys4 FPGA that supports Verilog     |
| **7-Segment Display** | Shows floor & parking spot info |


## 📜 Features
### 🎯 Core Functionalities
- 🚗 **Gate Control** – Opens **only** when there’s an available parking spot.
- 🏢 **Smart Parking Assignment** – Ensures parking spots are **filled in order** to reduce congestion.
- 📟 **7-Segment Display Integration** – Displays **available floor and parking spot**.
- ⚖️ **Weight Sensor Input** – Detects **occupied** parking spaces.


## 📂 Project Structure
```
/parking-garage-fpga
│── src/              # Source files (Verilog)
│── sim/              # Simulation files
│── docs/             # Documentation
│── README.md         # Project documentation
```
## 🛠️ How to Run It
### 1️⃣ Simulation
To test the design before FPGA implementation:
1. Open **Vivado Simulator**.
2. Load `topModule.v` and include all submodules (`topModule.v`, `clkControl.v`, `fsmParkingLogic.v`, `sevenSegment.v`).
3. Compile and run the testbench (`testbench.v`).
4. Observe the waveform in the built-in waveform viewer.

### 2️⃣ FPGA Implementation (Nexys4 Board)
1. Open **Xilinx Vivado**.
2. Create a new project and add all Verilog files.
3. Assign FPGA board I/O pins according to your hardware setup using a Constraints XDC file.
4. Run Synthesis, implementation, and generate the bitstream.
5. Program your bitstream to the FPGA and test using the physical switches.


## 📜 Source Files (`src/`)
| File Name              | Description                                       |
|------------------------|---------------------------------------------------|
| `topModule.v`          | **Top-level module** integrating all components.  |
| `clkControl.v`        | **Clock control module** for timing synchronization. |
| `fsmParkingLogic.v`   | **Finite state machine** for parking management.  |
| `sevenSegment.v`      | **7-segment display driver** for parking space display. |
 
## 📸 Simulation Waveform

## ✉️ Contact
For any questions or improvements or collaborations, feel free to connect:
- **GitHub:** [Seibatu](https://github.com/Seibatu)
- **LinkedIn:** [Seiba Abdul Rahman](https://www.linkedin.com/in/seiba-abdul-rahman)
