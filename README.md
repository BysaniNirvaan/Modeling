# 📚 Library Navigator (3D Interactive)

A fully interactive **3D library environment** built with **Three.js**, featuring:
- Smooth WASD movement system  
- Mouse-look controls  
- Jump, sprint, gravity  
- High-quality lighting & shadows  
- Real-time FPS & coordinate display  
- Automatic GLB model loading with fallback detection  
- Beautiful auto-material system for books, shelves, walls, floors & furniture  

This project loads a **3D library model (.glb)** and lets the user walk inside it like a small game.

---

## 🎮 Features
### 🏃 Player Movement  
| Key | Action |
|-----|--------|
| **W** | Move Forward |
| **A** | Move Left |
| **S** | Move Backward |
| **D** | Move Right |
| **SPACE** | Jump |
| **SHIFT** | Sprint |
| **Mouse Drag** | Look Around |

- Built-in gravity system  
- Smooth acceleration  
- FPS counter  
- Live position display  

---

## 🗂 Included Files
index.html ← Interactive library viewer (WASD controls) 68e0fce3-d6ae-4423-b9dc-67960a6…
library.glb ← 3D model of the library (uploaded)

yaml
Copy code

---

## 🚀 How to Run

### ✔️ Option 1: Open directly
Just double-click **index.html**  
(If the .glb is in the same folder, it will load.)

### ✔️ Option 2: Local server (recommended)
python3 -m http.server

yaml
Copy code

Then visit:
http://localhost:8000

yaml
Copy code

---

## 🧠 How It Works

### 🔹 Model Loading System
The script tries 10+ file paths:

library.glb
./library.glb
bhs_library.glb
../library.glb
../lib3/bhs_library.glb
...

markdown
Copy code

The moment it finds the correct path → It loads your `.glb` file successfully.

If all paths fail, it displays a **clean error message**.

### 🔹 Professional Lighting Setup
Used:
- Ambient light  
- 3 directional lights  
- 2 point lights  
- Fog  
- ACES Filmic tone mapping  
- Physically correct lights  

### 🔹 Smart Material Re-Color System  
The code detects mesh names:

- `book`, `spine` → realistic book colors  
- `shelf`, `bookcase` → natural wood  
- `wall` → neutral wall tones  
- `floor` → stone/wood floor colors  
- `table`, `desk`, `chair` → furniture wood  
- `door`, `glass` → transparent material  

Every object receives **MeshStandardMaterial** with:
- custom roughness  
- custom metalness  
- shadow support  

---

## ❗ Important: File Placement  
Place your files like this:

/project-folder
├── index.html
├── library.glb
└── README.md

yaml
Copy code

If the `.glb` is not in the same folder → it may not load.

---

## ⚙️ Requirements
- Any modern browser (Chrome / Edge / Firefox)
- WebGL support
- Internet (to load Three.js from CDN)

---

## 🧪 Browser Support
✔ Chrome  
✔ Edge  
✔ Firefox  
✔ Safari (with WebGL)  

---
