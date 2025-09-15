# 🎬 Talk-to-Edit: AI-Powered Video Editing

## Inspiration  
Editing videos is powerful but painful. Traditional editors require scrubbing through timelines, hunting clips, and stacking effects.  

We asked: **what if editing was as easy as telling your computer what to do?**  

That’s how this project was born — inspired by Cursor, but reimagined for video editing.  
Instead of `cut()` and drag-and-drop, you just say:  

> “Trim the part where the guy speaking is silent.”  

…and it happens.  

---

## ⚙️ How We Built It  
- **Backend (FastAPI + TwelveLabs + FFmpeg):** Handles video/audio processing, trims clips, adds effects, and generates previews.  
- **NLP (Cohere):** Parses natural language into structured editing commands.  
- **Video Search (Twelve Labs):** Finds key moments (like *“LeBron silent”* or *“when the person dies”*).  
- **Frontend:** A minimal Cursor-like UI with chat-driven commands, video preview, and instant feedback.  
- **Dev Environment (Windsurf):** Used Windsurf’s AI-first IDE to rapidly prototype, refactor, and debug the stack under hackathon time pressure.  

**Workflow:**  
User Command → Cohere (parse intent) → Twelve Labs (find moment)
→ Executor (FFmpeg) → Preview Video

yaml
Copy code

---

## 📚 What We Learned  
- How much AI-powered development environments like Windsurf accelerate building — almost like pair-programming with a senior engineer.  
- How multimodal AI (language + video) can completely reshape creative tools.  
- The trade-offs between real-time performance vs. hackathon prototyping.  
- Why ruthless scoping matters: better to demo **3 magical features** than **10 broken ones**.  
- Even for creative tools, structured pipelines (NLP → search → execution) simplify everything.  

---

## 🚧 Challenges We Faced  
- **Latency:** Running Cohere + server + Twelve Labs was heavy → solved with mocks + pre-indexed demos.  
- **Parsing ambiguity:** Natural language is messy → solved with careful Cohere prompting + heuristics.  
- **Media handling:** Syncing audio overlays with video timelines → FFmpeg saved us.  
- **Time pressure:** 30 hours forced razor-thin scope.  

---

## 🚀 What’s Next  
- Expand effect libraries (glitch, transitions, auto-cuts).  
- Real-time collaboration — multiple users editing via chat.  
- Distributed video rendering for scaling beyond demos.  

---

## 💡 Final Thought  
We set out to answer one question:  

**What if video editing was as simple as talking to your video?**  

This project is our first step toward that future.  

---

## 🛠️ Built With  
- [Cohere](https://cohere.com)  
- [FastAPI](https://fastapi.tiangolo.com/)  
- [FFmpeg](https://ffmpeg.org/)  
- [Twelve Labs](https://twelvelabs.io)  
- [Windsurf](https://codeium.com/windsurf)  
- HTML, CSS, JavaScript, Python  

---
