<div align="center">

# 🪐 ApexCube Cosmic Lab

### A premium WebGL Rubik’s Cube simulator for speedcubers, cube geeks, and interaction design lovers.

一个面向魔方极客、速拧玩家与 3D 交互爱好者的高拟真魔方实验室。  
集成多阶魔方、贴纸级拖拽、WCA 风格计时、成绩统计、公式执行、智能还原与宇宙级视觉动效。

<br />

<p>
  <img alt="HTML5" src="https://img.shields.io/badge/HTML5-0f172a?style=for-the-badge&logo=html5&logoColor=ff6b35">
  <img alt="Three.js" src="https://img.shields.io/badge/Three.js-0f172a?style=for-the-badge&logo=three.js&logoColor=white">
  <img alt="WebGL" src="https://img.shields.io/badge/WebGL-0f172a?style=for-the-badge&logo=webgl&logoColor=00e5a0">
  <img alt="Rubik Cube" src="https://img.shields.io/badge/Rubik's_Cube-0f172a?style=for-the-badge&logoColor=white">
</p>

<p>
  <a href="#-features">Features</a> ·
  <a href="#-quick-start">Quick Start</a> ·
  <a href="#-controls">Controls</a> ·
  <a href="#-architecture">Architecture</a> ·
  <a href="#-roadmap">Roadmap</a>
</p>

<br />

> **ApexCube Cosmic Lab** is not just a cube on a screen.  
> It is a polished, interactive, high-fidelity cube playground built with Three.js — crafted for fast turning, visual immersion, and algorithm exploration.

</div>

---

## ✨ Preview

> Replace the placeholders below with your own screenshots or GitHub Pages demo link.

<p align="center">
  <img src="./assets/preview.png" alt="ApexCube Cosmic Lab Preview" width="920">
</p>

<div align="center">

**Live Demo:** `https://muskke.github.io/apexcube-cosmic-lab/`

</div>

---

## 🚀 Features

### 🧊 Multi-order cube engine

ApexCube supports multiple cube orders with consistent physical behavior:

- **3×3** standard speedcubing cube
- **4×4** master cube with inner-layer moves
- **5×5** advanced cube with middle-layer and multi-wide moves
- Unified cubie-based state system
- Smooth animated rotations with instant-turn support
- Layer, wide-layer, middle-layer, and whole-cube rotations

---

### 🖱️ Sticker-level gesture interaction

The cube can be turned directly from the visible stickers.

- Raycast-based sticker picking
- Drag direction resolved in local 3D cube space
- Physical layer detection from the touched sticker
- Supports mouse and touch input
- Prevents accidental camera dragging during sticker turns
- Consistent drag-to-turn behavior across 3×3 / 4×4 / 5×5

This makes the cube feel closer to a real physical puzzle instead of a button-only simulator.

---

### ⚡ Speed-oriented move queue

ApexCube includes a non-blocking move queue designed for rapid input.

- Keyboard burst input support
- Automatic acceleration when the queue grows
- Smooth animation under normal use
- Near-instant execution during high-speed formula input
- Move history recording
- Undo support

The result is a cube that remains responsive even when formulas are entered aggressively.

---

### ⌨️ Keyboard speedcubing controls

Built-in keyboard mapping covers standard and advanced moves.

- `U D L R F B` outer-layer turns
- `Shift + key` inverse turns
- `Alt + key` inner-layer turns
- `Ctrl + key` wide turns
- `Ctrl + Alt + key` three-layer wide turns on 5×5
- `M E S` middle-layer moves
- `X Y Z` whole-cube rotations
- `Space` WCA-style timer control
- `Esc` timer cancel

---

### 🧠 Algorithm console

A dedicated algorithm input panel lets you run standard cube notation directly.

Supported examples:

```txt
R U R' U'
F R U R' U' F'
Rw U Rw' U'
M E S
X Y Z
```

It also includes:

- Formula execution
- Formula inversion
- Move archive
- History copy
- Clean reset

---

### ⏱️ WCA-inspired timer dashboard

ApexCube includes a built-in timing experience for practice sessions.

- Hold-space preparation flow
- Large fullscreen timer overlay
- PB tracking
- Ao5 / Ao12 statistics
- TPS peak display
- Recent solve history
- Local persistent stats

---

### 🪄 Smart solve and guide mode

For 3×3 solving workflows, ApexCube integrates a Kociemba-based solving pipeline.

- Smart solve trigger
- Formula sequence generation
- Step-by-step visual guide
- Highlighted move progression
- Progress feedback

> Advanced solving for larger cubes is a future extension target.

---

### 🌌 Premium visual system

The project is designed with a cyber-cosmic visual language.

- Glassmorphism control panels
- Neon accent lighting
- Cosmic grid background
- Floating cube aura
- Particle burst effects
- High-contrast sticker palette
- Smooth camera orbiting
- Responsive side panel layout

It is built to look like a product, not just a demo.

---

## 🛠️ Quick Start

### Option 1 — Open directly

