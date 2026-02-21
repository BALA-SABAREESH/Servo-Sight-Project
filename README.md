# ⚙ Servo-Sight
### Industrial IoT Live Dashboard
**Developed by [IndhuMuruganantham](https://github.com/IndhuMuruganantham)**

---

A real-time monitoring dashboard for a mechanical workshop with live sensor streaming every 30 seconds.

## 🏭 Machines Monitored

| Machine | Model | Sensors |
|---------|-------|---------|
| 3D Printer | PRUSA MK4 | Temp (°C), Vibration (mm/s), Current (A) |
| CNC Mill | HAAS VF-2 | Temp (°C), Vibration (mm/s), Current (A) |
| Air Compressor | ATLAS GA-11 | Temp (°C), Vibration (mm/s), Current (A) |

## ✨ Features

- **Live 30-second sensor polling** with countdown timer
- **Circular gauges** for each sensor metric per machine
- **Sparkline charts** showing the last 20 readings at a glance
- **Status indicators**: RUNNING · IDLE · WARNING · FAULT
- **Alert log panel** with severity levels (warning / fault)
- **Detailed history table** — click any machine card to expand
- **Anomaly detection** — threshold-based status derivation with 8% random spike simulation
- Dark industrial aesthetic with scan-line animation and grid overlay

## 🛠 Tech Stack

- **React 18** + **TypeScript**
- **Vite** (dev server + bundler)
- **Tailwind CSS**
- Pure CSS animations (no animation library needed)

## 🚀 Getting Started

```bash
npm install
npm run dev
```

Open [http://localhost:5173](http://localhost:5173)

## 📁 Project Structure

```
servo-sight/
├── src/
│   ├── main.tsx          # React entry point
│   ├── ServoSight.tsx    # Main dashboard (all components)
│   └── index.css         # Tailwind + global styles
├── index.html
├── vite.config.ts
├── tailwind.config.js
├── tsconfig.json
└── package.json
```

## 🎨 Status Colors

| Status | Color | Condition |
|--------|-------|-----------|
| RUNNING | 🟢 Green | Normal operation |
| IDLE | 🔵 Blue | Low activity |
| WARNING | 🟡 Yellow | Any sensor > threshold |
| FAULT | 🔴 Red | Any sensor > 115% of threshold |
