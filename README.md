# 🔧 LED Blink using Register-Level Programming (Arduino UNO)

This project demonstrates how to blink an LED connected to **pin 13 (PB5)** of the **ATmega328P** microcontroller using **direct register access**, instead of the Arduino functions.

---

## 🧩 Hardware Used
- Arduino UNO (ATmega328P)
- Onboard LED (Pin 13)

---

## ⚙️ Register Explanation
| Register | Purpose | Bit |
|-----------|----------|-----|
| DDRB | Data Direction Register | DDB5 = 1 → Output |
| PORTB | Output Register | PB5 = 1 → LED ON, PB5 = 0 → LED OFF |

---

## 🧠 Code Logic
1. Configure PB5 as output (`DDRB |= (1 << DDB5)`).
2. Toggle PB5 ON and OFF with a delay using `_delay_ms()`.

---

## 🧰 Build and Upload
1. Open **Atmel Studio / AVR-GCC / PlatformIO**.
2. Compile and flash the HEX file to Arduino UNO.
3. The onboard LED blinks at 10Hz (100ms ON, 100ms OFF).