Clone the repository and open `index.html` in your browser.

```bash
git clone https://github.com/muskke/apexcube-cosmic-lab.git
cd apexcube-cosmic-lab
open index.html
```

On Windows, double-click `index.html` or open it with your browser manually.

---

### Option 2 — Run with a local static server

Recommended when testing CDN scripts, browser policies, or deployment behavior.

```bash
python3 -m http.server 5173
```

Then visit:

```txt
http://localhost:5173
```

---

## 📦 Tech Stack

| Layer | Technology |
| --- | --- |
| Rendering | Three.js / WebGL |
| Interaction | Pointer Events + Raycasting |
| Cube Model | Cubie-based physical state |
| Animation | requestAnimationFrame |
| Solver | Kociemba algorithm |
| UI | HTML / CSS / Vanilla JavaScript |
| Persistence | localStorage |

No build step.  
No framework lock-in.  
Just open, run, and play.

---

## 🎮 Controls

### Mouse / Touch

| Action | Behavior |
| --- | --- |
| Drag empty space | Rotate camera view |
| Drag a sticker | Turn the corresponding cube layer |
| Scroll wheel | Zoom in / out |
| Touch drag | Mobile-friendly cube interaction |

### Keyboard

| Input | Move |
| --- | --- |
| `U D L R F B` | Outer-layer moves |
| `Shift + U/D/L/R/F/B` | Inverse outer-layer moves |
| `Alt + U/D/L/R/F/B` | Inner-layer moves |
| `Ctrl + U/D/L/R/F/B` | Wide moves |
| `Ctrl + Alt + U/D/L/R/F/B` | 3-layer wide moves on 5×5 |
| `M E S` | Middle-layer moves |
| `X Y Z` | Whole-cube rotations |
| `Space` | Timer hold/start/stop |
| `Esc` | Cancel timer |

---

## 🧩 Supported Notation

ApexCube understands common cube notation, including:

```txt
U D L R F B
U' D' L' R' F' B'
U2 D2 L2 R2 F2 B2
u d l r f b
Uw Dw Lw Rw Fw Bw
Uw3 Dw3 Lw3 Rw3 Fw3 Bw3
M E S
X Y Z
```

The parser is designed to support both normal practice input and high-order cube operations.

---

## 🏗️ Architecture

ApexCube is organized around several core modules:

```txt
index.html
├── Scene initialization
├── Cube construction
│   ├── Cubie generation
│   ├── Sticker generation
│   └── Physical grid state
├── Move parser
│   ├── Standard moves
│   ├── Inner moves
│   ├── Wide moves
│   ├── Middle moves
│   └── Whole-cube rotations
├── Move queue
│   ├── Buffered execution
│   ├── Animation speed control
│   └── Post-move state updates
├── Pointer interaction
│   ├── Raycasting
│   ├── Sticker picking
│   ├── Local drag resolution
│   └── Layer mapping
├── Timer system
├── Smart solve guide
└── UI dashboard
```

### Design principle

The core philosophy is:

> **Visual polish should not come at the cost of physical consistency.**

Every visible turn is resolved through a real cube-layer model, rather than being treated as a cosmetic animation only.

---

## 🧪 Browser Support

Recommended browsers:

- Chrome latest
- Edge latest
- Safari latest
- Firefox latest

For best performance, use a browser with stable WebGL acceleration enabled.

---

## 📁 Suggested Repository Structure

```txt
apexcube-cosmic-lab/
├── index.html
├── README.md
├── LICENSE
└── assets/
    ├── preview.png
    └── demo.gif
```

---

## 🧭 Roadmap

Planned or potential future improvements:

- [ ] Full NxN support beyond 5×5
- [ ] Configurable color scheme
- [ ] Mobile gesture refinement
- [ ] Import / export scramble state
- [ ] Shareable solve replay links
- [ ] Replay timeline
- [ ] Sound effects and haptic feedback
- [ ] Offline-first PWA mode
- [ ] Advanced solver support for 4×4 / 5×5
- [ ] Training modes for OLL / PLL / parity cases

---

## 🤝 Contributing

Contributions are welcome.

You can help by:

- Improving cube interaction accuracy
- Optimizing rendering performance
- Adding new notation support
- Refining mobile controls
- Improving the solving guide
- Designing better visual assets
- Reporting bugs with reproducible steps

Before submitting a pull request, please keep the project style consistent: polished visuals, clean interactions, and no unnecessary build complexity.

---

## 📄 License

This project is licensed under the **GNU General Public License v3.0 (GPL-3.0)**.

You are free to use, modify, and distribute this project under the terms of the GPL-3.0 license.

---

## 🌟 Acknowledgements

Built with:

- [Three.js](https://threejs.org/)
- Kociemba two-phase solving algorithm
- The speedcubing community
- Everyone who believes a web demo can still feel premium

---

<div align="center">

### If you like this project, consider giving it a ⭐.

**ApexCube Cosmic Lab**  
_Where algorithms, interaction, and cosmic aesthetics meet._

</div>
