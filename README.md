# GestureKart — Civic Driving Simulator 🚗

**Drive Smart. Stay Safe.** GestureKart is a browser-based 3D civic-driving game that encourages safer road behaviour through traffic awareness, traffic lights, and gesture or keyboard controls.

> **Project status:** Hackathon prototype. The preview images below are illustrative concept visuals, not screenshots captured from the running application.

## Visual Preview

### Driving through traffic
![GestureKart gameplay concept](assets/gesturekart-gameplay.png)

### Collision and game-over concept
![GestureKart game-over concept](assets/gesturekart-game-over.png)

## Features

- **3D driving scene** built with Three.js and React Three Fiber.
- **Gesture controls** powered by MediaPipe Pose Landmarker: lean your torso left or right to steer, and raise your right hand to brake.
- **Keyboard controls** for driving without a webcam.
- **Moving traffic** and collision detection that ends the current run.
- **Roadside traffic signals**, zebra crossings, and penalties for running a red light.
- **Civic driving score** and session statistics, including distance, duration, clean lane changes, and violations.
- **PDF scorecard export** to review a run.
- **Pause/resume and end-game controls** using `Esc` and the in-game menu.
- Sound toggle and responsive dashboard UI.

## Tech Stack

- React 18
- Vite
- Three.js
- React Three Fiber and Drei
- MediaPipe Tasks Vision (pose tracking)
- jsPDF
- Lucide React icons

## Getting Started

### Requirements

- Node.js 18 or newer
- npm
- A modern browser
- Webcam access for gesture controls (optional; keyboard controls are available)

### Install and run locally

```bash
git clone https://github.com/YOUR-USERNAME/gesturekart.git
cd gesturekart
npm install
npm run dev
```

Open the local URL printed by Vite (usually `http://localhost:5173`). If you want to use gesture controls, click **Enable Camera** and allow browser camera permission. Camera access is supported on `localhost` and deployed HTTPS sites. The first camera startup may download MediaPipe model/WASM files, so an internet connection is required.

### Create a production build

```bash
npm run build
npm run preview
```

Vite writes the production files to `dist/`.

## Controls

| Input | Action |
| --- | --- |
| `←` / `A` | Steer left |
| `→` / `D` | Steer right |
| `↑` / `W` | Move forward |
| `↓` / `S` | Move backward |
| `Space` | Brake / resume driving |
| `Esc` | Open the pause menu; resume or end the run there |
| Torso lean left/right (camera) | Change lanes |
| Raise right hand above your head (camera) | Brake / stop |

For gesture tracking, keep your shoulders and hips visible in the webcam frame and use small, deliberate movements.

## GitHub Upload

1. Create a new repository on GitHub named `gesturekart`.
2. Extract the project ZIP, then open a terminal in the `gesturekart` folder.
3. Initialise Git and commit the project:

   ```bash
   git init
   git add .
   git commit -m "Initial GestureKart project"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/gesturekart.git
   git push -u origin main
   ```

4. Replace `YOUR-USERNAME` with your GitHub username. If GitHub asks you to authenticate, complete its sign-in flow.

## Deploy with Vercel

1. Push the project to GitHub.
2. Import the repository into Vercel.
3. Select **Vite** as the framework preset.
4. Set the build command to `npm run build` and output directory to `dist`.
5. Deploy, then test camera permission on the HTTPS deployment URL.

## Project Structure

```text
gesturekart/
├── assets/
│   ├── gesturekart-gameplay.png
│   └── gesturekart-game-over.png
├── src/
│   ├── main.jsx
│   └── style.css
├── index.html
├── package.json
└── README.md
```

## Contributing

Suggestions and pull requests are welcome. You can help improve traffic behaviour, gesture sensitivity, accessibility, visual design, and civic-scoring rules.

## Disclaimer

GestureKart is an educational prototype, not a substitute for real-world driving instruction or official traffic-safety guidance. Always follow local traffic laws.
