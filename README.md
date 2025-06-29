# 🔍 Sequence Detector (1011) using Verilog - Moore FSM

This project implements a **1011 sequence detector** using a **Moore finite state machine (FSM)** in Verilog. It detects a specific binary pattern (`1011`) in a serial input stream and outputs a high signal (`1`) whenever the sequence is recognized.

---

## 📌 Problem Statement

Design a Moore finite state machine in Verilog to detect the sequence `1011` from a serial binary input. The detector should output `1` when the sequence is found and `0` otherwise. The design must be tested using a Verilog testbench and verified through waveform simulation.

---

## 💡 Key Features

- ✅ Moore FSM: Output depends **only on the current state**
- ✅ Detects sequence: `1011`
- ✅ Supports overlapping detection
- ✅ Tested with a custom Verilog testbench
- ✅ Waveform verified

---

## 📂 Files Included

| File Name                                 | Description                                   |
|------------------------------------------|-----------------------------------------------|
| `Sequence_Detector_MOORE_Verilog.v`      | Verilog source code of the Moore FSM          |
| `tb_Sequence_Detector_Moore_FSM_Verilog.v` | Verilog testbench for simulating the FSM     |
| `README.md`                              | Project documentation                         |

---

## 🚦 FSM Design

### States

- `Zero` – Initial state
- `One` – Detected ‘1’
- `OneZero` – Detected ‘10’
- `OneZeroOne` – Detected ‘101’
- `OneZeroOneOne` – Detected `1011` → Output = 1

### Transition Flow
| State           | Input = 1         | Input = 0        |
|-----------------|-------------------|------------------|
| Zero            | One               | Zero             |
| One             | One               | OneZero          |
| OneZero         | OneZeroOne        | Zero             |
| OneZeroOne      | OneZeroOneOne     | OneZero          |
| OneZeroOneOne   | One               | OneZero          |              OneZero









---

## 🔬 Simulation Insights

- ✅ Output depends **only** on current state (Moore logic)
- ✅ Detects `1011` correctly
- ✅ Output returns low after detection unless sequence continues
- ✅ Handles overlapping sequences

---

## 🛠 Tools Used

- 🖥️ Language: **Verilog HDL**
- 🧪 Simulator: **Vivado / ModelSim / any Verilog simulator**
- 📁 Design: **RTL FSM Design**
- 🧰 Testbench: Included for verification

---

## 📚 Educational Purpose

This project is a basic yet powerful introduction to FSM design in Verilog. It demonstrates:
- State transitions
- Pattern detection
- Moore FSM logic separation
- Testbench-based simulation

---

## 👨‍💻 Author

**Arkaprava Paul**  
B.Tech in Electronics and Electrical Engineering  
Minor in Computer Science and Engineering  
Indian Institute of Technology, Guwahati  
📧 imapaul05@gmail.com | p.Arkaprava@iitg.ac.in  
🔗 [LinkedIn](www.linkedin.com/in/arkaprava-paul-73223a314) 
This project is created as a part of learning digital design using Verilog and FSMs.

---

## 📜 License

This project is for educational purposes. Feel free to use and modify it with attribution.
