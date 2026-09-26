# IARELS - Executive Voice Intelligence

An aesthetic voice assistant presented by **Abhi and Phanendra**. Features hands-free wake word activation (**"HEY"**, **"TELL"**, **"ABOUT"**), strictly one-time spoken answers, real-time live data retrieval from web and AI browsers, and a structured 3-box briefing with keyword representation.

Styled with a signature palette: **Celestial Aurora Olive (`#14361e`, `#2d6a4f`)** and **Midnight Obsidian Navy (`#030712`, `#071326`)** with luminous glassmorphism.

---

## ✨ Features

- **🗣️ Real-Time Voice Speed Detection (Words Per Minute - WPM)**:
  - Dynamically calculates the user's speech delivery speed in real-time Words Per Minute (WPM) using speech timing telemetry (`performance.now()`) and word count.
  - Intelligently classifies speech cadence:
    - `Calm / Deliberate (< 110 WPM)`
    - `Natural Cadence (110 - 165 WPM)`
    - `Fast / Dynamic (> 165 WPM)`
  - Transmits voice speed metrics to the backend and renders an aesthetic glowing badge: `🗣️ 140 WPM (Natural Cadence)`.
  - Persists voice speed telemetry inside the History Drawer for every past inquiry.
- **🎙️ Hands-Free Wake Words ("HEY", "TELL", "ABOUT")**:
  - Automatically turns ON and listens when you speak trigger words like **"HEY"**, **"TELL"**, or **"ABOUT"** without needing to touch or click the microphone!
  - Examples:
    - *"Hey tell me about astronaut"*
    - *"Tell me about quantum computing"*
    - *"About black holes"*
- **🔉 Strictly One-Time Spoken Reply**:
  - The voice answers the query **strictly once** without repeating itself or looping.
- **🌐 Real-Time Live Web & AI Browser Knowledge Retrieval**:
  - Automatically queries live web repositories to retrieve real-world facts, scientific definitions, and deep context across any subject.
- **🏷️ Real Extracted Key Words**:
  - Prominent hashtag keywords are extracted directly from the real knowledge data and displayed as glowing tags inside Box 2.
- **📦 Dedicated Rectangle Box with Exactly 3 Sub-Boxes**:
  - **Question Section**: What you asked, your avatar, and timestamp.
  - **Spoken Answer Section**: Factual answer with **`🔊 Replay Voice`**, source attribution badge, latency pill, and **`🗣️ Voice Speed Badge`**.
  - **Box 1: `📝 TEXT — FACTUAL OVERVIEW`**: Comprehensive encyclopedic and AI exploration with voice cadence telemetry.
  - **Box 2: `📌 SUMMARIZATION`**: Executive summary with **`🏷️ Key Words Represented`**.
  - **Box 3: `💡 KEY TAKEAWAYS`**: Bulleted factual takeaways derived from real data.
- **📜 Top-Right History Console**: Access all past inquiries, timestamps, voice speed stats, and full dossiers anytime from the top-right button.
- **Presented by Abhi and Phanendra**: Featured at the bottom of the workspace.

---

## 🚀 Quickstart & Local Setup

### 1. Clone & Navigate
```bash
git clone https://github.com/<YOUR_GITHUB_USERNAME>/IARELS.git
cd IARELS
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Launch Server
```bash
python3 my.py
```

Open your browser to:
👉 **[http://localhost:8000](http://localhost:8000)**

---

## 📁 Repository Structure

```
IARELS/
├── .github/workflows/ci.yml # Automated CI pipeline testing the API on push
├── my.py                    # FastAPI server with wake-word stripping, live web browsing & 3-box model
├── hept.html                # Aesthetic frontend with hands-free wake word listener & history drawer
├── style.css                # Celestial Aurora Olive & Midnight Obsidian Navy stylesheet
├── crazy.css                # Stylesheet alias
├── requirements.txt         # Dependencies
├── .gitignore               # Git ignore rules
└── README.md                # Documentation & GitHub guide
```

---

## 🛠️ GitHub Push Instructions

```bash
cd /Users/phani/Desktop/IARELS
git add .
git commit -m "feat: Hands-free wake words (HEY, TELL, ABOUT) with one-time spoken reply (presented by Abhi and Phanendra)"
git branch -M main
git remote add origin https://github.com/<YOUR_GITHUB_USERNAME>/IARELS.git
git push -u origin main
```
