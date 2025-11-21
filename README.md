# Rohit Interactive Portfolio – WebGL Particle Simulation

This project is an advanced **Google-style Anti-Gravity Particle Simulation Hero Section** built using **Three.js**, **GPGPU shaders**, and **GLSL noise algorithms**.  
The particles smoothly react to mouse movement and create a high-end, interactive background for the portfolio hero section.

---

## Features

### Advanced Particle Physics (GPU Powered)
- 65,536+ particles using **GPGPU FBO Simulation**
- **3D Simplex Noise + Curl Noise** for natural fluid motion
- Real-time particle physics entirely on GPU

###  Mouse Interaction
- Particles repel and react to mouse position
- Smooth interpolation using lerp()
- World-space accurate interaction

### Clean Portfolio UI
- Modern hero section with gradient text
- Fully responsive layout
- Buttons and logo overlay on top of WebGL canvas

### High Performance
- HalfFloat textures for fast simulation
- Ping-pong render targets (double buffering)
- Animation loop optimized for smooth FPS

---

## Tech Stack

| Technology | Use |
|-----------|-----|
| **HTML / CSS** | Front-end layout + design |
| **JavaScript (ES Modules)** | Main logic + WebGL control |
| **Three.js** | Rendering engine for particles |
| **GLSL Shaders** | Physics simulation + rendering |
| **GPGPU (Framebuffer Objects)** | Compute physics on GPU |

---

## Project Structure

├── index.html # Main WebGL + UI code
├── README.md # Documentation file
└── assets/ # (Optional) images, logos, fonts


---

## How It Works

### 1. GPU Simulation (GPGPU)
Particles are stored inside textures:
- One texture stores **position**
- One texture stores **velocity**

Each frame:
- Velocity shader updates speed
- Position shader updates location
- Render shader draws particles

### 2. Noise-Based Flow Field
- Simplex noise generates a 3D turbulence flow  
- Curl noise makes motion smooth + fluid  
- Particles never collide, they swirl gracefully

### 3. Mouse Interaction
- Mouse position converted to world coordinates  
- Nearby particles receive repulsion force  
- Smooth easing applied for natural behavior  

### 4. Rendering
- 1 point = 1 particle  
- Custom fragment shader draws soft round glowing dots

---

## How to Run

### **Option 1: Open Directly**
Just open `index.html` in Chrome or Edge.

### **Option 2: Run Local Server (Recommended)**

#### VS Code Live Server:
1. Install Live Server extension  
2. Right-click `index.html` → **Open with Live Server**

#### Node.js:
```sh
npx serve .

Author

Rohit Kumar
Frontend Developer | Interactive UI Designer
Built using Three.js, GLSL.

