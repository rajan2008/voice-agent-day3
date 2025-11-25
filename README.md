# 🌿 Day 3 – Wellness Check-in Voice Agent

AI Voice Agent Challenge – Murf AI x LiveKit

🚀 Overview

For Day 3, you build a Daily Wellness Check-in Agent using:

LiveKit Agents SDK (Python)

Deepgram STT

Google Gemini LLM

Murf Falcon TTS

Silero VAD + Turn Detection

This agent asks the user one question at a time, collects mood/energy/stress/goals, generates personalized wellness advice, and saves each check-in in local JSON logs.

🎯 Goals Completed
✔ 1. Ask one question at a time

The agent now waits for the user’s response before asking the next question.

✔ 2. Emotional, supportive wellness agent

No medical advice — only gentle emotional wellness suggestions.

✔ 3. Persistent logging system

All check-ins are saved to:
```
/backend/wellness_logs/wellness_log.json
```

Each entry contains:
```
{
  "timestamp": "...",
  "mood": "...",
  "energy": "...",
  "stress": "...",
  "goals": ["..."],
  "summary": "Mood: X. Energy: Y. Stress: Z. Goals: ...",
}
```
✔ 4. Original advice engine

Not templates — a programmatically generated supportive paragraph based on mood/energy/stress/goals.

✔ 5. Murf Falcon TTS working with Tanushree voice

The voice agent speaks smoothly using:

voice="tanushree"
style="Conversation"

✔ 6. Frontend + Backend connected and working with LiveKit

Fully tested through browser conversation.

📁 Project Structure
```
voice-agent-day3/
│
├── backend/
│   ├── agent.py                 ← Main Day 3 logic
│   ├── welless_logs/            ← Auto-created wellness history
│   ├── .env.local
│   ├── requirements.txt
│   └── ...
│
└── frontend/
    └── (same as Day 1 & Day 2 starter)
```
⚙️ Tech Stack
Component	Technology
Speech-to-Text	Deepgram Nova-3
LLM	Google Gemini 2.5 Flash
Text-to-Speech	Murf Falcon Voice (Tanushree)
VAD/Turn Detection	Silero VAD + Multilingual Model
Runtime	LiveKit Agents SDK
▶️ How to Run (Backend)
1. Activate virtual environment
.\.venv\Scripts\activate

2. Install dependencies
```
pip install -r requirements.txt
```
4. Run agent
```
python agent.py
```
▶️ How to Run (Frontend)
```
cd frontend
npm install
npm run dev
```

Open browser → connect to your agent → start speaking.

💬 Conversation Flow (Example)

Agent:
Hi! I help you reflect on your day. How are you feeling right now?

User:
A bit tired honestly.

Agent:
Thanks — I’ve recorded your mood as tired. How is your energy today?

User:
Low.

Agent:
Okay — energy set to low. Are you stressed today?

…and so on.

At the end, the agent saves a history entry and gives personalized advice.

