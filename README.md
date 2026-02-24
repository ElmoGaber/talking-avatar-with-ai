# Talking Avatar with AI

![License](https://img.shields.io/badge/License-MIT-yellow.svg)
![React](https://img.shields.io/badge/React-18-blue?logo=react)
![Three.js](https://img.shields.io/badge/Three.js-Ready-black?logo=three.js)
![AI Voice](https://img.shields.io/badge/AI%20Voice%20%26%20Lip%20Sync-Integrated-brightgreen)

**Interactive web-based talking avatar** powered by AI — users type or speak text, the avatar listens, generates natural voice using text-to-speech, and performs realistic lip-sync animation in real-time using 3D facial models.

Perfect for virtual assistants, educational tools, language learning, customer support demos, or creative storytelling applications.

---

## ✨ Features

- Realistic 3D humanoid avatar with facial expressions and lip synchronization  
- Real-time text-to-speech voice generation (multi-language support)  
- Accurate lip-sync driven by viseme analysis from TTS output  
- Natural head movements, eye blinks, and subtle idle animations  
- Text input field + optional microphone speech-to-text  
- Responsive design — works on desktop and mobile browsers  
- Customizable avatar appearance (skin tone, hair, clothing — depending on implementation)  
- Smooth animations using Three.js and morph targets / blend shapes  
- Low-latency response pipeline for conversational feel  
- Clean, modern UI with dark/light theme toggle  

---

## 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/ElmoGaber/talking-avatar-with-ai.git
cd talking-avatar-with-ai
```

# Install dependencies
```
npm install
# or
yarn install
```

# Start development server
```
npm run dev
# or
yarn dev
```
Open http://localhost:5173 (or the port shown)

## 🛠 Tech Stack

Frontend Framework: React 18 + Vite
3D Rendering & Animation: Three.js + @react-three/fiber
Avatar Model: Ready Player Me / custom GLB/GLTF with morph targets
Lip Sync: Rhubarb Lip Sync / Viseme mapping / Wav2Lip-style analysis
Text-to-Speech: ElevenLabs / Google Cloud TTS / Microsoft Azure TTS / Web Speech API
Speech-to-Text (optional): Web Speech Recognition API / Whisper via API
State Management: Zustand / React Context
Styling: Tailwind CSS or styled-components
Build Tool: Vite
Package Manager: npm / yarn

```
📁 Project Structure
texttalking-avatar-with-ai/
├── apps/                     # Main application source (React app)
├── resources/                # 3D models, audio samples, textures
├── public/                   # Static assets
├── src/                      # React source code
│   ├── components/           # Avatar, UI controls, input form
│   ├── scenes/               # Three.js scene setup & animation logic
│   ├── services/             # TTS, STT, lip-sync providers
│   ├── hooks/                # Custom hooks (animation, audio)
│   └── App.jsx / main.jsx
├── .idea/
├── package.json
├── package-lock.json
├── yarn.lock
├── .gitignore
├── LICENSE
└── README.md
```
## 🎯 How It Works (Core Pipeline)

User enters text or speaks → captured via input / microphone
Text is sent to TTS engine → generates audio waveform + timing metadata
Audio is analyzed → extracts visemes / phonemes with timestamps
Viseme sequence drives facial blend shapes / morph targets on 3D model
Head rotation, eye gaze, and idle animations layered on top
Audio played synchronously with animation
Real-time rendering in Three.js canvas


## 🔧 Customization & Extension Points

Swap TTS provider (ElevenLabs → PlayHT → Coqui TTS local)
Change avatar model (Ready Player Me → MetaHuman → custom rigged)
Add emotion detection from text / voice tone
Implement multi-avatar conversations
Support sign language avatar (future)
Integrate with chatbot backend (LangChain / OpenAI)
Add background environments / scenes
Record & export talking avatar videos
