# IARELS# IARELS — Executive Voice Intelligence

<div align="center">

![License](https://img.shields.io/badge/License-MIT-emerald?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python)
![FastAPI](https://img.shields.io/badge/FastAPI-0.115%2B-teal?style=for-the-badge&logo=fastapi)
![Build](https://img.shields.io/badge/Build-Passing-brightgreen?style=for-the-badge)
![Presented By](https://img.shields.io/badge/Presented%20By-Abhi%20%26%20Phanendra-gold?style=for-the-badge)

### **Next-Generation Hands-Free Voice AI with Live Real-Time Web Intelligence & Voice Speed Telemetry**

*Presented by **Abhi and Phanendra***

[Overview](#-overview) •
[Key Features](#-key-features) •
[Voice Speed Telemetry](#-voice-speed-telemetry-wpm) •
[Architecture](#-architecture) •
[Quickstart](#-quickstart) •
[API Reference](#-api-reference) •
[GitHub Deployment](#-github-deployment)

</div>

---

## 🌟 Overview

**IARELS** is an executive voice intelligence platform engineered by **Abhi and Phanendra**. Inspired by Google Assistant but elevated with a bespoke design, IARELS combines hands-free continuous wake-word activation, real-time speech velocity measurement (Words Per Minute — WPM), live web and AI knowledge synthesis, strictly non-repeating vocal playback, and an aesthetic glassmorphic single-rectangle briefing layout.

The interface is styled in a signature color palette:
- **Celestial Aurora Olive** (`#14361e`, `#2d6a4f`, `#52b788`)
- **Midnight Obsidian Navy** (`#030712`, `#071326`, `#0b1e36`)

---

## ✨ Key Features

- **🎙️ Continuous Hands-Free Wake Words ("HEY", "TELL", "ABOUT")**:
  - Automatically triggers without clicking the microphone icon.
  - Uttering phrases like *"Hey tell me about black holes"*, *"Tell about quantum computing"*, or *"About Mars"* immediately activates question capture.
- **🗣️ Dynamic Voice Speed Detection (Words Per Minute — WPM)**:
  - Measures the user's speaking velocity using high-resolution millisecond timestamps (`performance.now()`) and word count.
  - Automatically classifies cadence into:
    - **`Calm / Deliberate`** (< 110 WPM)
    - **`Natural Cadence`** (110 - 165 WPM)
    - **`Fast / Dynamic`** (> 165 WPM)
  - Renders a real-time badge (`🗣️ 145 WPM (Natural Cadence)`) and stores metrics in session history.
- **🔉 Strictly One-Time Spoken Answers (Zero Repetition)**:
  - Web Speech synthesis is queued with single-execution locks and `.cancel()` enforcement to prevent duplicate readouts or audio looping.
- **🌐 Real-Time Live Web & AI Browser Knowledge Retrieval**:
  - Direct integration with open web knowledge APIs and encyclopedic summaries for verified, real-world factual data.
  - In-memory high-speed caching engine delivering sub-millisecond repeated queries (`0.0 ms` latency).
- **📦 Single Unified Rectangle Container with Exactly 3 Sub-Boxes**:
  1. **Question Section**: User's transcribed inquiry, user avatar, and timestamp.
  2. **Spoken Reply Header**: Conversational spoken readout with **`🔊 Replay Voice`**, **`📋 Copy All`**, **`⚡ Latency Pill`**, and **`🗣️ Voice Speed Badge`**.
  3. **BOX 1: `📝 TEXT — FACTUAL OVERVIEW`**: Comprehensive encyclopedic briefing, category, and voice cadence record.
  4. **BOX 2: `📌 SUMMARIZATION`**: Synthesized summary accompanied by **`🏷️ Key Words Represented`** (glowing hashtag pills e.g. `#Astronomy`, `#NASA`).
  5. **BOX 3: `💡 KEY TAKEAWAYS`**: Bulleted factual highlights extracted from verified intelligence.
- **📜 Top-Right History Console**:
  - Clickable drawer in the upper right corner displaying previous inquiries, recorded timestamps, voice speed telemetry, and instant recall capabilities.
- **Presented by Abhi and Phanendra**:
  - Elegantly credited in the persistent footer.

---

## 🗣️ Voice Speed Telemetry (WPM)

IARELS calculates speech rate client-side and transmits telemetry to the backend:

$$\text{WPM} = \text{round}\left(\frac{\text{Word Count}}{\Delta t_{\text{seconds}}} \times 60\right)$$
