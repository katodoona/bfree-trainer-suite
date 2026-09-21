![preview](https://raw.githubusercontent.com/katodoona/bfree-trainer-suite/main/cover_aef1bf4.svg)
# 🚴 Bfree Companion — The Smart Trainer Co-Pilot for Discerning Cyclists

[![Download](https://raw.githubusercontent.com/katodoona/bfree-trainer-suite/main/latest_92461e.svg)](https://katodoona.github.io/bfree-trainer-suite/)

![Status](https://img.shields.io/badge/status-actively--maintained-brightgreen)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux%20%7C%20Android%20%7C%20iOS-blue)
![Language](https://img.shields.io/badge/i18n-14%20languages-orange)
![License](https://img.shields.io/badge/license-MIT-lightgrey)
![Uptime](https://img.shields.io/badge/support-24%2F7-success)
![Year](https://img.shields.io/badge/release-2026-purple)

---

## 🧭 Overview

**Bfree Companion** is a next-generation indoor cycling companion built for riders who treat their smart trainer like a trusted teammate rather than a gadget. Where the original `bfree` project laid the groundwork for pairing riders with their equipment, Bfree Companion expands the concept into a full hospitality suite for your watts — a place where cadence, resistance, heart rate, and gradient data all converse with each other in a language your legs immediately understand.

Think of it as the difference between a hotel lobby and a concierge desk. The old experience got you through the door. Bfree Companion remembers your room number, knows your preferred wake-up call, and quietly adjusts the lights before you arrive.

Whether you are chasing a structured threshold interval block at 5 a.m. or improvising a virtual hill climb on a rainy Sunday afternoon, Bfree Companion bends to your rhythm — not the other way around.

---

## 🎯 Why This Project Exists

Most trainer applications assume the rider should adapt to the software. We take the opposite view. Bfree Companion was constructed from the ground up around a simple principle: *the app should feel invisible once your wheels start spinning.* Every control surface, every notification, every menu was stress-tested against a single question — does this help the rider forget they are staring at a screen?

The result is a companion that feels less like a dashboard and more like a riding partner who happens to have an encyclopedic memory and infinite patience.

---

## ✨ Feature Highlights

### 🖥️ Responsive Interface That Bends to Any Screen
From a 6-inch phone mounted on aerobars to a 49-inch ultrawide in a pain cave, the layout reflows intelligently rather than simply shrinking. Panels dock, collapse, and reassemble themselves based on available real estate. Touch targets remain generous; typography scales without losing hierarchy.

### 🌍 Multilingual Support Across 14 Locales
Riders describe suffering in every language. Menus, tooltips, workout cues, and error dialogs are available in English, Spanish, French, German, Italian, Portuguese, Dutch, Polish, Japanese, Korean, Mandarin, Swedish, Danish, and Norwegian. Locale detection is automatic, and switching mid-session never interrupts an active workout.

### ☎️ Round-the-Clock Assistance, Every Day of the Year
A dedicated support rotation keeps response times short regardless of your timezone. Whether you are debugging an ANT+ dropout at midnight in Lisbon or configuring ERG smoothing at noon in Auckland, someone is on the other end who actually rides.

### 📡 Broad Protocol Compatibility
ANT+, ANT+ FE-C, Bluetooth Low Energy FTMS, and legacy proprietary bridges are all first-class citizens. The pairing wizard walks through each transport with plain-language diagnostics rather than cryptic numeric fault codes.

### 📈 Live Telemetry with Zero Perceptible Lag
Cadence, power, heart rate, and virtual elevation stream into the interface with sub-100 ms perceived latency. A dedicated rendering thread keeps the UI at high frame rates even on modest hardware.

### 🧩 Workout Builder and Library
Compose interval structures visually, drag segments to reorder, and export to portable formats. The bundled library ships with endurance, sweet spot, threshold, VO2, and sprint progressions suitable for riders from casual to competitive.

### 🏔️ Gradient Simulation & Resistance Profiles
Simulated climbs respond to weight, gearing assumptions, and rolling resistance coefficients you control. Want to feel like you are climbing the Stelvio with a heavier bike? Adjust the parameters and the resistance curve tightens accordingly.

### 🔄 Session Recovery & Auto-Save
Crash? Power cut? Browser tab closed by an enthusiastic pet? The session state persists every few seconds, and the resume flow restores position, resistance, and elapsed metrics without missing a beat.

### 🎨 Theme Engine
Light, dark, high-contrast, and an accessibility-focused "amber dusk" palette accommodate different lighting environments — from a sunlit garage to a blacked-out basement studio.

### 🔒 Privacy-First Architecture
Ride data stays on your device by default. Optional cloud sync is opt-in, encrypted, and fully revocable. No third-party advertising SDKs, no shadow telemetry, no surprises.

---

## 🧪 Use Cases

- **Structured Training Blocks** — Load a plan, hit start, and let the companion steer resistance while you focus on breathing.
- **Recovery Spins** — Light resistance, gentle cadence coaching, and a calm interface that discourages overdoing it.
- **Virtual Hill Repeats** — Simulate a gradient profile and practice pacing discipline without leaving the garage.
- **Group Sessions** — Multiple riders on the same network can share workout templates and compare telemetry side by side.
- **Coaching Handoffs** — Export session files in standard formats that coaches and analysts already know how to read.

---

## 🛠️ Architecture at a Glance

Bfree Companion is structured as a modular monolith with a pluggable transport layer. The core domain models — Rider, Session, Segment, TelemetryFrame — are transport-agnostic. Adapters for ANT+, BLE, and legacy bridges sit at the perimeter, translating external protocols into the same internal vocabulary. This separation means adding a new transport does not ripple through the workout engine, and refining the workout engine does not disturb device pairing.

Rendering uses a retained-mode scene graph rather than immediate-mode redraws, which keeps CPU usage predictable during long sessions. Persistence is handled by an embedded store with a write-ahead log, ensuring that session recovery survives even abrupt terminations.

---

## 🚀 Getting Started (Conceptual)

You do not need to compile anything to begin. The companion app is distributed as a ready-to-run bundle for each supported platform. Approach the process as you would approach a new bike fit: measure first, adjust second, ride third.

1. Install the bundle appropriate for your operating system.
2. Power on your smart trainer and confirm it is broadcasting.
3. Launch the companion and follow the pairing wizard.
4. Calibrate once, save the profile, and you are ready.
5. Optionally, import a workout plan or design one yourself.

Setup documentation lives in the `docs/` directory, organized by platform and by trainer family.

---

## 🧭 Roadmap for 2026

- Expanded workout analytics with fatigue modeling
- Native integrations with popular virtual riding ecosystems
- Additional locale coverage including Turkish and Brazilian Portuguese variants
- Offline-first sync conflict resolution improvements
- Accessibility audit and remediation across all interaction surfaces
- Public plugin API for third-party transport adapters

Priorities shift based on rider feedback. If a feature matters to you, say so — the issue tracker is read daily.

---

## 🧑‍🤝‍🧑 Contributing

Contributions are warmly welcomed, whether they take the form of code, documentation, translation, or a well-argued bug report. Before opening a pull request, please review the guidelines in `CONTRIBUTING.md` and ensure your changes align with the project's emphasis on responsiveness, privacy, and rider-first design.

Translation contributions are especially valued. If your language is not yet represented among the fourteen locales, the localization template in `i18n/` provides a clear starting point.

---

## 📜 License

This project is released under the MIT License. You are welcome to read, adapt, and build upon it in accordance with the terms described in the full license text:

[MIT License](https://opensource.org/licenses/MIT)

Copyright (c) 2026 Bfree Companion Contributors

---

## ⚠️ Disclaimer

Bfree Companion is an independent project and is not affiliated with, endorsed by, or sponsored by any smart trainer manufacturer or fitness platform. All product names, trademarks, and registered trademarks referenced remain the property of their respective owners.

The software is provided "as is," without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and non-infringement. In no event shall the authors or copyright holders be liable for any claim, damages, or other liability arising from, out of, or in connection with the software or the use or other dealings in the software.

Indoor training involves physical exertion. Consult a qualified medical professional before beginning any structured exercise program, and stop immediately if you experience pain, dizziness, or unusual shortness of breath.

---

## 🙏 Acknowledgements

Gratitude to every rider who filed a bug report at 6 a.m. before their own workout, to every translator who wrestled with the nuance of "cadence" in their language, and to the original `bfree` community whose curiosity made this successor possible.

Ride steady. Ride curious. Ride like the road is listening.

[![Download](https://raw.githubusercontent.com/katodoona/bfree-trainer-suite/main/latest_92461e.svg)](https://katodoona.github.io/bfree-trainer-suite/)