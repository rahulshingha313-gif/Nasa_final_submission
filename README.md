# 🔥 FlameGuard AI

**AI-powered interactive dashboard that turns NASA's microgravity combustion research into clear, actionable fire-safety insights for future Moon and Mars missions.**

🌐 **Live Demo:** https://visionary-dango-20c1ac.netlify.app/

Built by **Team Solstice** for the **NASA Space Apps Challenge 2026**, "Flame in Freefall" challenge.

---

## 📌 Problem

Fire is one of the most dangerous hazards on a spacecraft. In microgravity, flames behave very differently from flames on Earth. They can be spherical, burn at lower temperatures, produce "cool flames" that are invisible to the eye, and respond strongly to oxygen concentration and airflow.

NASA has run many combustion experiments (BASS, Saffire, FLEX, SAME, ACME), but the data is scattered, technical and hard for mission planners, students and researchers to explore and apply.

## 💡 Solution

FlameGuard AI organizes NASA's Physical Sciences Informatics (PSI) combustion research into one easy-to-use web platform. It helps users to:

- Explore and compare experiments
- Understand how oxygen concentration, airflow, pressure and gravity change fire behavior
- Rank investigations by relevance to spacecraft and lunar-habitat fire safety
- Turn research findings into prevention, detection and suppression strategies

---

## ✨ Features

| Module | What it does |
|---|---|
| 🏠 **Home** | Hero video, live mission stats, animated explainer (5 scenes), guided tour |
| 🔎 **Experiment Explorer** | Browse 19 investigations (BASS, Saffire, FLEX, SAME, ACME and more). Filter, sort and compare them with a radar chart |
| 🧠 **AI Relevance Ranker** | Weighted scoring across 5 dimensions (prevention, detection, suppression, material, habitat). Mission scenarios and an auto-generated research brief |
| 🧪 **Flame Lab** | Particle-based flame simulation. Change gravity, airflow, O₂ and pressure and see the flame respond |
| 🗺️ **Flammability Atlas** | O₂ × airflow heat-map showing the Limiting Oxygen Index (LOI) trend by material |
| 🏗️ **Habitat Fire-Risk Planner** | Enter habitat conditions and get a risk index and recommendations. Export as `.txt`, `.json` or print |
| 🎬 **Media Hub** | NASA Image and Video API search, offline SVG illustrations, lightbox, URL or local video loader |
| 🎮 **Arcade** | 3 educational games with a shared local leaderboard (below) |
| 🤖 **AI Assistant** | Local keyword-retrieval chatbot that answers questions about experiments and combustion terms |
| 🛰️ **Live ISS Telemetry** | Real-time ISS data (with simulated fallback if offline) |
| 🔊 **Soundscape** | Generative ambient space audio (Web Audio API), sound effects, volume controls, custom track upload |

### 🎮 Games

1. **Astrobee Drone Defense**: pilot a drone in zero-G physics, use the UV scan to find invisible cool flames, manage the power bus across 3 waves.
2. **Fire Triage Command**: manage 6 spacecraft modules, prioritize fires and build combo multipliers.
3. **Research Quiz**: 10 timed questions on microgravity combustion.

### 🔊 Media

- **Sound:** background ambient audio generated live in the browser (no audio files needed). It starts after the first click because of browser autoplay rules.
- **Video:** canvas-rendered hero video, the NASA Video API, and your own video via URL or file.
- **Images:** NASA Image API plus offline procedural SVG art.

---

## 🧰 Tech Stack

- **HTML5, CSS3, Vanilla JavaScript (ES6+)**, a single self-contained file
- **Chart.js 4.4.1** for charts
- **Canvas API** for the flame lab, hero animation and games
- **Web Audio API** for generative sound
- **NASA Images API** (`images-api.nasa.gov`) for media
- **wheretheiss.at API** for ISS telemetry
- **localStorage** for leaderboard and settings
- Google Fonts: Inter, JetBrains Mono, Orbitron

No build step, no framework and no backend.

---

## 🚀 Run Locally

```bash
git clone https://github.com/<your-username>/FlameGuard-AI.git
cd FlameGuard-AI
# Just open the file in a browser:
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

Or serve it locally:

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

> Rename `FlameGuard-AI.html` to `index.html` for deployment on Netlify, GitHub Pages or Vercel.

## ☁️ Deploy

- **Netlify:** drag and drop the folder (this is how the live demo is hosted).
- **GitHub Pages:** Settings → Pages → Deploy from branch → `main` / root.

---

## ⌨️ Shortcuts

- `Alt + 1` … `Alt + 9`: jump between the 9 sections
- Hash routing: `#explorer`, `#ranker`, `#lab`, `#atlas`, `#planner`, `#media`, `#arcade`, `#about`

---

## 🧠 How the "AI" Works

- **Relevance Ranker:** each investigation has 5 dimension scores. The final score is a weighted sum, adjusted by the selected mission scenario (oxygen-fit scaling plus tag bonuses).
- **LOI model:** a conceptual model of the limiting oxygen index versus gravity, airflow and pressure, used by the Flame Lab and Atlas.
- **Assistant:** local keyword retrieval over a curated FAQ and glossary. It runs fully in the browser with no external AI service.

---

## ⚠️ Disclaimer

FlameGuard AI is an **educational and research-exploration tool**. Relevance scores and physics models are **illustrative editorial estimates** based on public NASA research summaries. They are **not** certified safety tools and must not be used for real spacecraft or habitat safety decisions.

## 📚 Data and Credits

- NASA Physical Sciences Informatics (PSI): https://www.nasa.gov/ (experiments: BASS, Saffire, FLEX, SAME, ACME)
- NASA Image and Video Library API
- ISS position data: wheretheiss.at
- NASA Space Apps Challenge: https://www.spaceappschallenge.org/

This project is not affiliated with or endorsed by NASA.

## 👥 Team Solstice

- **Rahul Singha**, Developer, Premier University Chittagong (PUC)
- *(add teammates here)*

## 📄 License

MIT License. Free to use, modify and share with attribution.

---

⭐ If you like this project, give it a star on GitHub!
