# 🚀 555 Timer IC Visualizer (v4)

A standalone, bare-metal hardware instrument built on the **ATmega328P** to make 555 timer behavior visible, measurable, and easy to understand in real time—without bulky lab gear.

---

## 📌 Executive Summary

The **555 Timer IC Visualizer** bridges electronics theory and practical debugging by combining live waveform rendering, timing analytics, logic-state display, and DC voltage probing in one compact platform.

---

## 💎 Premium Frontend & Interface

### 📺 Dual-Display System
- **1.3" SH1106 OLED (128×64):** Real-time waveform plots, capacitor charge/discharge curves, and dynamic metrics.
- **CD4511 BCD 7-Segment Display:** Instant ambient hardware feedback for logic levels and pin states.

### 🎛️ Real-Time Signal Analytics & Graph Engine
- **Frequency Range:** **0.2 Hz to 12 kHz**
- **Oscilloscope-style controls:**
  - **Hold (Freeze):** Capture pulse events for close inspection.
  - **Clear:** Reset history buffer while frozen.
- **Adaptive graph behavior:**
  - High frequency → stabilized multi-cycle synthesized waveform.
  - Low frequency → live rolling sample track.
- **Live computed metrics:**
  - Frequency
  - Duty cycle (rounded integer %)
  - Time period (auto-formatted in μs / ms / s)

### ⚡ Integrated DC Voltmeter Probe
- Dedicated front-facing probe header for **0V to 10V DC** measurement.
- Live OLED voltage readout for fast node/power rail troubleshooting.

---

## 🔌 Triple-Input Power Architecture

1. **3.7V Li-ion battery** + onboard boost to stable **5V logic rail** + dedicated charging module
2. **USB Type-C input** for modern adapters, laptops, and power banks
3. **DC 5V screw terminal** for benchtop laboratory power supplies

---

## 🛠️ Deep Menu Architecture (5-Button Navigation)

Buttons: **UP / DOWN / SELECT / BACK / HOME**

### 🔄 Astable Mode
- Theory and oscillator behavior overview
- Live waveform + frequency tracking + freeze/clear controls
- RC timing graph with real-time potentiometer slope response across **1/3 VCC** and **2/3 VCC** thresholds
- Timing equations: *tH, tL, T, f*
- Step-by-step DIY breadboard guide
- Applications: LED flashers, clock generators

### ⏱️ Monostable Mode
- One-shot pulse generator theory
- Triggered waveform capture + rolling history + hold/clear
- RC charge slope visualization during pulse generation
- Equation: **T = 1.1 × R × C**
- DIY breadboard blueprint
- Applications: timer delays, switch debouncing

### 🔒 Bistable Mode
- Two-state latch/flip-flop behavior explanation
- Direct SET/RESET logic tracking
- Wiring guide with independent SET and RESET buttons (no RC timing network)
- Applications: toggles, digital latches, memory cells

---

## 🎯 Key Design Advantages

- **Zero-lag bare-metal performance** for synchronized graphics, ADC voltmeter sampling, and interrupt-driven timing.
- **Complete lab autonomy** by consolidating key bench functions into one platform.
- **Interactive learning workflow** that converts invisible circuit behavior into real-time visual metrics.

---

## ⏩ Current Status

✅ Prototyping, triple-power integration, and firmware optimization are complete and validated.

### Next Step
➡️ Transitioning from wire-formed prototype to a compact, professional **2-layer PCB**.

---

## 🌟 Why It Matters

The 555 Timer IC Visualizer transforms the classic 555 timer from a black box into a fully observable system—ideal for learners, hobbyists, and engineers who want fast, practical insight into timing circuits.
