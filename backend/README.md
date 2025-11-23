🎙️ Voice Agent Backend

This backend handles the real-time communication between the user and the AI voice agent.

✅ Features

Real-time audio input/output

Speech-to-text pipeline

AI response handling

Fast Murf Falcon TTS

LiveKit voice session integration

📂 Backend Structure
src/
└─ agent.py   # Main entry point for the voice agent

⚙️ Setup & Installation
1️⃣ Install dependencies
uv sync

2️⃣ Run the backend
uv run python src/agent.py dev

🔑 Environment Variables

Create a .env file and add:

LIVEKIT_API_KEY=your_key
LIVEKIT_API_SECRET=your_secret
MURF_API_KEY=your_key


(Use your actual keys)

🧠 How It Works

Agent listens to user audio

Converts speech → text

Processes the text for a response

Converts text → speech using Murf Falcon

Sends audio back to the user in real time

🚀 Future Enhancements

Agent memory

Custom prompts

Web-based UI

Multi-language support

✅ Requirements

Python 3.10+

LiveKit account

Murf API access
