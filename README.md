<div align="center">
  <img src="https://raw.githubusercontent.com/kvik0802/particle-manipulator/main/media/how-does-it-work.mp4" alt="Particle Manipulator Demo" width="100%"/>

  # ✦ Particle Manipulator ✦

  **An interactive 3D particle morphing engine** — 150,000 WebGL particles that seamlessly transform between shapes, text, and cosmic formations in real time.

  [![Live Demo](https://img.shields.io/badge/LIVE_DEMO-Render-46E3B7?style=for-the-badge&logo=render&logoColor=white)](https://work-flow-0ltc.onrender.com/)
  [![Made with Three.js](https://img.shields.io/badge/Made%20with-Three.js-000000?style=for-the-badge&logo=three.js&logoColor=white)](https://threejs.org/)
  [![Flask](https://img.shields.io/badge/Backend-Flask-000000?style=for-the-badge&logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

  <br/>
</div>

---

## Overview

Particle Manipulator is a high-performance creative coding project that brings **150,000 particles** to life. Each particle is individually animated via custom GLSL shaders, enabling butter-smooth morphing between 8 distinct 3D shapes — or any text you type. The experience is enriched with cinematic bloom, motion trails, a procedurally twinkling starfield, and mouse-reactive physics.

---

## ✨ Features

| | Feature | Details |
|---|---|---|
| 🚀 | **High-Density Engine** | 150K particles rendered in a single draw call via `THREE.Points` |
| 🔄 | **Dynamic Morphing** | Smooth transitions between Heart, Cube, Star, Sphere, Flower, Galaxy, Cone, Ring — or any custom text |
| ✏️ | **Text-to-Particles** | Renders typed words by sampling a hidden canvas and mapping pixels to 3D coordinates |
| 🌟 | **Cinematic Post-Processing** | UnrealBloomPass (nebula glow), AfterimagePass (motion trails), Reinhard tone mapping |
| 🖱️ | **Interactive Physics** | Mouse-driven attraction/repulsion + click-to-burst effect |
| 🎨 | **Shape-Aware Colors** | Each shape has a unique palette; text renders in pure white |
| ⚡ | **Auto-Optimization** | LOD system reduces pixel ratio & disables trails when FPS drops |
| 🎛️ | **Real-Time GUI** | `lil-gui` panel to tweak bloom, particle size, physics, exposure, rotation & colors |
| 🌌 | **Procedural Starfield** | 8,000 twinkling background stars with custom GLSL vertex shader |
| 🪟 | **Glassmorphic UI** | Sleek transparent controls with backdrop blur |

---

## Tech Stack

```
Frontend          Three.js 0.164 · GLSL · lil-gui · CSS3 · ES6
Backend           Python 3 · Flask · Gunicorn
Deployment        Render (Web Service)
```

---

## Getting Started

```bash
# Clone the repository
git clone https://github.com/kvik0802/particle-manipulator.git
cd particle-manipulator

# Install Python dependencies
cd backend
pip install -r requirements.txt

# Start the app (opens browser automatically)
cd ..
npm start
```

Then open **[http://localhost:5001](http://localhost:5001)** in your browser.

---

## Controls

| Action | Control |
|---|---|
| **Morph to shape** | Click shape buttons in the top bar |
| **Morph to text** | Type a word & press `Enter` or click "Morph" |
| **Rotate view** | Left-click + drag |
| **Zoom** | Scroll wheel |
| **Pan** | Right-click + drag |
| **Tune visuals** | `lil-gui` panel (top-right corner) |

---

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/api/metadata` | Project version & author info |
| `GET` | `/api/shapes` | List of supported shapes |
| `GET` | `/api/settings` | Current particle system settings |
| `POST` | `/api/settings` | Update particle system settings |

---

## Project Structure

```
particle-manipulator/
├── backend/
│   ├── server.py              # Flask server
│   └── requirements.txt       # Python deps (flask, gunicorn)
├── frontend/
│   └── index.html             # WebGL app (all-in-one: HTML, CSS, JS, GLSL)
├── media/                     # Demo videos
├── .gitignore
├── LICENSE
├── package.json
└── README.md
```

---

## Deployment

This project is ready to deploy on **Render**:

- **Build Command:** `pip install -r backend/requirements.txt`
- **Start Command:** `gunicorn --chdir backend server:app`

---

<div align="center">
  <sub>Built with ❤️ by <a href="https://github.com/kvik0802">Naini Vivekanand</a></sub>
  <br/>
  <sub>Three.js · GLSL · Flask · Creative Coding</sub>
</div>
