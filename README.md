# GuitarPedal

A real-time, FPGA-based digital audio effects processor designed for guitar signals. This project combines an FPGA (Basys3 Artix-7) and a microcontroller (ESP32-C3) to implement a modular and customizable effects chain.

## 🎯 Features
- Real-time audio signal processing
- Modular audio effects (distortion, delay, EQ, noise gate)
- Hardware control via rotary encoders, OLED, and buttons
- Low-latency I2S communication between MCU and FPGA
- 32-bit ADC/DAC (PCM1802/PCM5102) for high-fidelity sound

## 🔧 Architecture Overview
- **Signal Path**:  
  `Guitar Input → Inverting Op-Amp Buffer → ADC → FPGA (Effects DSP) → DAC → Inverting Op-Amp → Amp`

- **Control Path**:  
  `blank`

## 📦 Hardware
- **FPGA**: Digilent Basys3 (Artix-7)
- **Microcontroller**: ESP32-C3 Rust Dev Board
- **ADC**: PCM1802
- **DAC**: PCM5102
- **Op-Amps**: TL072
- **UI**: KY-040 Rotary Encoders, OLED Display
- **Audio Connectors**: 1/4” Panel-Mount Mono Jacks
- **Power**: 9V barrel input, 5V/3.3V regulated rails

## 🛠️ Project Milestones
- [] blank

## 🎸 Effects Modules (Planned)
- **Distortion / Overdrive**: Hard clip, soft clip, wave shaping
- **Delay / Echo**: Circular buffer w/ tap tempo
- **EQ / Tone Control**: Adjustable low/mid/high bands
- **Noise Gate**: Dynamic threshold-based muting

## 📁 Repo Structure (planned)
