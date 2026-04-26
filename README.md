# Person Counter using LCD and Gate Sensors (Embedded C)

## 📌 Overview
This project implements a person counting system using an embedded microcontroller and a 16x2 LCD display. The system counts the number of people entering and exiting through two gates and displays the count on the LCD. LEDs and a buzzer provide indication for sensor activity and count updates.

---

## 🚀 Features
- Person counting based on two gate inputs
- Entry and exit detection using sequence logic
- Real-time display of count on LCD
- LED indication for each gate trigger
- Buzzer alert when count is updated
- Cooldown mechanism to prevent multiple triggers

---

## 🧰 Components Used
- Microcontroller (AVR-based)
- 16x2 LCD Display (4-bit mode)
- Two input sensors (connected as Gate 1 and Gate 2)
- LED (2)
- Buzzer
- Resistors
- Jumper wires

---

## ⚙️ Pin Configuration

### LCD (4-bit mode)
| Signal | Pin |
|--------|-----|
| RS     | PB0 |
| RW     | PB1 |
| EN     | PB2 |
| Data   | PD4–PD7 |

### Inputs
| Component | Pin |
|-----------|-----|
| Gate 1    | PB3 |
| Gate 2    | PB4 |

### Outputs
| Component | Pin |
|-----------|-----|
| LED1      | PD2 |
| LED2      | PB5 |
| Buzzer    | PD3 |

---

## 🔄 Working Principle

- The system continuously monitors two inputs: Gate 1 and Gate 2.
- When Gate 2 is triggered followed by Gate 1:
  - The person is considered to have entered
  - Count is incremented
- When Gate 1 is triggered followed by Gate 2:
  - The person is considered to have exited
  - Count is decremented (if greater than zero)

- The updated count is displayed on the second line of the LCD.
- LEDs blink when respective gates are triggered.
- A buzzer is activated whenever the count is updated.

---

## 🧠 Concepts Used
- Embedded C programming
- Direct register manipulation (PORT and PIN registers)
- LCD interfacing in 4-bit mode
- Digital input/output handling
- State-based logic for direction detection
- Basic timing and delay handling

---

## 🛠️ Software Used
- Embedded C
- AVR toolchain (e.g., AVR-GCC)

---

## 📷 Output
- LCD displays: "Persons entered:" on the first line
- Current count is displayed on the second line
- LED and buzzer indicate system activity

---

## 📌 Notes
- The system uses a cooldown delay to avoid multiple detections from a single trigger.
- Count will not go below zero.

---

## 👩‍💻 Author
Sneha
