# Arduino LED Light - 3 Light Test

This simple Arduino project demonstrates how to control three LEDs connected to an Arduino Uno. The LEDs blink **in sequence**, creating a basic "chase" light effect.

## 🔧 What It Does

- Turns on three LEDs one after the other.
- Each LED lights up briefly, then turns off.
- The sequence repeats in a loop.

## 🛠️ Hardware Requirements

- Arduino Uno
- 3 LEDs
- 3 Resistors (220Ω recommended)
- Breadboard and jumper wires
- USB cable to connect Arduino to PC

## ⚡ Circuit Diagram

| LED | Arduino Pin | Notes                |
|-----|-------------|----------------------|
| 1   | 13          | Anode to pin 13, cathode to GND via resistor |
| 2   | 12          | Anode to pin 12, cathode to GND via resistor |
| 3   | 11          | Anode to pin 11, cathode to GND via resistor |

## 💻 Arduino Code

```cpp
void setup() {
  pinMode(13, OUTPUT);
  pinMode(12, OUTPUT);
  pinMode(11, OUTPUT);
}

void loop() {
  digitalWrite(13, HIGH);
  delay(300);
  digitalWrite(13, LOW);

  digitalWrite(12, HIGH);
  delay(300);
  digitalWrite(12, LOW);

  digitalWrite(11, HIGH);
  delay(300);
  digitalWrite(11, LOW);
}
