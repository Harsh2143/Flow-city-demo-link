# FlowCity — AI Crowd Intelligence

**Live demo:** [https://harsh2143.github.io/Flow-city-demo-link/](https://harsh2143.github.io/Flow-city-demo-link/)

FlowCity is a **smart-city crowd intelligence prototype** for Pune. It visualizes crowd density, gate pressure, stampede risk, and forecasts for concerts, sports, festivals, and religious gatherings — with separate dashboards for **citizens**, **authorities**, and **event organizers**.

> **Note:** All metrics are **simulated** for demo purposes. The UI and workflows are designed to plug into real ticket APIs, traffic data, and sensor feeds in production.

---

## Problem

Large public events create unpredictable crowd surges. Citizens need to know *when* to visit; authorities need early warnings; organizers need resource and gate visibility — often with fragmented tools and delayed information.

## Solution

A single-page operations dashboard with:

- Fullscreen **Leaflet** map and color-coded event markers
- **10 real Pune venues** (NH7, IPL at MCA Stadium, Sunburn, Ganpati mandals, Navratri, Holi)
- **Live simulation** (updates every 30s) for scores, ticket scans, and gate utilization
- **Stampede risk alerts**, 2-hour forecasts, parking status, and less-crowded alternatives
- **Authority** city overview, alerts feed, and intelligence override
- **Organizer** footfall forecast, gate pressure, resource stress, and AI recommendations

---

## Screenshots

| Map & events | Citizen detail | Authority view |
|:---:|:---:|:---:|
| Open the [live demo](https://harsh2143.github.io/Flow-city-demo-link/) and select any event on the map | Score ring, gate intelligence, AI reasoning, forecast | City stats, live alerts, override panel |

*Tip: Click **IPL Match** on load for ticketed-event features (scans, gates, stampede alert).*

---

## Features

| Area | Highlights |
|------|------------|
| **Map** | Custom SVG markers by risk level; ticketed **T** badge; tooltips with wait time |
| **Citizen** | Crowd score ring, stampede alert, best visit times, parking, alternatives |
| **Authority** | Critical/watch counts, footfall estimate, live alerts, override + toast |
| **Organizer** | Footfall chart, gate pressure bars, parking/queue/staff/medical stress |
| **Search & filters** | Instant search; chips: All, Ticketed, Ganapati, Navratri, Holi |

---

## Tech stack

- **HTML / CSS / Vanilla JavaScript** (no frameworks — single `index.html`)
- **[Leaflet.js](https://leafletjs.com/)** — interactive maps
- **Inter** + **JetBrains Mono** — typography
- Client-side simulation engine (deterministic random walk within safe ranges)

---

## Run locally

```bash
git clone https://github.com/Harsh2143/Flow-city-demo-link.git
cd Flow-city-demo-link
# Open index.html in a browser, or:
npx --yes serve .
```

---

## Deploy (GitHub Pages)

1. Repo → **Settings** → **Pages**
2. Source: **Deploy from branch** → `main` → `/ (root)`
3. Save — demo will be at `https://harsh2143.github.io/Flow-city-demo-link/`

---

## Data model (demo)

Each event includes: name, venue, coordinates, crowd score (0–100), wait time, trend, risk level, 2-hour forecast, parking, AI signal weights, and verdict text. Ticketed events add scan counts, gate capacity, utilization, and crush-risk status.

**Events:** NH7 Weekender · IPL Match · Sunburn Arena · Dagdusheth Ganpati · Kasba Ganpati · Tulshibaug Ganpati · FC Road Navratri · MIT Navratri · Koregaon Park Holi · Shivajinagar Holi

---

## Roadmap (production)

- [ ] Backend API + WebSocket for live feeds
- [ ] Ticket scan and traffic API integration
- [ ] Rule-based / ML risk scoring (density × flow × exit capacity)
- [ ] Optional LLM layer for natural-language verdicts from structured metrics
- [ ] IoT / CCTV count ingestion (with privacy governance)

---

## Resume

Copy-paste bullets and interview notes: see **[RESUME.md](./RESUME.md)**.

---

## Author

**Harsh** — [GitHub @Harsh2143](https://github.com/Harsh2143)

Smart City / Public Safety · Frontend · HCI prototype

---

*Built as a portfolio project. Metrics are simulated; architecture is intended for real-world data integration.*
