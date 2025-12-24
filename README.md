# 🔌 Boost Converter Project – AstraVolt

## 📌 Project Overview
This project presents the **design and implementation of an irreversible (asynchronous) DC–DC Boost Converter** as an **educational and practical power electronics system**.

The converter steps up a low DC input voltage to a higher regulated output voltage using:
- An inductor for energy storage  
- A MOSFET for high-frequency switching  
- A fast recovery diode  
- An output capacitor to reduce voltage ripple  

An **isolated gate driver (TLP250)** is used to safely interface the low-voltage control circuit (Arduino) with the high-power switching stage, improving electrical safety, noise immunity, and reliability.

---

## 🎯 Educational Objectives
This project helps learners understand:
- Inductor charging and discharging behavior  
- The effect of duty cycle on output voltage  
- Continuous Conduction Mode (CCM) operation  
- Practical component selection and real-world losses  
- The importance of isolated gate drivers  
- Voltage regulation using feedback control  

---

## ⚙️ System Architecture
The system consists of the following main blocks:
- Power Stage (Boost Converter)
- Isolated Gate Driver (TLP250)
- Control Unit (Arduino Nano)
- Measurement Circuit (INA219 + Voltage Divider)
- User Interface (LCD + Potentiometer)

![System Block Diagram](images/Schematic.png)

---

## 🧩 Main Components

### 🔋 Power Stage Components
| Component | Description |
|---------|-------------|
| Inductor | 40 mH |
| MOSFET | IRFP260 / FQPF20N60 |
| Diode | BY399 Fast Recovery |
| Output Capacitor | 22 µF / 350 V |
| Heat Sink | TO-247 / TO-220F |

### 🧠 Control & Measurement
| Component | Function |
|---------|----------|
| Arduino Nano | PWM generation & control |
| TLP250 | Isolated MOSFET gate driver |
| INA219 | Current measurement |
| LCD 16×2 | Voltage & current display |
| Potentiometer | Duty cycle adjustment |

---

## 🔄 Boost Converter Operating Principle

### 🔹 Mode 1: Switch ON – Energy Storage
- MOSFET is ON  
- Inductor stores energy  
- Diode is reverse-biased  
- Load is supplied by the output capacitor  

📷 **[Insert energy storage mode diagram]**

---

### 🔹 Mode 2: Switch OFF – Energy Transfer
- MOSFET is OFF  
- Inductor releases stored energy  
- Diode conducts  
- Output voltage becomes higher than input voltage  

📷 **[Insert energy transfer mode diagram]**

---

## 📐 Design Specifications
- **Input Voltage:** 12 V  
- **Output Voltage:** ≈ 34 V  
- **Switching Frequency:** 50 kHz  
- **Operating Mode:** CCM  
- **Control Method:** PWM with feedback  

---

## 📊 Design Summary
| Parameter | Value |
|---------|-------|
| Duty Cycle (Real) | 0.68 |
| Inductor | 40 mH |
| Peak Inductor Current | ≈ 3.55 A |
| Output Capacitor | 22 µF |
| Diode | BY399 |
| MOSFET | IRFP260 / FQPF20N60 |

---

## 🧮 Control & Firmware
The Arduino firmware performs the following tasks:
- Generates PWM at 50 kHz  
- Reads potentiometer to set duty cycle  
- Calculates theoretical output voltage  
- Measures actual voltage and current  
- Applies feedback control for voltage regulation  
- Displays data on LCD and Serial Monitor  

📷 **[Insert firmware flowchart here]**

---

## 🧪 Simulation
The design was verified using:
- **LTspice**
- **MATLAB Simulink**

📷 **[Insert LTspice simulation results]**  
📷 **[Insert MATLAB Simulink model]**

---

## 🧱 PCB Design
The PCB was designed using **EasyEDA** and includes:
- A dedicated PCB for the gate driver
- A main PCB for the boost converter
- Proper power routing and isolation
- 3D PCB visualization

📷 **[Insert schematic images]**  
📷 **[Insert PCB top & bottom layers]**  
📷 **[Insert 3D PCB view]**

---

## 🧪 Testing & Results
- Tested at multiple duty cycle values
- Stable output voltage observed
- Real-time voltage and current monitoring
- Significant improvement after adding feedback control

📷 **[Insert hardware testing images]**

---

## ⚠️ Challenges & Solutions

### MOSFET Availability Issue
- Some MOSFETs showed poor thermal and efficiency performance  
- **Solution:** Switched to FQPF20N60 (isolated package)

### Inductor Charging Issue
- High ripple and poor efficiency observed  
- **Solution:** Optimized inductance value and switching frequency

### Load Dependency Issue
- Output voltage varied with load changes  
- **Solution:** Implemented feedback control loop

---

## 🚀 Conclusion
This project demonstrates a **complete Boost Converter system**, covering:
**design → simulation → firmware → PCB → hardware testing**.

It provides a strong foundation for advanced power electronics designs such as:
- Synchronous boost converters  
- Isolated DC–DC converters  
- Advanced SMPS applications  

---

## 📜 License
This project is released under the  
**MIT License (Engineering Extension)**.  
Use at your own risk.

---

