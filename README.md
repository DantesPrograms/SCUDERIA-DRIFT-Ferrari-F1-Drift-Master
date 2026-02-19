# 🏎️ SCUDERIA DRIFT — Ferrari F1 Drift Master

A fully-featured, browser-based top-down drifting game built in a single HTML file. No dependencies, no install — just open and race.

---

## 🚀 Getting Started

1. Download `ferrari-drift.html`
2. Open it in any modern browser (Chrome, Firefox, Edge, Safari)
3. Press **Enter** or **Space** (or click the button) to start
4. Go sideways

---

## 🎮 Controls

| Input | Action |
|---|---|
| `W` / `↑` | Throttle |
| `S` / `↓` | Brake / Reverse |
| `A` / `←` | Steer Left |
| `D` / `→` | Steer Right |
| `Space` | **Drift** (hold to slide) |
| `Shift` / `N` | **Nitro Boost** |
| `R` | Reset Car Position |

---

## 🏁 How to Score Points

Drift points are calculated in real-time based on three factors:

- **Drift Angle** — the bigger the angle between your car direction and velocity, the more points per second
- **Speed** — faster drifts score more
- **Combo Multiplier** — the longer you hold a single drift, the higher your multiplier climbs (up to ×10)

Points are **banked** the moment your drift ends. A longer, faster, more sideways drift = a bigger payout.

### Drift Zones
Red and orange marked areas on the arena floor apply a score multiplier (×2 or ×3) to any points earned while drifting inside them. Stack them with a high combo for massive runs.

---

## ⚙️ Systems & Features

### 🔴 Ferrari F1 Car
A hand-drawn top-down Ferrari F1 car (#16) complete with front wing, rear wing, sidepods, halo, helmet, and wheel rims. The car body glows red during active drifts.

### ⚡ Nitro
- Collected from **blue orbs** scattered around the arena, or regenerates slowly over time
- Hold `Shift`/`N` to activate — applies a 1.7× speed multiplier and blue exhaust flame particles
- Monitor the **NITRO** bar at the bottom left

### 🔥 Turbo
- Builds passively while you drift
- At 50%+ turbo, your engine gets an automatic 15% speed bonus
- Collect **orange orbs** for a direct +60 turbo charge
- Drains when a drift ends

### 🌡️ Tire Heat
Four individual tire indicators (FL, FR, RL, RR) track heat in real-time:
- **Green** — cold tires, maximum grip
- **Yellow** — warming up
- **Red** — overheated, maximum smoke output

Rear tires heat up significantly faster during drifting.

### 💨 Tire Smoke
Smoke is emitted from both rear tires during a drift. Color shifts from **white → grey → black** as tires heat up. Smoke particles expand and fade naturally over time.

### 🛞 Skid Marks
Skid marks are drawn directly onto the world canvas and persist for the entire session, building up over time to create a realistic drifting history across the arena floor.

### 💥 Wall Collision & Damage
- Hitting a wall at speed causes **chassis damage** (0–100%)
- The impact bounces the car back and triggers a screen shake + explosion particle burst
- At 80%+ damage a critical warning fires — keep away from the walls

### 🏆 Combo System
| Drift Duration | Combo |
|---|---|
| 0–3s | ×1 |
| 3s+ | ×2 |
| 6s+ | ×3 |
| 9s+ | ×4 |
| ...and so on | up to ×10 |

Each new combo tier triggers a screen flash and notification.

### 🎵 Procedural Audio
Engine sound is generated via the Web Audio API — no audio files required. Pitch and volume respond to RPM and speed in real-time. Tire screech is a filtered noise source that fades in during drifts.

### 📷 Camera
- Follows the car with smooth lerp interpolation
- **Lookahead** — camera offsets in the direction of travel so you can see what's ahead
- **Speed zoom** — the camera zooms out slightly at high speeds for better awareness
- **Screen shake** — triggered on wall impacts and powerup collection

---

## 📊 HUD Reference

| Element | Location | Description |
|---|---|---|
| **Drift Points** | Top Center | Current drift run score (resets on landing) |
| **Combo / Session** | Top Center | Active multiplier and total session points |
| **Drift Angle** | Top Right | Current slip angle in degrees |
| **Speed** | Bottom Center | Speed in KMH |
| **Gear** | Bottom Center | Current gear (N / 1–6) |
| **RPM Bar** | Bottom Center | Engine RPM with redline indicator |
| **Lap Timer** | Bottom Center | Time since last crossing the start gate |
| **Nitro Bar** | Bottom Left | Current nitro level |
| **Turbo Bar** | Bottom Left | Current turbo charge |
| **G-Force Circle** | Left Side | Real-time lateral and longitudinal G forces |
| **Tire Heat** | Right of Minimap | 4 colored squares showing per-tire temperature |
| **Chassis Bar** | Top Left | Damage percentage |
| **Session Stats** | Top Right | Total drifts, max speed, best combo, powerups |
| **Minimap** | Bottom Right | Full arena overview with car, cones, and orbs |

---

## 🗺️ Arena Layout

- **4000×4000** world with red-striped walls on all sides
- **Traffic cones** placed in concentric rings — knock them out of the way
- **Drift zones** in four corners / edges with multiplier overlays
- **12 powerup orbs** (6 nitro, 6 turbo) that respawn after 12 seconds
- **Checkered start/finish gate** in the center for lap timing

---

## 🛠️ Technical Details

| Property | Value |
|---|---|
| Language | Vanilla HTML / CSS / JavaScript |
| Rendering | HTML5 Canvas 2D API |
| Audio | Web Audio API (procedural, no files) |
| File Size | Single `.html` file, ~700 lines |
| Dependencies | Google Fonts (Orbitron, Rajdhani) — loaded via CDN |
| Browser Support | All modern browsers (Chrome recommended) |
| Physics | Custom arcade physics — grip/drift lateral friction model |

---
