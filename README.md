# PACE — Mile Performance Tracker

> *Built by a runner, for runners who think in data.*

**PACE** is a personal performance analytics tool that tracks mile times alongside the factors that actually influence them — sleep, hydration, nutrition, weather, mental state, training load, and more. Instead of guessing why a run felt fast or slow, PACE shows you.

🔗 **[Live App →](https://babaganoosh2020.github.io/pace-mile-tracker)**

---

## Why I Built This

I'm a junior and a competitive XC and track & field athlete. After years of logging miles, I kept noticing patterns — great sleep before a race, a tailwind, caffeine at the right time — but I had no systematic way to track what was actually moving the needle on my mile time.

Most running apps track *what* you ran. PACE tracks *why* you ran it the way you did.

This project is also part of my journey building a CS/engineering portfolio as I explore Computer Engineering, Mechanical Engineering, and Biomedical Engineering for college. It's the first tool I've built that solves a problem I personally face every day.

---

## Features

### 📋 Log Run
Capture 30+ factors across five categories every time you run:

| Category | Factors Tracked |
|---|---|
| **Performance** | Mile time, run type (race/workout/easy), surface, shoes |
| **Body & Recovery** | Sleep hours, sleep quality, resting heart rate, soreness, illness, weekly mileage, days since last hard workout |
| **Nutrition & Hydration** | Water intake, pre-run meal type & timing, carb load, caffeine dose & timing, total calories |
| **Environment** | Temperature, humidity, wind speed & direction, season, time of day, air quality, altitude |
| **Mental & Warmup** | Stress level, motivation, warmup duration & quality, notes |

### 📊 Dashboard
- Personal record, latest time, and rolling average displayed at a glance
- Progress chart over time with PR baseline marker
- Instant delta showing if your latest run was faster or slower than the previous

### 📁 History
- Full run log in reverse chronological order
- Color-coded tags for sleep, hydration, soreness, and conditions
- PR badge automatically applied to best runs

### 💡 Insights *(unlocks after 3 runs)*
- **Best conditions** — averages from your top performing runs
- **Time of day comparison** — when do you actually run fastest?
- **Sleep impact** — 7+ hours vs under 7, quantified in seconds
- **Shoe comparison** — how much faster are your racing flats really?
- **Factor correlations** — Pearson correlation coefficients showing which variables statistically correlate with your mile time

---

## The Stats Behind It

The Insights tab uses the **Pearson correlation coefficient** — a real statistical measure used in sports science and data analysis:

```
r = Σ[(xi - x̄)(yi - ȳ)] / √[Σ(xi - x̄)² · Σ(yi - ȳ)²]
```

Output ranges from **-1.0 to +1.0**:
- **Negative** → as the factor increases, mile time decreases *(faster = good)*
- **Positive** → as the factor increases, mile time increases *(slower = bad)*
- **Near 0** → no relationship detected

The more runs logged, the more statistically meaningful the correlations become. This is the same methodology used in exercise physiology research.

---

## Tech Stack

```
HTML5          →  structure and layout
CSS3           →  custom properties, grid, animations, pseudo-elements
Vanilla JS     →  all logic, data processing, DOM manipulation
localStorage   →  client-side data persistence (no server needed)
Chart.js 4.4   →  progress visualization
Google Fonts   →  Bebas Neue + DM Mono + DM Sans
```

**No frameworks. No backend. No dependencies to install.**  
One file. Opens in any browser. Works offline.

---

## Key Concepts Used

- **localStorage API** — persists run data across sessions without a database
- **JSON.stringify / JSON.parse** — serializes JavaScript objects for storage
- **Array.map() / Array.reduce()** — functional data transformation and aggregation
- **Pearson correlation** — statistical analysis of factor relationships
- **CSS custom properties** — design token system for consistent theming
- **Event-driven programming** — all UI interactions driven by user events
- **Chart.js** — external library integration for data visualization
- **CSS pseudo-elements** — `::before` for the animated grid background

---

## Getting Started

No installation needed.

**Option 1 — Use the live app:**  
👉 [https://babaganoosh2020.github.io/pace-mile-tracker](https://babaganoosh2020.github.io/pace-mile-tracker)

**Option 2 — Run locally:**
```bash
git clone https://github.com/babaganoosh2020/pace-mile-tracker.git
cd pace-mile-tracker
# Open index.html in any browser
open index.html
```

**Option 3 — Download:**  
Click `Code` → `Download ZIP` → open `index.html`

> ⚠️ Data is stored in your browser's localStorage. Clearing browser data will erase your runs. Export feature coming in a future version.

---

## Roadmap

Features planned for future versions:

- [ ] Export runs to CSV for analysis in Excel / Google Sheets
- [ ] Race predictor (estimate 5K time from mile PR + training load)
- [ ] Weather API integration (auto-fill conditions from GPS location)
- [ ] Training load calculator (acute:chronic workload ratio — a key injury prevention metric used in sports science)
- [ ] Mobile-optimized PWA (installable on phone for logging immediately after a run)
- [ ] Data visualization for individual factor deep-dives

---

## What I Learned

Building PACE taught me several things that go beyond the code:

**Technically:** How to structure a single-page app without a framework, how localStorage works as a lightweight persistence layer, how to implement a real statistical algorithm (Pearson correlation) from scratch in JavaScript, and how Chart.js handles dynamic data.

**As an athlete:** Logging even a few weeks of data reveals patterns that feel intuitive but are hard to confirm — sleep and hydration matter more than I thought, caffeine timing matters a lot, and racing flats are genuinely worth the hype.

**As an aspiring engineer:** The intersection of data, biology, and performance optimization is exactly what draws me toward CE/ME/BME. This project sits at all three.

---

## About

Built by **Arjun** ([@babaganoosh2020](https://github.com/babaganoosh2020))  
Junior · XC & Track and Field athlete · Aspiring CE / ME / BME student  

---

## License

[MIT](LICENSE) — free to use, modify, and build on.  
If you use this or build something inspired by it, I'd love to know.

