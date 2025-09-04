# Vending-Machine-using-verilog

## 📌 Overview
This project implements a **coin-based vending machine** using **Verilog HDL**.  
The machine is designed to:
- Accept ₹1, ₹2, and ₹5 coins.  
- Dispense a product when the total amount reaches **₹5 or more**.  
- Return change if the user inserts more than the required amount.  
- Reset for the next transaction after dispensing.  

The design is modeled using a **Finite State Machine (FSM)** and verified through **Verilog testbenches**.

---

## ✨ Features
- Accepts multiple coin denominations (₹1, ₹2, ₹5).  
- Dispenses product when balance ≥ required cost.  
- Returns change automatically.  
- Implemented using **FSM (Mealy model)**.  
- Fully simulated with **testbench and waveform results**.  

---

## 🛠️ Design Approach
The vending machine is modeled as a **Mealy FSM**, where:
- Each **state** represents the accumulated amount of coins.  
- **Transitions** occur when coins are inserted.  
- Output signals (`product`, `change`) are based on current state and input.  

### State Transitions:
- From `S0`:  
  - ₹1 → `S1`  
  - ₹2 → `S2`  
- From `S2`: ₹2 → `S4`  
- From `S3`: ₹2 → `S5` (dispense product)  
- At `S5`: Product is dispensed and FSM resets to `S0`.  

---

## 📊 Simulation
- The design was tested using **Xilinx ISE** and simulated with custom testbenches.  
- Results confirm:  
  - Correct state transitions.  
  - Proper dispensing when balance ≥ ₹5.  
  - Accurate change return.  

---

## 💡 Applications
- **Snack/Beverage Vending Machines**.  
- **Automated Ticketing Systems**.  
- **Digital transaction systems with FSM logic**.  
- Teaching aid for **FSM and Verilog-based design**.  

---

## 🚀 Future Enhancements
- Add support for **more products with different prices**.  
- Implement **cancel transaction and refund** logic.  
- Expand to accept **digital payments or cards**.  
- Deploy design on an **FPGA board** for real-time demonstration.  

---

## 👩‍💻 Author
**Pavan C K**  
Department of Electronics and Telecommunication  
Dr. Ambedkar Institute of Technology, Bengaluru, India  

---


