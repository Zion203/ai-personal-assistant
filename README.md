🧠 Project: SARAH – Smart AI Runtime Assistant for Humans
“Not just another assistant. Sarah thinks. Sarah acts.”

✅ Mission
Build a Python-based local assistant that understands natural language commands using an LLM (Gemini or DeepSeek), and takes meaningful local actions on your computer—like a powerful sidekick.

🛠️ Core Capabilities of SARAH (v1.0 Plan)
#	Feature	Description	Tech
1️⃣	🎛️ Global Hotkey + Popup	Press Ctrl+Shift+S to bring up Sarah	keyboard, tkinter
2️⃣	🤖 LLM Query	Sarah sends your message to Gemini/DeepSeek	google.generativeai / deepseek_sdk
3️⃣	🧠 Command Parsing	LLM returns JSON like {action: "open_app", args: {"name": "Chrome"}}	Built-in JSON parsing
4️⃣	⚙️ Action Dispatcher	Sarah maps actions to real Python functions	Python dict, dispatcher pattern
5️⃣	📂 Open Apps	"Open Chrome", "Launch VSCode", etc.	subprocess.Popen, os
6️⃣	🎵 Play Songs	"Play Blue Bird" → open Spotify or YouTube	webbrowser, pywhatkit, optional Spotify API
7️⃣	⏰ Reminders	"Remind me to drink water in 30 min"	apscheduler, plyer toast
8️⃣	🧠 Memory (Recall)	"Remember that I have test on Monday" → recall later	TinyDB or JSON
9️⃣	💼 Modes	"Work mode" or "Fun mode" triggers app bundles	Python macro
🔟	⚠️ Screen Time Alerts	Warn if using YouTube or Chrome for too long	psutil, timer system

🧩 Future (v2.0 and beyond)
🌱 Idea	Description
Voice command	Mic input using speech_recognition
Voice reply	Sarah speaks back using pyttsx3
Context Memory	“Remind me tomorrow” → use clock
File manager tools	“Open downloads folder”, “Search for PDF”
Smart scheduling	“Schedule Python session every Monday”
Weather, news	“What’s today’s weather?” via web scraping/API
Chat + jokes	Conversational fallback when no action is found

📁 Folder Structure (Early)
pgsql
Copy
Edit
sarah/
├── main.py              ← Entry point
├── ui/
│   └── popup.py         ← Tkinter popup UI
├── core/
│   ├── dispatcher.py    ← Maps commands to actions
│   ├── actions.py       ← Functions like open_app, play_song
│   └── memory.py        ← Save/recall user memories
├── llm/
│   ├── gemini_api.py    ← Gemini API connection
│   └── deepseek_api.py  ← (optional alt)
├── config/
│   └── settings.json    ← App path configs
└── utils/
    └── tools.py         ← Time parsing, string cleanup, etc.
⏳ Timeline
Day	Goal	Status
✅ Day 1	Finalize Vision, Features, Name	✔️ Done — "Sarah" it is
🔜 Day 2	Popup UI + Hotkey + App Open (MVP1)	Next
🧠 Day 3	LLM integration + command routing	Soon
💥 Day 4	Implement 3 tools: play_song, open_app, reminder	Soon
📅 Day 5	Memory & recall system	Soon
🧪 Day 6	Full test run: "Play Naruto", "Work mode"	Soon
🎁 Day 7	Polish, GitHub, show-off ready	Soon








