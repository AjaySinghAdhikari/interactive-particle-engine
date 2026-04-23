# ✋ NEXUS — Interactive Particle Engine X

A **Level 10** interactive 3D particle visualization controlled by **real-time hand tracking**.  
Built with a custom **GLSL shader pipeline**, **MediaPipe Hands**, and **Three.js WebGL rendering**.

---

## 🚀 Live Demo
👉 https://ajaysinghadhikari.github.io/interactive-particle-engine/

> ⚠️ Webcam permission is required for hand tracking. Works best in Chrome/Edge.

---

## ✨ What's New (v2.0)

| Feature | Before | Now |
|---|---|---|
| Particles | 15,000 | **25,000** |
| Renderer | PointsMaterial | **Custom GLSL Shader** |
| Shapes | 6 | **10** |
| Gestures | 2 | **4** |
| FX Controls | None | **5 toggleable effects** |
| UI | Basic overlay | **Full HUD + shape navigator** |
| Keyboard | None | **Full shortcuts** |

---

## 🔮 Particle Forms (10 Shapes)

| # | Shape | Description |
|---|---|---|
| 01 | Galaxy Spiral | 6-arm logarithmic spiral with scatter |
| 02 | Torus Knot | Intricate p=2, q=3 interlocking tube |
| 03 | Klein Bottle | Non-orientable 4D surface projected to 3D |
| 04 | Black Hole | Accretion disk + infall funnel |
| 05 | Sphere | Fibonacci distributed surface |
| 06 | Heart | Parametric 3D heart equation |
| 07 | DNA Helix | Dual-strand helix with twist |
| 08 | Möbius Strip | Single-sided infinite loop |
| 09 | Lorenz Attractor | Chaotic strange attractor |
| 10 | Cymatic Wave | Standing wave interference pattern |

---

## 🎮 Controls

### Hand Gestures
| Gesture | Action |
|---|---|
| ✋ Move Hand | Warp particles + dynamic color shift |
| 👏 Clap Both Hands | Morph to next shape |
| 👌 Pinch (thumb + index) | Reverse vortex → attraction pull |
| 🤙 Spread All Fingers | Trigger particle explosion |

### Keyboard Shortcuts
| Key | Action |
|---|---|
| `Space` / `→` | Next shape |
| `←` | Previous shape |
| `E` | Explosion |
| `G` | Toggle gravity well |
| `C` | Toggle color flow |
| `T` | Toggle trails |

### On-Screen FX Panel
Click the buttons at the top to toggle: **Trails · Vortex · Explode · Gravity · Color Flow**

---

## 🛠️ Tech Stack

- **Three.js r128** — WebGL 3D rendering
- **Custom GLSL Shaders** — per-particle glow core with radial falloff
- **MediaPipe Hands** — real-time 2-hand landmark detection
- **ACES Filmic Tone Mapping** — cinematic color grading
- **HTML5 / Vanilla JS (ES6+)**

---

## 📂 Project Structure

```
interactive-particle-engine/
├── index.html      # Full engine — single file, zero dependencies to install
└── README.md
```

---

## 🧠 How It Works

1. **MediaPipe** processes webcam frames and returns 21 3D landmarks per hand at ~30fps
2. Landmark positions are mapped to Three.js world coordinates
3. Each frame, 25,000 particles LERP toward their target shape positions
4. The custom vertex shader sizes each particle by depth (perspective point sizing)
5. The fragment shader draws a soft glowing disc with a bright core per particle
6. Hand position drives a curl/vortex force field applied per particle per frame

---

## 📸 Shapes Preview

> Galaxy → Torus Knot → Klein Bottle → Black Hole → Sphere → Heart → DNA → Möbius → Lorenz → Cymatic

Clap to cycle through all 10 forms with smooth morphing transitions.

---

## 🙌 Author

**Ajay Singh Adhikari**  
[GitHub](https://github.com/ajaysinghadhikari) · [Live Demo](https://ajaysinghadhikari.github.io/interactive-particle-engine/)