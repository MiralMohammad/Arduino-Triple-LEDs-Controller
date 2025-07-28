# 💡 Triple LED Controller with Arduino Uno

This project demonstrates how to control **three LEDs** using an **Arduino Uno**.  
It was built and tested using **Tinkercad Circuits**, simulating a real-life Arduino setup.

![Circuit Diagram](./LedButtonConroller33.png)

---

## 🎯 Project Description

The circuit lights up 3 different LEDs (red, blue, yellow/orange) one after another in a timed loop using `digitalWrite()` and `delay()` functions.

Each LED is connected to a **digital pin** and turns on/off in a pattern that alternates every second.

---

## 🧰 Components Used

- 1 × Arduino Uno R3  
- 3 × LEDs (red, blue, yellow)  
- 3 × 220Ω resistors  
- Breadboard  
- Jumper wires  
- Tinkercad Circuits for simulation

---

## 🖥️ Code Overview

```cpp
//
void setup()
{
  pinMode(7, OUTPUT);
  pinMode(8, OUTPUT);
  pinMode(12, OUTPUT);

}

void loop()
{
  digitalWrite(7, HIGH);
  digitalWrite(8, LOW);
  digitalWrite(12, HIGH);

  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(7, LOW);
  digitalWrite(8, HIGH);
  digitalWrite(12, LOW);
  delay(1000); // Wait for 1000 millisecond(s)
}
