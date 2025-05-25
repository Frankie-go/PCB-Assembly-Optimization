## 📌 Project: PCB Assembly Optimization

This project tackles a real-world case study inspired by Philips Electronics, focusing on optimizing the **placement of 102 components** on a printed circuit board (PCB) using **three robotic machines**, each equipped with three unique pick-and-place heads.

### 🔧 Problem Overview

* Each component must be picked from a designated feeder and placed at a specified location.
* Only certain heads (equipment) are compatible with specific component types.
* Each machine has a fixed set of tools and can only process batches of **up to 3 components**.
* Each batch follows the workflow: `HOME → Pick → Place → HOME`.

### 🎯 Objectives

* **Minimize total robot movement distance**.
* **Balance the workload** across all machines to maximize throughput.
* Respect all operational constraints: batch size, tool compatibility, machine-tool exclusivity, and complete task assignment.

### 🧠 Algorithms Implemented

* **Greedy Algorithm**: Builds the solution step-by-step by always choosing the locally optimal move. Fast but may lead to suboptimal global solutions.
* **Simulated Annealing**: A metaheuristic that explores the solution space probabilistically, allowing temporary acceptance of worse solutions to escape local optima. Provides significantly better performance in terms of cost and workload balance.

### 📊 Features

* Full implementation of task assignment, batch scheduling, and movement cost evaluation.
* Constraint handling for batch limits, equipment compatibility, and tool uniqueness.
* Export of detailed placement steps to CSV.
* **Visualizations**:

  * Bar chart showing number of placements per machine.
  * Grid-based layout showing component placement and machine responsibility.
  * Movement convergence curve for simulated annealing.

### 📁 Files

* `optimized_board_assembly_batch3_HOME.csv`: Step-by-step movement and placement log (SA).
* `greedy_board_assembly_result.csv`: Step-by-step movement log (Greedy).
* Python scripts: Complete implementation of both algorithms.
* `PCB_Assembly_Optimization_Presentation.pptx`: Summary of methods, results, and visualizations.

### ✅ Result Highlights

* Simulated Annealing achieved **lower total cost** and **better load balancing** than the Greedy algorithm.
* Visual output clearly shows reduced path overlap and improved throughput.


