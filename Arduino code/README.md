# 🔌 Boost Converter Firmware – AstraVolt

<p align="center">
  <img src="https://img.shields.io/badge/Arduino-Nano-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/PWM-50kHz-brightgreen?style=for-the-badge">
  <img src="https://img.shields.io/badge/INA219-Current%20Sensor-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge">
</p>

---

## ⚡ Overview
This firmware controls an **asynchronous DC–DC Boost Converter** developed by the  
**AstraVolt Team** 🛠️

It generates a **50 kHz PWM** signal to drive the MOSFET, measures **output voltage & current**, and displays real-time data on an **I²C LCD**.

---

## 🔧 Features
✅ 50 kHz PWM using **Timer1**  
✅ Duty cycle control via **potentiometer**  
✅ Voltage sensing using **analog divider**  
✅ Current sensing via **INA219**  
✅ Real-time **LCD + Serial Monitor** output  
⚠️ Simple educational feedback (non-PID)

---

## 🧠 Control Logic
🟢 Read potentiometer → set duty cycle  
🟢 Calculate theoretical boost voltage  
🟢 Measure actual voltage & current  
🟢 Adjust PWM duty accordingly  

📷 **[Insert control flow diagram here]**

---

## 🧩 Hardware Used
| ⚙️ Component | 📌 Description |
|-------------|---------------|
| 🔵 MCU | Arduino Nano |
| 🔌 Driver | TLP250 (Isolated) |
| 📏 Sensor | INA219 |
| 🖥️ Display | 16×2 I²C LCD (0x27) |
| ⚡ Vin | 12.5 V |

---

## 🔗 Pin Mapping
| 🔗 Function | 📍 Arduino Pin |
|------------|---------------|
| PWM Output | D9 |
| Potentiometer | A0 |
| Voltage Sense | A1 |
| INA219 + LCD | I²C (A4, A5) |

---

## ▶️ Upload Steps
1️⃣ Open `BoostConverter.ino` in **Arduino IDE**  
2️⃣ Select **Arduino Nano (ATmega328P)**  
3️⃣ Install required libraries:
- Adafruit INA219  
- TimerOne  
- LiquidCrystal I2C  
4️⃣ Upload 🚀

---

## ⚠️ Important Note
> ⚠️ This firmware is intended for **educational and experimental use only**.  
> Not designed for commercial or high-power applications.

---

## 👥 Team
💡 **AstraVolt Team**  
📅 2025

---

## 📜 License
🟡 MIT License (Engineering Extension)  
Use at your own risk ⚡
