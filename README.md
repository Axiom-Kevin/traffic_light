# 🚦 Arduino Traffic Light Controller

## 📌 Overview

This project simulates a basic traffic light system using an Arduino Uno and three LEDs (Red, Yellow, and Green). Each LED represents a traffic signal and lights up in sequence with realistic timing.

This project expands on previous Arduino projects by introducing multiple outputs and sequential programming, helping build a stronger understanding of digital electronics and embedded systems.

---

## 🎯 Objectives

* Learn to control multiple digital output pins.
* Understand sequential execution in Arduino programs.
* Practice using `delay()` for timing.
* Improve debugging skills for both hardware and software.
* Simulate a real-world embedded system.

---

## 🛠 Components

* Arduino Uno
* Breadboard
* 3 × LEDs

  * 🔴 Red
  * 🟡 Yellow
  * 🟢 Green
* 3 × 220Ω (or 330Ω) Resistors
* Jumper Wires
* USB Cable

---

## 🔌 Circuit Connections

| LED       | Arduino Pin |
| --------- | ----------- |
| 🔴 Red    | D8          |
| 🟡 Yellow | D9          |
| 🟢 Green  | D10         |

Each LED is connected in series with a resistor before connecting to GND.

---

## 🚦 Traffic Light Sequence

```text
🔴 Red      → 5 seconds
🟡 Yellow   → 2 seconds
🟢 Green    → 5 seconds
🟡 Yellow   → 2 seconds
Repeat...
```

---

## 💻 Arduino Code

```cpp
void setup() {
  pinMode(8, OUTPUT);
  pinMode(9, OUTPUT);
  pinMode(10, OUTPUT);
}

void loop() {

  // Red
  digitalWrite(8, HIGH);
  delay(5000);
  digitalWrite(8, LOW);

  // Yellow
  digitalWrite(9, HIGH);
  delay(2000);
  digitalWrite(9, LOW);

  // Green
  digitalWrite(10, HIGH);
  delay(5000);
  digitalWrite(10, LOW);

  // Yellow
  digitalWrite(9, HIGH);
  delay(2000);
  digitalWrite(9, LOW);
}
```

---

## 🧠 Concepts Learned

* Digital Outputs (`pinMode`, `digitalWrite`)
* Controlling Multiple LEDs
* Sequential Programming
* Timing with `delay()`
* Hardware Troubleshooting
* Reading Compiler Errors
* Basic Embedded System Design

---

## 📷 Project Preview

### Circuit

*(Insert your circuit image here)*

### Demo

*(Insert your project video or GIF here)*

---

## 🚀 Future Improvements

* Add a pedestrian crossing button.
* Replace `delay()` with `millis()` for non-blocking timing.
* Add a buzzer for pedestrian signals.
* Display countdown using a 7-segment display or LCD.
* Simulate a four-way traffic intersection.

---

## 📚 Skills Demonstrated

* Arduino Programming
* Breadboard Prototyping
* Circuit Assembly
* Embedded Systems Fundamentals
* Debugging Hardware and Software
* Technical Documentation
