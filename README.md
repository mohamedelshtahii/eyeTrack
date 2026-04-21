# eyetrack 👁️
## 🌐 Live Demo

👉 https://vocal-starship-6b4f11.netlify.app/

**Eye Infection Recovery Dashboard (Browser‑Only AI Tool)**

A lightweight, privacy‑first web app that tracks eye infection recovery in real time using your webcam, computer vision, and optional AI voice guidance.


<img width="700" height="600" alt="image" src="https://github.com/user-attachments/assets/e448edce-6330-415e-8637-c2b3fb731db4" />

## ✨ What is eyetrack?

**eyetrack** is a fully client‑side dashboard that helps monitor recovery from eye infections (e.g. conjunctivitis, chalazion) by measuring eye openness, symmetry, and blinking using **MediaPipe Face Mesh**.

It can optionally connect to an AI assistant (**Iris**) that explains your condition using vision analysis and voice — all without a backend.

---

## ✅ Key Features

- 478‑point MediaPipe face mesh (live)
- Eye metrics: **EAR, asymmetry, relative openness**
- Real‑time recovery colour feedback
- AI image analysis (optional)
- Voice narration + two‑way Q&A
- Session history (local only)
- **No server · No database · No build step**

---

## 🚀 Getting Started

> A local HTTP server is required (ES modules).

### Option 1 — VS Code (recommended)
1. Install **Live Server**
2. Open `index.html` → **Open with Live Server**
Option 3 — Node
npx serve .
⚙️ Setup (Optional AI)

Open Settings
Add Anthropic API key (enables vision + Iris)
(Optional) Add ElevenLabs API key for premium voice
Select infected eye → Start Session


Works without AI — all measurements run locally.


📊 Metrics Used

EAR (Eye Aspect Ratio)
Relative Openness (%)
Left–Right Asymmetry
Blink detection
Lid morphology

Colour Guide
Colour Meaning
🔴 Red    Poorly open
🟡 Amber  Improving
🟢 Green   Near recovery
🔵 Cyan    Healthy eye

🧠 Iris (Voice Assistant)
Click Ask Iris, speak a question, and get a spoken answer based on:

Your live measurements
Session history
Latest AI vision analysis


Iris always recommends a doctor for severe cases.


🧩 Tech Stack

HTML5 · CSS3 · JavaScript (ES Modules)
MediaPipe FaceLandmarker
Chart.js
Claude Vision (browser fetch)
Web Speech API / ElevenLabs
localStorage

eyetrack/
├── index.html
├── css/style.css
├── js/
│   ├── app.js
│   ├── facetracker.js
│   ├── measurements.js
│   ├── ai.js
│   └── voice.js
└── README.md

🔒 Privacy

Webcam processed locally (MediaPipe WASM)
No backend — ever
Data & API keys stored only in your browser

⚠️ Limitations

Chrome / Edge for voice input
Camera requires HTTPS or localhost
AI features require internet & API key


### Option 2 — Python
```bash
python -m http.server 8080
