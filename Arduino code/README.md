# Arduino Firmware – Boost Converter (AstraVolt)

## Overview
This firmware controls an **asynchronous DC–DC Boost Converter** developed by the **AstraVolt Team**.  
It generates a **50 kHz PWM** signal to drive the MOSFET, measures output voltage and current, and displays the results on an LCD.

---

## Features
- 50 kHz PWM using **Timer1** (Pin D9)
- Duty cycle control via potentiometer
- Output voltage sensing (A1)
- Output current sensing using **INA219**
- 16×2 I²C LCD display
- Simple feedback-based voltage regulation
- Serial monitor output

---

## Hardware
- Arduino Nano  
- TLP250 isolated gate driver  
- INA219 current sensor  
- 16×2 I²C LCD (0x27)  
- Input voltage: 12.5 V  

---

## Pin Mapping
| Function | Arduino Pin |
|--------|-------------|
| PWM Output | D9 |
| Potentiometer | A0 |
| Voltage Sense | A1 |
| INA219 / LCD | I²C (A4, A5) |

---

## Control Logic
- Duty cycle is set by potentiometer  
- Theoretical Vout is calculated using boost equation  
- Measured voltage is compared to theoretical value  
- PWM duty is adjusted accordingly  

⚠️ Educational control method (not PID).

---

## Upload Instructions
1. Open `BoostConverter.ino` in Arduino IDE  
2. Select **Arduino Nano (ATmega328P)**  
3. Install required libraries:
   - Adafruit INA219  
   - TimerOne  
   - LiquidCrystal I2C  
4. Upload

---

## License
MIT License (Engineering Extension)  
Use at your own risk.
