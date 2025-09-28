# 🖥️ 8-Bit Microprocessor (Verilog)

A simple educational **8-bit microprocessor** built in **Verilog HDL**, featuring a modular architecture with dedicated ALU, Program Counter, Register File, and a top-level CPU core. This project demonstrates the fundamentals of datapath design, instruction sequencing, and basic verification through testbenches.

---

## 📂 Project Structure
```
8-bit-microprocessor-master/
│
├─ ALU/                    # Arithmetic & Logic Unit
│  ├─ design.v             # ALU implementation
│  └─ test.v               # ALU testbench
│
├─ Program_Counter/
│  └─ design.v             # 8-bit Program Counter module
│
├─ REGISTER_FILE/
│  └─ design.v             # 8-bit Register File module
│
├─ processor.v             # Top-level CPU integrates all modules
├─ test.v                  # CPU-level testbench
├─ pro / allfiles.txt      # Supporting/utility files
└─ README.md               # Documentation
```

---

## ⚙️ Features
- **8-bit datapath** with accumulator and general-purpose register file
- **ALU** supporting arithmetic (add, sub) and basic logic (AND/OR/XOR) operations
- **Program Counter** with increment & reset logic for instruction sequencing
- **Top-level CPU** integrates ALU, Program Counter, and Register File
- **Testbenches** for module-level (ALU) and system-level verification
- **Hierarchical design** to demonstrate modular CPU construction
- Suitable for **simulation** in Icarus Verilog / ModelSim / Xcelium

---

## ▶️ Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/EMBEDDED-JUICE/8-bit-microprocessor-master.git
cd 8-bit-microprocessor-master
```

### 2. Simulate (Example with Icarus Verilog)
```bash
# Compile and run top-level CPU
iverilog -g2012 -o cpu_sim processor.v ALU/design.v REGISTER_FILE/design.v Program_Counter/design.v test.v
vvp cpu_sim
```

> Use `gtkwave dump.vcd` if your testbench generates waveform dumps.

---

## 🧪 Testbenches
- **ALU/test.v** – unit-level test for ALU functionality  
- **test.v** – top-level CPU testbench to validate instruction execution and data flow  

---

## 📝 Future Work
- Extend ALU with shift/rotate and compare instructions  
- Add branching/jump logic and a minimal instruction memory  
- Create a simple assembler and demo programs  

---

## 🙌 Acknowledgments
Inspired by educational CPU design labs and open-source HDL projects.
