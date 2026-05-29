# FlowCity — Resume & Interview Guide

Use this file when adding FlowCity to your resume, LinkedIn, or portfolio. **Be honest:** say *prototype* or *simulated data* unless you add a real backend.

---

## One-line pitch

> FlowCity is a crowd-intelligence dashboard prototype for Pune events — map-based monitoring, multi-role views, and simulated risk/forecast UX for citizens, authorities, and organizers.

---

## Resume bullets (pick 2–3)

**Frontend-focused**

- Built **FlowCity**, a single-page crowd-intelligence dashboard (**HTML/CSS/JS**, **Leaflet**) with map markers, live simulation, and role-based UIs for citizens, authorities, and event organizers.
- Designed **Apple-style** responsive interface with risk-coded visuals, animated score rings, gate crush alerts, and 2-hour crowd forecasts across **10 Pune venues**.
- Implemented client-side state management, search/filter, map fly-to, and sliding panels with no frameworks — deployed on **GitHub Pages**.

**Full-stack angle** (use after you add an API, or soften as “architecture-ready”)

- Architected FlowCity as a **decision-support prototype** with JSON event model and 30s simulation loop, structured for future integration with ticket, traffic, and sensor APIs.

**Smart city / product angle**

- Prototyped **smart-city crowd safety** workflows: stampede alerts, authority override feed, organizer resource stress — targeting festivals, sports, and religious gatherings in Pune.

---

## Links to put on resume

| Label | URL |
|-------|-----|
| Live demo | https://harsh2143.github.io/Flow-city-demo-link/ |
| Source | https://github.com/Harsh2143/Flow-city-demo-link |

---

## Skills to tag

`JavaScript` · `HTML/CSS` · `Leaflet` · `Data Visualization` · `UI/UX` · `Smart City` · `Responsive Design` · `Git` · `GitHub Pages`

---

## Interview: “Is the data real?”

**Good answer:**  
“No — it’s a **UX and workflow prototype**. Scores and gates update via a simulation engine every 30 seconds. In production I’d ingest ticket scan rates, traffic APIs, and optionally sensor or CCTV counts, then run a rule-based or ML risk model. The frontend is already structured around an event JSON model so swapping simulation for an API is straightforward.”

---

## Interview: “How would you calculate crowd risk?”

**Good answer:**  
“Combine **density**, **arrival rate vs exit capacity**, **gate utilization**, and **historical peaks** for that venue. Stampede risk rises when density is high *and* flow is constrained — e.g. one gate above 85% with a large approaching queue. The UI reflects that with gate cards and stampede countdowns; the math would live on the server in production.”

---

## Interview: “Hardest technical part?”

Pick one you actually built:

- Syncing **map markers**, **sidebar selection**, and **right panel** across three views without a framework.
- **Gate intelligence** UX — OK / WATCH / CRUSH states with thresholds and warnings.
- **Authority vs citizen vs organizer** — same data, different layouts and actions (override vs alternatives vs resource stress).

---

## What NOT to claim (unless you build it)

- ❌ “Trained XGBoost model” — not in this repo  
- ❌ “Real-time IoT integration” — roadmap only  
- ❌ “Production AI predicts stampedes” — say *prototype / simulated*

---

## Optional next steps (strengthen resume later)

1. Add screenshot images to `README.md` (`/docs/screenshots/`)
2. Small **Node/Python API** serving the same JSON + GitHub Pages frontend
3. One **Gemini** endpoint that rewrites `aiVerdict` from metrics (label clearly as demo)

---

*Last updated: May 2026*
