# AnalogLabs

> **CRT Video Player & Content Creation Tool for the Web**  

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML](https://img.shields.io/badge/HTML-5-orange.svg)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![WebGL](https://img.shields.io/badge/WebGL-2.0-blue.svg)](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API)

---


### Effect Tools
| Effect | Description |
|--------|-------------|
| **Scanlines** | Classic CRT horizontal scan lines |
| **VHS Noise** | Authentic tape distortion and static |
| **RGB Split** | Chromatic aberration effect |
| **Curvature** | Curved CRT screen simulation |
| **Bloom** | Soft glow and light bleeding |
| **Flicker** | Unstable analog signal simulation |
| **Glitch** | Digital/analog signal corruption |
| **Loop** | Seamless video looping |

### Hardware Skins
Choose from **Wood**, **Tech**, **Studio**, or **Minimal** monitor designs 

### Theme Toggle
 **dark** and **light** modes.


---

## ⌨️ Keyboard Shortcuts

| Key | Action |
|:---:|:---|
| `V` | Upload Video |
| `G` | Randomize Glitch |
| `L` | Toggle Loop |
| `F` | Toggle Fullscreen |
| `S` | Open Settings |
| `E` | Export Video |

---

##  How It Works

```
Video → WebGL Texture → Fragment Shader → Screen
```

### Audio Filter 
Web Audio API processes sound for nostalgic "warmth":
```
Video Audio → BiquadFilter (Low-pass @ 0.8 Rate) → Output
```
### Export
Captures WebGL canvas and processed audio in real-time:

Canvas + AudioDest → MediaRecorder →  WebM Export
```

---

## Project Structure

```
AnalogLabs/
├── index.html    # Single-file application (all HTML, CSS, JS)
└── README.md     # Documentation
```

---

## Data Flow

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│  Video Upload   │ ──▶ │  WebGL Render   │ ──▶ │  Effect Layer   │
└─────────────────┘     └─────────────────┘     └────────┬────────┘
                                                         │
┌─────────────────┐     ┌─────────────────┐              ▼
│ Settings Change │ ──▶ │ Uniform Update  │ ──▶  Re-render Frame
└─────────────────┘     └─────────────────┘              │
                                                         ▼
                                               ┌─────────────────┐
                                               │  Export Video   │
                                               └─────────────────┘
```


## References

- [WebGL API](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API) - Graphics rendering
- [Web Audio API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API) - Audio processing
- [MediaRecorder API](https://developer.mozilla.org/en-US/docs/Web/API/MediaRecorder) - Video export

---

## 📄 License

This project is licensed under the **MIT License** - feel free to use, modify, and share!

---

<p align="center">
  Made with ❤️ for the analog aesthetic
</p>
