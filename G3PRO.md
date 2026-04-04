# 🎛️ Product Requirement Document (PRD)
## Product Name: Pro USB Audio Interface (WXL-Pro)

---

## 1. Overview

The WXL-Pro is a professional-grade USB audio interface designed to directly compete with products like Elgato Wave XLR Pro. It targets streamers, podcasters, musicians, and content creators who require high-quality microphone input, intuitive control, and seamless software integration.

The product combines:
- High-performance microphone preamp
- USB audio interface functionality
- Real-time digital control (gain, mute, monitoring)
- Integrated DSP routing and mixing

---

## 2. Objectives

- Deliver **studio-grade microphone input quality**
- Provide **simple, intuitive one-knob control**
- Enable **low-latency USB audio streaming**
- Integrate **software-based digital mixer and routing**
- Compete with Elgato Wave ecosystem in usability and UX

---

## 3. Target Users

- Streamers (Twitch / YouTube)
- Podcasters
- Content creators
- Home studio users
- Gamers with professional audio needs

---

## 4. Key Features

### 4.1 Microphone Input

- 1x XLR input (balanced)
- Supports:
  - Dynamic microphones
  - Condenser microphones (+48V phantom power)
- Input impedance: ≥ 3 kΩ

---

### 4.2 Preamp Design

- Gain range: 0 – 75 dB
- Ultra-low noise preamp:
  - EIN ≤ -128 dBu
- THD+N ≤ 0.002%
- Digitally controlled gain (no analog pot noise)
- Smooth gain stepping (0.5–1 dB steps)

---

### 4.3 USB Audio Interface

- USB Type-C
- USB Audio Class 2.0 compliant
- 24-bit / 48 kHz (base), optional 96 kHz
- 2-in / 2-out audio streaming
- Compatible with:
  - Windows
  - macOS
  - iOS / Android (OTG)

---

### 4.4 Control Interface

- Multi-function rotary encoder:
  - Gain control
  - Headphone volume
  - Monitor mix
- Capacitive touch mute button
- LED ring indicator:
  - Gain level
  - Clip indication
  - Mute status

---

### 4.5 Monitoring

- Zero-latency direct monitoring
- 1x headphone output (6.35mm)
- Output power: ≥ 100 mW @ 32Ω
- Mix control:
  - Mic vs PC playback

---

### 4.6 DSP & Software Mixer

- Digital mixer software (desktop app)
- Features:
  - Input/output routing
  - Virtual channels (music, game, chat, mic)
  - Volume control per channel
  - Mute / solo / monitoring
- Optional DSP:
  - Noise suppression
  - Compressor
  - EQ
  - Limiter

---

### 4.7 SD Card Recording (Optional Advanced Feature)

- Standalone recording without PC
- Supports SD / SDHC / SDXC
- File format: WAV (24-bit)
- Dual recording:
  - Raw mic
  - Processed signal

---

## 5. Hardware Architecture

### 5.1 Block Diagram

flowchart LR
    A[XLR Mic Input] --> B[Low-Noise Preamp]
    P[+48V Phantom Power] --> B
    B --> C[ADC]
    C --> D[MCU / DSP Engine]
    D --> E[USB Interface]
    E --> F[PC / Mobile Device]

    D --> G[Headphone DAC]
    G --> H[Headphone Output]

    D --> I[SD Card Recorder]
    I --> J[SD Card Storage]

    K[Rotary Encoder / Touch Control] --> D
    L[LED Ring Indicator] --> D

    M[Power (USB 5V)] --> N[Power Regulation]
    N --> B
    N --> C
    N --> D
    N --> G

---

### 5.2 Core Components

- Preamp Op-Amp: OPA1612 / AD797 class
- ADC/DAC: AKM / ESS high dynamic range
- MCU/DSP: ARM Cortex-M / DSP core
- USB Controller: UAC2 compliant
- Power: USB 5V with internal regulation

---

## 6. Software Requirements

### 6.1 Desktop App

- Platforms:
  - Windows
  - macOS

Features:
- Gain control UI
- LED ring sync
- DSP configuration
- Virtual routing mixer
- Firmware update

---

### 6.2 Firmware

- Real-time audio processing
- Gain control logic
- USB streaming
- SD recording engine (if enabled)
- Preset storage

---

## 7. Performance Metrics

| Metric              | Target Value        |
|-------------------|--------------------|
| Gain Range        | 75 dB              |
| EIN               | ≤ -128 dBu         |
| THD+N             | ≤ 0.002%           |
| Latency           | < 10 ms            |
| Dynamic Range     | ≥ 110 dB           |

---

## 8. User Experience (UX)

- One-knob control philosophy
- Clear LED feedback (color-coded)
- Plug-and-play operation
- Minimal setup required
- Seamless integration with streaming software

---

## 9. Competitive Positioning

| Feature              | WXL-Pro | Elgato Wave XLR |
|---------------------|--------|-----------------|
| Gain Range          | 75 dB  | ~70 dB          |
| DSP Effects         | Yes    | Limited         |
| SD Recording        | Optional | No            |
| Virtual Mixer       | Yes    | Yes            |
| UI/UX               | Premium | Premium        |

---

## 10. Risks & Challenges

- USB power stability with phantom power
- Heat dissipation in compact design
- DSP latency optimization
- Software stability (critical for UX)

---

## 11. Future Expansion

- Multi-channel version
- Bluetooth control
- Mobile app integration
- Cloud presets
- AI noise reduction

---

## 12. Timeline (Example)

| Phase          | Duration |
|---------------|----------|
| Concept       | 2 weeks  |
| Hardware Dev  | 8 weeks  |
| Firmware Dev  | 10 weeks |
| Software Dev  | 10 weeks |
| Testing       | 4 weeks  |
| Production    | 6 weeks  |

---

## 13. Success Criteria

- Stable USB audio performance
- Clean, low-noise microphone input
- Positive user feedback from creators
- Competitive differentiation vs Elgato ecosystem

---

