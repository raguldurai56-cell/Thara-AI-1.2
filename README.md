# 🤖 Thara AI 1.2 (Cross-Platform · Online + Offline)

Thara AI is a personal voice assistant built with Python and powered by Ollama. It understands voice commands, opens applications, searches the web, plays music, captures screenshots, and chats with you — and it works in **both online and offline mode** automatically — no switch needed.

> **Version:** 1.2  
> **Platforms:** macOS · Windows · Linux  
> **Language:** Python

---

# ✨ Features

- 🎤 Hybrid Voice Recognition: Google when online (more accurate), Vosk when offline
- 🤖 Local AI Chat using Ollama (Llama 3) — offline
- 🗣️ Offline Text-to-Speech Responses
- 💻 Open Visual Studio Code
- 🌐 Open Google Chrome
- 🧭 Open Safari (macOS only)
- 💬 Open WhatsApp
- 📂 Smart Folder Search
- 📸 Screenshot Capture
- 🎬 Startup GIF Animation
- 🎯 Wake Word Detection ("Thara")
- ▶️ Open YouTube, play songs, Google search, YouTube search (needs internet)

---

# 🔄 Online vs Offline

| Part | Online | Offline |
|------|--------|---------|
| Wake word "Hey Thara" | Vosk | Vosk |
| Your commands | Google speech (accurate) | Vosk (automatic fallback) |
| Voice replies | Works | Works |
| AI chat (Ollama) | Works | Works |
| Open apps / folders / screenshot | Works | Works |
| YouTube, songs, Google search | Works | "No internet boss" |

To always use offline speech, set `PREFER_ONLINE_SPEECH = False` in `main.py`.

---

# 🎙️ Available Voice Commands

| Voice Command | Action | Internet needed? |
|---------------|--------|------------------|
| Thara / Hey Thara | Activate the assistant | No |
| Open Visual Studio Code / Open VS Code | Opens VS Code | No |
| Open Safari | Opens Safari (macOS only) | No |
| Open Chrome | Opens Google Chrome | No |
| Open WhatsApp | Opens WhatsApp (web version if app not found) | No (web: yes) |
| Open Folder Downloads | Opens Downloads folder | No |
| Open Folder Desktop | Opens Desktop folder | No |
| Open Folder Documents | Opens Documents folder | No |
| Screenshot | Captures a screenshot | No |
| Tell me about yourself / Introduce yourself / Who are you | Thara introduces itself | No |
| Stop Thara | Closes Thara AI | No |
| Anything else | Answered by the local AI (Ollama) | No |
| Open YouTube | Opens YouTube | Yes |
| Play Believer | Plays the song on YouTube | Yes |
| Search Google for Python | Searches Google | Yes |
| Search YouTube for AI | Searches YouTube | Yes |

---

# 🛠️ Technologies Used

- Python
- Vosk (offline speech recognition)
- SpeechRecognition (Google speech when online)
- sounddevice (microphone)
- pyttsx3 / macOS `say` (offline voice)
- Ollama
- mss (screenshots)
- PyWhatKit (YouTube playback)

---

# 📦 Requirements

- Python 3.10 or later
- macOS, Windows or Linux
- Ollama installed + Llama 3 model (`ollama pull llama3`)
- Vosk speech model (see below)
- Working microphone
- Internet is needed once for setup. After that Thara works offline too; online commands and better speech accuracy need internet

---

# 🚀 Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/Thara-AI-1.2.git
cd Thara-AI-1.2
```

### 2. Install Python packages

```bash
pip install -r requirements.txt
```

### 3. Linux only — install system packages

```bash
sudo apt install espeak-ng libportaudio2
```

### 4. Download the offline speech model (one time)

1. Download **vosk-model-small-en-us-0.15** from https://alphacephei.com/vosk/models
2. Unzip it
3. Rename the folder to `model` and put it next to `main.py`

### 5. Set up the offline AI (one time)

```bash
ollama pull llama3
```

### 6. Run Thara AI

```bash
python main.py
```

---

# 📁 Project Structure

```
Thara-AI-1.2
│
├── main.py
├── gif_viewer.py
├── requirements.txt
├── README.md
├── thara_animation.gif
├── thara_animation.html
├── model/              (Vosk speech model - you download this)
└── screenshots/        (created automatically)
```

---

# ⚙️ How It Works

1. Launch Thara AI.
2. The startup animation will appear.
3. Thara activates the microphone.
4. Say **"Hey Thara"** (or just "Thara") to wake the assistant.
5. Thara replies **"Yes Boss"**.
6. Speak your command.
7. Thara processes and executes your request.

---

# 💬 Example

```
You: Hey Thara

Thara: Yes Boss

You: Open Chrome

Thara: Opening Chrome

(You can also say it together: "Hey Thara, open Chrome")
```

---

# ⚠️ Notes

- Make sure your microphone permission is enabled (macOS: System Settings → Privacy → Microphone).
- Ollama must be running for AI chat.
- If the wake word does not trigger, add the way it was heard to `WAKE_WORDS` in `main.py`.
- On Linux, screenshots may not work on Wayland (use an X11 session).
- Safari exists only on macOS.

---

# 🚀 Thara AI 1.7 — Coming Soon

Thara AI 1.7 is currently under active development and will introduce a major upgrade over version 1.2.

### Planned Features

- 🧠 Smarter AI Engine
- ⚡ Faster Performance
- 🎨 Modern User Interface
- 🎙️ Improved Voice Recognition
- 🤖 Advanced AI Automation
- 🔥 More Powerful Voice Commands
- 💎 Exclusive Premium Features

Stay tuned for future updates.

Thank you for supporting Thara AI! ❤️

---

# 👨‍💻 Author

Developed with ❤️ by **Taha**

If you like this project, please consider giving it a ⭐ on GitHub.

---

# 📄 License

This project is licensed under the MIT License.
