# 🌐 Holographic Gesture Globe V3

An immersive, contactless 3D planet navigation system that translates physical hand gestures captured via a standard webcam into real-time map manipulation commands. Built entirely using web-native technologies, this project eliminates heavy desktop software dependencies to deliver high-performance Human-Computer Interaction (HCI) directly inside any modern web browser.

---

## 🚀 Key Interaction Features

* **✊ Grab & Spin:** Pinch your thumb and index finger together into a closed fist to grab the map canvas. Drag your hand in any direction to rotate the globe along its X and Y axes.
* **👋 Velocity Momentum:** Releasing a spin gesture with a quick flick calculates hand velocity vectors. The globe maintains smooth inertia and naturally glides to a stop using a built-in friction engine.
* **👐 Multi-Hand Proximity Zoom:** Raise both hands and adjust the distance between your wrists. Spreading them wide pulls the camera vector forward (Zoom In), while bringing them together pushes it back (Zoom Out).
* **✌️ Hyper-Speed Spin:** Flash a two-finger peace sign and swipe side-to-side to instantly boost default rotational velocity by **500% (5x speed)** for rapid continental traversal.
* **👉 Target Laser Inspector:** Extend *only* your index finger to cast a real-time vector raycast line from your finger onto the sphere. The system places a pulsing structural tracker node at the exact coordinate intersection.
* **🛑 Freeze Frame Lock:** Face a flat palm with all fingers extended toward the lens to pause the rendering update loop and lock the globe static.
* **👌 Infrared Tactical Layer:** Touch your thumb tip to your pinky finger tip to swap visual render textures from standard neon cyan to a tactical deep red infrared heat mapping environment.

---

## 🛠️ Tech Stack & Architecture

* **Frontend Rendering Engine:** Three.js (WebGL) handling real-time 3D vertices, atmospheric fog pipelines, and a 2,500-node vector particle swarm.
* **Computer Vision Pipeline:** MediaPipe Hands running localized multi-hand landmark calculations down to 21 distinct joint coordinates.
* **Performance Matrix Optimization:** Scaled machine learning processing hooks (`modelComplexity: 0`) down to a performance-lite network tier, eliminating video buffering latency and keeping frame execution fluid at 30+ FPS.

---

## 📂 System File Structure

```text
├── index.html        # Monolithic entry point containing HTML5 DOM, CSS HUD, and system logic
└── README.md         # Documentation and project manual
```

---

## 💻 Local Sandbox Setup Instructions

Because web browsers enforce strict security sandboxes for hardware webcam calls, this file **must** be executed inside a local secure hosting environment (`localhost`).

### 1. Initialize Your Terminal
Open your terminal or command prompt inside your project repository folder.

### 2. Boot Your Local Web Server
Spin up a lightweight development server environment using native Python:
```bash
python -m http.server 8000
```
*(If your system configuration requires Python 3, run `python3 -m http.server 8000` instead).*

### 3. Initialize the Core Engine
Open your web browser window and navigate directly to your local sandbox address:
```text
http://localhost:8000
```
*Accept the browser prompt requesting permission to read your webcam feed, step back 1-2 feet, and begin testing interaction mechanics.*

---

## 🧠 Architectural Insights for Evaluators

### 3. Mathematical Coordinate Translations
* **Euclidean Proximity Matrices:** The project maps physical gestures by constantly monitoring coordinate distance ratios through standard 3D Euclidean distance math lines:
  $$\Delta d = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2 + (z_2 - z_1)^2}$$
* **Raycast Intersections:** The **Laser Point Inspector** reads normalized browser coordinates, projects an imaginary line vector from the virtual camera space down into the Three.js warehouse matrix, and solves intersection algorithms over the bounding sphere properties to position tracking elements.
