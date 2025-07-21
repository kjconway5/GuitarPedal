# GuitarPedal

A real-time, FPGA-based digital audio effects processor designed for guitar signals. This personal project combines an FPGA (Basys3 Artix-7) and a microcontroller (ESP32-C3) to implement a modular and customizable audio effects chain. The FPGA is used to modify the signal and create desired audio effects while the MCU is used to handle all of the user interface.

## 📦 Hardware
- **FPGA**: Digilent Basys3 (Artix-7)
- **Microcontroller**: ESP32-C3 Rust Dev Board
- **ADC**: PCM1802
- **DAC**: PCM5102
- **Op-Amps**: TL072

## 🎯 Features
- Real-time audio signal processing
- Modular audio effects (distortion, delay, EQ, noise gate)
- Hardware control via rotary encoders, OLED, and buttons
- Low-latency I2S communication between MCU and FPGA
- 32-bit ADC/DAC (PCM1802/PCM5102) for high-fidelity sound

## 🔧 Hardware Architecture
- **Signal Path**:  
  `Guitar Input → Inverting Op-Amp Buffer → ADC → FPGA (Effects DSP) → DAC → Inverting Op-Amp → Amp`

- **Control Path**:  
  `blank`

## 🛠️ Project Goals
- [] Multiple effects available (distortion, EQ, delay, and a noise gate to start)
- [] Ability to stack multiple effects at a time
- [] Ability to control how intensly the effect changes the original signal
- [] 

## 🎸 Signal Effects Modules (Planned)
- **Distortion / Overdrive**: Hard clip, soft clip, wave shaping
- **Delay / Echo**: Circular buffer w/ tap tempo
- **EQ / Tone Control**: Adjustable low/mid/high bands
- **Noise Gate**: Dynamic threshold-based muting

## 📁 Repo Structure (planned)

```
GuitarPedal/
├── README.md                  # Project overview, setup instructions
├── docs/                      # Design docs, diagrams, notes
│   ├── blank
│   ├── blank
│   └── blank
├── hardware/                  # Hardware-specific files (KiCad, part lists)
│   ├── blank
│   └── blank
├── mcu/                       # ESP32-C3 microcontroller firmware (C/C++)
│   ├── src/
│   │   └── blank
│   └── README.md
├── fpga/                      # FPGA logic (SystemsVerilog, constraints, Vivado project)
│   ├── src/
│   │   ├── blank
│   │   ├── blank
│   │   ├── effects/
│   │   │   ├── distortion.sv
│   │   │   ├── delay.sv
│   │   │   └── eq.sv
│   └── constraints/
│       └── basys3.xdc
├── tests/                     # Simulation testbenches or fuzzing
│   ├── fpga/
│   │   └── blank
│   ├── mcu/
│   │   └── blank
└── tools/                     # Utility scripts, e.g. flashing tools or log parsers
    └── flash_fpga.sh
```
