# Fireline — Wildfire Simulation

An interactive, browser-based wildfire simulation for a mathematical modelling hackathon.

## Quick start

1. Extract the `Fireline_Final.zip` archive.
2. Open `index.html` in Chrome, Edge, Firefox, or Safari.
3. Click **Start** to run the simulation, **Pause** to stop playback, or **Step** to advance one simulation turn.

No Python, packages, build tools, accounts, or server are required. The gameplay and graphics are contained in one HTML file. An internet connection is optional (used only to load a custom Google font; a fallback font works offline).

## Controls

- **Left-click and drag** on the map to paint with the selected tool. Brushes range from 1 to 5 cells.
- **1** Wood | **2** Dirt | **3** Stone | **4** Ignite | **5** Water | **6** Firebreak.
- **Space** Start/Pause | **N** Advance one turn | **R** Restart the same map.
- **New map** generates fresh terrain.
- **Ground style** switches between pixel textures and clean coloured tiles.
- **Conditions** lets you adjust wind speed (0–25 m/s), the direction the wind blows toward, environmental moisture, and playback speed.

## Terrain and water

- Terrain editing and firefighting tools have no costs, cooldown budgets, or placement limits.
- Select **Water** and paint to extinguish burning cells and increase local moisture. Each application increases moisture by 80% of the **remaining dryness**, not by 80 percentage points. Repeated strokes can increase moisture further.
- The water tool uses the supplied seven-frame pixel-art splash animation. The visible splash expands, while the gameplay effect is applied to the selected cell(s).
- Use **Custom blocks** to define a name, colour, and flammability for up to six additional materials. These definitions are kept in the browser's local storage where supported.

## Experiments

- The **Status** panel shows the number of turns, percentage of the map burned, and currently burning cells.
- **Run 30 trials** runs repeated stochastic simulations from the current map state without further manual actions, reporting the average, minimum, and maximum burned percentages. Results vary because ignition is probabilistic.
- The simulation automatically pauses when no burning cells remain. There is no defeat threshold or scoring objective.

## Notes for demonstration

This is a simplified educational simulation and **not** a validated wildfire forecast. The parameters are adjustable so that teams can study relative effects and discuss model assumptions. The mathematical equations are intentionally not displayed in the game's interface, allowing presenters to explain the model themselves.

## Project files

- `index.html` — complete HTML/CSS/JavaScript simulator, including embedded pixel-art textures and water-animation frames.
- `README.md` — these setup and usage notes.
