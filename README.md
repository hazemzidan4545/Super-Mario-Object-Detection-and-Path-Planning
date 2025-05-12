
---

#  Super Mario Game Planner using YOLOv8 & OpenCV

A Python-based project that uses **YOLOv8** for object detection and **path planning algorithms** to help Mario collect all coins and reach the castle on a 13×11 grid. The project simulates intelligent gameplay planning based solely on visual input.

---

##  Project Overview

This project takes an **input image** of a Mario game scene and performs the following:

1. **Detects** key objects using YOLOv8:

   * Mario
   * Coins
   * Enemies
   * Blocks
   * Castle (Goal)
2. **Maps** detected objects onto a fixed **13×11 grid**.
3. **Plans a sequence of actions** for Mario:

   * Collect all coins.
   * Reach the castle safely.
   * Avoid or attack enemies.
4. Outputs a **sequence of game actions** like:

   * `→` Move Right
   * `←` Move Left
   * `↑` Jump
   * `↓` Move Down
   * `A` Attack

---

##  Key Features

* **YOLOv8 Detection**: Uses Ultralytics YOLOv8 to identify all relevant game entities from a screenshot.
* **AI Path Planning**: Applies **Breadth-First Search (BFS)** to find optimal paths for coin collection and reaching the goal.
* **Grid Mapping**: Converts YOLO bounding boxes to grid coordinates for logic processing.
* **Action Sequence Generator**: Outputs clear and structured movement instructions.

---

##  Installation

### 1. Clone the repository:

```bash
git clone https://github.com/hazemzidan4545/Super-Mario-Object-Detection-and-Path-Planning.git
cd mario-game-planner
```


### 2. Download YOLOv8 weights:

* Place the YOLOv8 `.pt` model (e.g., `yolov8s.pt`) in the project root or model directory.

---


### Parameters:

* `--image`: Path to the Mario scene image.
* `--model`: Path to your YOLOv8 weights.

### Output:

* Terminal: Text-based action sequence (e.g., `→ → ↑ A → ↓ → →`).
* Optional: Grid visualizations or path overlays (if enabled).

---

##  Example

Given the following image:

![Test Image With All Cases](https://github.com/user-attachments/assets/ae67375d-8242-4bcf-8c04-1afbd85fd24e)


The output:
![Output](https://github.com/user-attachments/assets/a3d254f8-9811-4d18-a77b-8686856d5b63)
```
Victory Path: →↑↓→→A→↑→→↓→→→
Final Score: 10
```

---


##  Algorithms Used

* **YOLOv8**: Real-time object detection
* **Breadth-First Search (BFS)**: Pathfinding and coin collection strategy
* **Grid-based AI Planning**: Discrete logic for valid Mario moves
