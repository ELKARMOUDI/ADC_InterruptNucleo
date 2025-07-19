# STM32F411 Nucleo ADC with Interrupts

![STM32F411](https://img.shields.io/badge/STM32F411-Nucleo-blue)
![ADC](https://img.shields.io/badge/ADC1-Interrupt_Mode-green)

<img src="https://github.com/user-attachments/assets/3c40f655-2922-431f-8795-05a0d89c3244" width="400" alt="EA36A5BE-2271-4E74-9D01-951FB1B2243B">

Read potentiometer values using ADC1 with conversion complete interrupts.

## Features
- **Interrupt-Driven** ADC conversions
- **PA0 Analog Input** for potentiometer
- **High Accuracy**: 480-cycle sample time
- **64MHz System Clock** (HSI-based PLL)
- **Non-blocking** operation

## Hardware Setup
| Component | Connection | Nucleo Pin |
|-----------|------------|------------|
| Potentiometer | VCC → 3.3V | - |
| | GND → GND | - |
| | WIPER → PA0 | CN7 pin 10 |

## Technical Details
### ADC Configuration 
```c
Clock: 32MHz (64MHz PCLK2 / 2)
Channel: ADC1_IN0 (PA0)
Sampling Time: 480 ADC cycles
Mode: Single conversion with interrupt
