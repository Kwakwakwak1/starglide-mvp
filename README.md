# StarGlideMVP

An XR browser-based flight simulator built with **Three.js** and designed for **Apple Vision Pro**. The app features minimal user controls and allows users to fly a low-poly ship through immersive environments using gaze and gesture-based navigation. The goal is to build a seamless, hands-free exploratory experience using real-time 3D rendering techniques. 

---

## 🧰 Tech Stack

- **Three.js** – for WebGL-based 3D rendering.
- **Apple Vision Pro (visionOS + Safari)** – for XR interface and hand/gaze interaction.
- **WebXR / WebXR-Polyfill** – for enabling immersive mode on supported browsers.
- **Hand Tracking API** (visionOS) – to detect gestures for UI interaction.

---

## 🚀 MVP Features

- Low-poly starship model in a 3D environment.
- Gaze-based orientation (look to steer).
- Pinch gesture to accelerate or maintain velocity.
- Multiple hand-based menus (appearing above hands on closed fist).
- Menu selection via look + close fist gesture.
- Immersive space-like or planet-based environment with minimal textures.
- Simple HUD with basic indicators (speed, direction).
- Future integration with Gaussian Splatting viewer.

---

## 🖐 Interaction Model

| Gesture        | Action                                     |
|----------------|--------------------------------------------|
| Gaze           | Ship orientation                           |
| Pinch + Hold   | Accelerate / maintain speed                |
| Closed Fist    | Open contextual menu above the hand        |
| Look + Close Fist | Select menu option                      |

---

## 🧪 Install & Run (Local Dev)

1. **Clone the repo**
   ```bash
   git clone https://github.com/yourusername/starglidemvp.git
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

4. **Open on Vision Pro Safari**
   - Host your dev server (use `ngrok` or local IP).
   - Visit the hosted URL using Safari in visionOS.
   - Make sure device permissions are enabled for motion, hand tracking, and immersive view.

---

## 📁 Project Structure

```
starglidemvp/
├── public/
│   └── models/              # 3D models (e.g. low-poly starship)
├── src/
│   ├── main.js              # Three.js scene setup and controls
│   ├── ui/
│   │   └── handMenus.js     # Hand menu generation + gesture logic
│   └── xr/
│       └── gazeControls.js  # Gaze and input handling
├── index.html
├── README.md
└── package.json
```

---

## 📌 Notes

- Environments and models are kept lightweight for optimal performance.
- Future updates may include: Gaussian Splat viewer, LiDAR-based environment capture, and terrain-aware flight.
- Gaussian Splatting integration will likely use PLY file loading, async chunk rendering, and proximity-based data loading.

