# Mini XR Training Simulation
## Overview

This repository contains a mini project demonstrating data-driven XR/VR training for construction worker tasks. The project simulates joint angles, task time, and discomfort, then visualizes them in a simple WebXR/A-Frame environment.

The goal is to showcase how analytics can be integrated into XR-based feedback, enabling users to see real-time color-coded discomfort levels based on simulated data.

## Project Structure

MiniXRDemo/

├── worker_task_data.json   # Simulated task dataset with color mapping

├── mini_xr_training.py     # Python file for data simulation & analysis

├── index.html              # A-Frame VR environment

├── README.md               # This file


## Tools and Libraries Used

**Python & Analytics**:

- Python 3.x

- pandas, numpy

- matplotlib, seaborn, plotly

- scikit-learn (LinearRegression)

**XR/VR Visualization**:

- WebXR / A-Frame

- HTML, JavaScript

- JSON for feeding data to VR scene

**Development Tools**:

- VS Code (editor)

- Live Server extension (for local hosting)

### How It Works

**Data Simulation (Python)**:

- Joint angles, task time, and discomfort scores are generated for workers and tasks.

- A linear regression model predicts discomfort from the simulated angles and task times.

- Discomfort is mapped to color codes (green/yellow/red) for VR visualization.

- JSON file is exported (worker_task_data.json) to feed into the VR environment.

**VR Visualization (A-Frame)**:

- The index.html reads the JSON and displays a cube representing a worker’s task.

- Cube color updates every few seconds according to the discomfort score.

- Text panels show Worker ID, Task, and Discomfort.

### Viewing the VR Environment
**Option 1: Loca**l

- Clone this repository.

- Open VS Code and open the project folder.

- Open index.html.

- Start Live Server in VS Code. The browser will open and you will see the cube changing colors according to discomfort.

**Option 2: Recorded Demo**

For users who cannot run locally, a screen recording demonstrates the VR environment. Find the Google Drive Demo Link [Here](https://drive.google.com/file/d/1BNu9QZnDo2ZxmK8MYaGt51zZHLB8C37x/view?usp=sharing)


### Key Insights

- The model predicts mid-range discomfort accurately but underestimates extreme values (1 or 5).

- Color-coded VR cube provides quick visual feedback of task risk and discomfort.

- The workflow demonstrates end-to-end integration of Python analytics with XR visualization.

### How to Run
-**Clone repo**
git clone https://github.com/ModestaUZO/Mini-XR-Training-Simulation.git
cd MiniXRDemo

-**Open index.html in VS Code and run Live Server**

### Future Work

- Add more workers/tasks.

- Animate cube limbs based on joint angles.

- Host VR environment live online for full interaction.
