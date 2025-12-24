# 🎄 Merry Christmas – Interactive Hand-Gesture Christmas Tree

An experimental Creative Technologist project combining Three.js, WebGL, and MediaPipe Hand Tracking to create an interactive, gesture-controlled Christmas tree experience in the browser.

Users can manipulate a 3D Christmas tree using hand gestures, upload personal photos as floating memories, and trigger different spatial modes using natural hand movements — no controllers required.

# ✨ Features

- 🎄 Procedural 3D Christmas Tree (spiral cone algorithm)

- ✋ Real-time hand gesture recognition (pinch, fist, open hand)

- 🖼 Upload personal images as framed memories

- 💾 Persistent photo storage using localStorage

- ✨ Cinematic lighting + bloom post-processing

- 🖥 Fully browser-based (no backend required)

# 🧠 Core Technologies Used
### 1. Three.js (WebGL Rendering)

WebGLRenderer with tone mapping (Reinhard)

Physically-based materials (MeshStandardMaterial, MeshPhysicalMaterial)

Procedural geometry (Boxes, Spheres, TubeGeometry)

Custom environment lighting using RoomEnvironment

Scene grouping & smooth interpolation (LERP)

### 2. Post-Processing

EffectComposer

UnrealBloomPass for luxury glow & highlights

### 3. MediaPipe Tasks Vision

@mediapipe/tasks-vision

HandLandmarker with GPU delegate

Real-time hand landmark detection (21 keypoints)

Gesture classification using spatial heuristics

### 4. Canvas & Texture Generation

Procedural Candy Cane texture via Canvas 2D API

Dynamic photo textures (uploaded images & generated greeting canvas)

### 5. State Machine Architecture
STATE.mode = 'TREE' | 'SCATTER' | 'FOCUS'


Smooth transitions via vector interpolation

Deterministic spatial behaviors per mode

### 6. Persistent Storage

Uploaded photos stored as Base64 in localStorage

Automatically restored on page reload

# 🎮 How to Control the Scene (Hand-by-Hand Guide)
🖐 Hand Position (Rotation Control)

Move your hand in front of the camera:

Move hand left / right → rotate tree horizontally

Move hand up / down → rotate tree vertically

This is mapped from the palm center landmark (index 9).

# ✊ Gesture Controls (Modes)
Gesture | Description | Effect
✊ Fist | Fingers close to wrist | 🎄 Tree Mode – particles form a Christmas tree
✋ Open | Hand	Fingers spread wide	| 💥 Scatter Mode – particles float & rotate freely
🤏 Pinch | 	Thumb + index close	| 🔍 Focus Mode – a memory photo zooms forward

# 🖼 Uploading Photos

Click “ADD MEMORIES”

Select an image from your device

The photo appears in a golden frame

The image is saved locally and restored on refresh

Photos are stored locally in your browser only — no server upload.

# ⌨ UI Controls

Press H → Hide / show UI overlay

🚀 How to Run Locally

Because this project uses ES Modules, it must be served via HTTP.

``
    Option 1: VS Code Live Server
    Right click → Open with Live Server
```

Then open: http://localhost:8000



