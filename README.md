# 555 Timer IC Visualizer (v4)

A standalone, bare-metal hardware instrument built on the **ATmega328P** for real-time analysis of 555 timer circuits.

## Executive Summary

The 555 Timer IC Visualizer is designed to close the gap between electronics theory and practical debugging. It provides a compact, self-contained platform to observe waveforms, measure timing behavior, and troubleshoot voltages without relying on bulky external lab instruments.

## System Highlights

| Feature | Capability |
|---|---|
| Graphics Display | 1.3" SH1106 OLED (128×64) for live waveform plots, RC curves, and metric readouts |
| Logic Display | CD4511 BCD 7-segment output for instant pin-state visibility |
| Signal Range | 0.2 Hz to 12 kHz |
| Live Metrics | Frequency, duty cycle (%), and period (μs/ms/s auto-format) |
| Voltmeter Probe | Dedicated 0V to 10V DC measurement input |
| Power Inputs | 3.7V Li-ion + boost, USB Type-C, and 5V screw terminal |

## Real-Time Signal Analytics

- Oscilloscope-style waveform rendering with **Hold (Freeze)** and **Clear** controls.
- Adaptive visualization:
  - high-frequency multi-cycle synthesized waveform for stable viewing
  - low-frequency rolling sample track for slow-pulse inspection
- Continuous parameter tracking for frequency, duty cycle, and time period.

## Integrated Voltmeter

A front-facing probe header allows direct DC voltage measurement from **0V to 10V**, with live numeric feedback on the OLED for node-level troubleshooting.

## Operating Modes and Menu Architecture

Navigation is handled through a 5-button array: **UP, DOWN, SELECT, BACK, HOME**.

### 1) Astable Mode

- Theory section for free-running oscillator behavior
- Live waveform output with freeze/clear support
- RC charge/discharge graph across **1/3 VCC** and **2/3 VCC** thresholds
- On-screen equations for *tH, tL, T,* and *f*
- Breadboard DIY guide and practical applications (e.g., LED flasher, clock source)

### 2) Monostable Mode

- One-shot pulse generator explanation
- Trigger-based waveform capture and rolling history
- RC charging slope visualization linked to potentiometer tuning
- Timing equation: **T = 1.1 × R × C**
- Breadboard DIY guide and use cases (timer delays, switch debouncing)

### 3) Bistable Mode

- Two-state latch behavior explanation
- Direct SET/RESET logic-state observation
- Breadboard guide without RC timing components
- Applications in toggles, control latches, and simple memory behavior

## Design Advantages

- **Bare-metal responsiveness:** synchronized graphics, ADC sampling, and timer interrupts with minimal overhead
- **Lab autonomy:** combines waveform viewing, frequency analysis, and voltage probing in one unit
- **Interactive learning:** converts abstract timing behavior into measurable, visual feedback

## Current Status

The prototype hardware, triple-input power frontend, and firmware optimization are complete and validated.

**Next milestone:** migration from bench prototype to a compact, professional **2-layer PCB**.
