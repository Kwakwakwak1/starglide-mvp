# StarGlide MVP

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

An **open-source** XR browser-based flight simulator built with **Three.js** and designed for **Apple Vision Pro** and other modern XR devices. The app features intuitive, hands-free controls that let users navigate a starship through immersive environments using gaze and gesture-based navigation. The goal is to create a seamless, accessible exploratory experience using real-time 3D rendering techniques.

[Live Demo](https://starglide.kwakwakwak.com) | [Documentation](https://github.com/Kwakwakwak1/starglide-mvp/wiki)

---

## 🧰 Tech Stack & Dependencies

- **Three.js (v0.157.0+)** – Core WebGL-based 3D rendering
- **WebXR API** – Native XR session management and device integration
- **WebXR Device API Polyfill** – Fallback for non-WebXR browsers
- **hand.js** – Hand tracking abstraction layer
- **Spatial Audio API** – 3D positional audio effects
- **TweenJS** – Animation interpolation
- **GLTFLoader** – 3D asset loading
- **Stats.js** – Performance monitoring (dev only)
- **Vite** – Modern build tooling and development server

### Supported Platforms
- **Apple Vision Pro (visionOS + Safari)** – Primary target platform
- **Meta Quest** (via Browser) – Secondary support
- **Desktop browsers** with WebXR support
- **Mobile AR** (iOS/Android) – Limited functionality 

---

## 🚀 Features

### Core Gameplay
- **Dynamic Flight Physics** – Realistic momentum, inertia, and velocity controls
- **Procedural Terrain Generation** – Endless, varied environments to explore
- **Multiple Starship Models** – Different handling characteristics and abilities
- **Objective-based Missions** – Optional gameplay goals like navigation challenges
- **Free Exploration Mode** – No objectives, pure discovery

### XR Interaction
- **Gaze-based Steering** – Look to change orientation
- **Gesture Control System** – Intuitive hand commands for flight
- **Spatial UI** – Context-aware interfaces that appear in 3D space
- **Voice Command Support** – Optional voice navigation (where supported)
- **Adaptive Difficulty** – Adjusts based on player skill and comfort

### Technical Features
- **Optimized Asset Loading** – Progressive loading for smooth experience
- **Level of Detail (LOD)** – Dynamic model complexity based on distance
- **Post-processing Effects** – Customizable visual filters
- **60+ FPS Target** – Performance-focused rendering
- **Offline Support** – Core game playable without internet connection
- **Persistence** – Save flight progress and settings

---

## 🖐 Interaction Model

| Gesture/Input          | Action                                          |
|------------------------|--------------------------------------------------|
| Gaze                   | Ship orientation and UI targeting                |
| Pinch + Hold           | Accelerate / maintain speed                      |
| Closed Fist            | Open contextual menu above the hand              |
| Look + Close Fist      | Select menu option                               |
| Spread Fingers         | Brake / slow down                                |
| Two-Handed Pinch + Pull | Zoom view / change perspective                   |
| Double Tap             | Toggle cockpit view / external view              |
| Voice Command "Menu"   | Open main settings menu                          |
| Voice Command "Boost"  | Temporary speed increase                         |

---

## 💻 Installation & Development

### Prerequisites
- Node.js (v18+)
- npm or yarn
- A WebXR-compatible browser for testing

### Local Development Setup

1. **Clone the repo**
   ```bash
   git clone https://github.com/Kwakwakwak1/starglide-mvp.git
   cd starglidemvp
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start development server**
   ```bash
   npm run dev
   ```

4. **Testing on devices**
   - **Vision Pro:** Host your dev server (using `ngrok http 5173` or local network IP)
   - **Desktop:** Visit `http://localhost:5173` in a WebXR-compatible browser
   - **Mobile/Quest:** Use secure HTTPS connection (required for WebXR)

### Building for Production
```bash
npm run build
```

---

## 📁 Project Structure

```
starglidemvp/
├── public/
│   ├── models/              # 3D models (.glb/.gltf)
│   ├── textures/            # Environment and ship textures
│   ├── audio/               # Sound effects and ambient audio
│   └── shaders/             # GLSL shader files
├── src/
│   ├── main.js              # Application entry point
│   ├── core/
│   │   ├── scene.js         # Three.js scene setup
│   │   ├── renderer.js      # WebGL renderer configuration
│   │   ├── physics.js       # Flight dynamics and collision
│   │   └── assets.js        # Asset management and loading
│   ├── entities/
│   │   ├── ship.js          # Player ship models and behavior
│   │   └── environment.js   # World generation and environment
│   ├── ui/
│   │   ├── hud.js           # Heads-up display
│   │   ├── menus.js         # Menu system
│   │   └── handMenus.js     # Hand-based contextual menus
│   ├── input/
│   │   ├── gazeControls.js  # Gaze tracking and control
│   │   ├── gestureInput.js  # Hand gesture detection
│   │   └── voiceCommands.js # Voice input processing
│   └── utils/
│       ├── math.js          # Math helpers
│       ├── debug.js         # Debug/performance tools
│       └── compatibility.js # Browser/device feature detection
├── tests/                   # Unit and integration tests
├── .github/                 # GitHub Actions workflows
├── index.html
├── vite.config.js
├── LICENSE
├── README.md
└── package.json
```

---

## 🤝 Contributing

We welcome contributions from the community! Please check out our [Contributing Guidelines](CONTRIBUTING.md) for details on how to submit issues, feature requests, and pull requests.

### Getting Started
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Code of Conduct
This project adheres to a [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

---

## 📈 Performance Guidelines

- Models should be under 20k triangles for optimal performance
- Textures should be compressed and power-of-two dimensions
- Avoid excessive dynamic lights (max 3 recommended)
- Target 72 FPS minimum on Vision Pro
- Prioritize hand tracking responsiveness

---

## 📋 Roadmap

- **v0.1** – Core flight controls and basic environment
- **v0.2** – Hand menu system and improved physics
- **v0.3** – Procedural terrain and mission system
- **v0.4** – Multi-device support and performance optimization
- **v0.5** – Voice commands and additional ships
- **v1.0** – Full featured release with all core systems

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Three.js community for their excellent documentation and examples
- Apple's visionOS development team for their XR input guidance
- The WebXR working group for their standards development
- All open source contributors who help make projects like this possible

---


