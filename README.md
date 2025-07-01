# Ultra-Low Power Analog Temperature Alert System 🔥🔋

This project is a fully analog temperature alert system designed for two-wheeler vehicles, powered by a 3V, 1Ah coin cell. It uses no microcontrollers or comparators and achieves ultra-low power consumption — as low as **15.7 µA** in idle state — extending battery life up to several months. The system gives distinct audible alerts at three temperature thresholds (60°C, 70°C, 80°C) using a single TLC555 timer and includes a battery health LED indicator.

## Features

- 🚫 **No microcontroller or comparator used**
- 🔊 **Three temperature thresholds** (60°C, 70°C, 80°C) triggering a buzzer at distinct frequencies
- 🔋 **3V coin cell-powered (1Ah)**
- 🌡️ **One thermistor** used with transistor logic for multi-level sensing
- 💡 **Green LED battery indicator** that turns off below 2.5V
- ⏱️ **Ultra-low power consumption** (~9.73 µA idle current)
- 🚲 **Designed for 2-wheeler engine thermal monitoring**

## Schematic

![image](https://github.com/user-attachments/assets/24cd2761-3a5d-4df8-985f-534caf1a5223)


## How It Works

- A single thermistor and voltage divider generate a varying voltage as temperature changes.
- Three transistors are biased to turn on at different base voltages corresponding to different temperature thresholds.
- Each transistor selectively connects a resistor (R1) to the TLC555 timer’s timing network, changing the frequency of the PWM output.
- The buzzer is driven via a transistor from the TLC555 output.
- A green LED indicates healthy battery voltage (>2.5V); it turns off when voltage drops.

## Components Used

- TLC555CD (Low-power CMOS Timer)
- NPN Transistors (e.g., BC547/BC548)
- Thermistor (NTC 100k or simulated via potentiometer)
- 3V coin cell (CR2032 or similar)
- Buzzer (3V, low-power)
- Resistors, Capacitors, LED
- 1MΩ potentiometer (for tuning sensing thresholds)

## Applications

- 🔧 Two-wheeler engine temperature monitoring
- 🧪 Industrial analog temperature alert systems
- 🌡️ Smart appliances with safety overheating alerts
- ⚡ Battery-operated low-power embedded analog systems

## Power Consumption

| Mode             | Current (Approx.) |
|------------------|-------------------|
| Idle             | 9.73 µA           |
| Active (Buzzer)  | < 1 mA            |

## Author

Chirag Vinayak  
Electronics & Computer Engineer  
GitHub: chirag-23-23  
LinkedIn: https://www.linkedin.com/in/chirag-vinayak-b3b576317/

