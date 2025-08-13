# Robot-Search-Simulation
### MATLAB simulation of an autonomous robot navigating a 4x4 grid to detect objects, calculate distances, and push the most isolated object out of bounds using reactive navigation and A* pathfinding.

## About the Project

This MATLAB simulation showcases an autonomous robot navigating an unknown 4x4 grid to locate hidden objects, map their positions, and push the most isolated one out of bounds. Using a reactive sense–plan–act navigation strategy combined with A* pathfinding, the robot explores and adapts to random object placements without a predefined map. The project demonstrates key concepts in autonomous navigation, sensor integration, occupancy grid mapping, and path planning. This is entirely a MATLAB simulation, no hardware is required.




#### Built With  

[![MATLAB](https://img.shields.io/badge/MATLAB-orange?logo=mathworks)](https://www.mathworks.com/products/matlab.html) – Main programming environment for simulation and algorithm development  

[![A* Pathfinding](https://img.shields.io/badge/A*-Pathfinding-blue)](https://en.wikipedia.org/wiki/A*_search_algorithm) – Path planning algorithm adapted for a 4x4 grid environment  


## Getting Started

### Prerequisites
 
You will need the following installed to build and run this project:  

- [MATLAB](https://www.mathworks.com/products/matlab.html) – Required to run the simulation and execute `.m` files  
- MATLAB toolboxes commonly included with the base installation (no additional specialized toolboxes required)  
- A computer capable of running MATLAB (Windows, macOS, or Linux)  


### Installation
  1. Clone the repository to your local machine (Replace "YourUsername" with your github username)
     ```sh
     git clone https://github.com/YourUsername/Autonomous_Robot_Grid_Simulation.git
     cd Autonomous_Robot_Grid_Simulation
     ```
  2. Open MATLAB
     
  3. Add the project folder to the MATLAB path by running the following commands in the command window:
     ```sh
     addpath(genpath(pwd))
     savepath
     ```
     
  4. Verify MATLAB can run .m files
     ```sh
     which Demo1
     ```
  5. Run the simulation in MATLAB command window using command:
     ```sh
     Demo1
     ```
## Usage

### Quick Summary
- ***Goal***: Simulate an autonomous robot navigating a 4x4 grid to find and remove the most isolated object.
- ***Approach***: Reactive navigation for exploration, A* pathfinding for targeted movement.
- ***Sensors***: Simulated left, front, and right obstacle detection.
- ***Key Features***: Object detection, grid mapping, Sum of Distances (SOD) calculation, and dynamic occupancy grid.
- ***Outcome***: Successfully completed all 10 test scenarios with varied object placements.

### Demo
![Robot Navigation Simulation Demo(1)](https://github.com/user-attachments/assets/dcff738e-cda8-4404-9219-45827e16635d)


### Reactive Navigation and Object Detection
- Navigates a 4x4 grid using sense-plan-act style loop
- Reads simulated left, front, and right sensors to detect objects and avoid obstacles.
- Uses a visit count matrix to prioritize unexplored tiles and prevent loops.
- Capable of locating all four hidden objects in varying configurations (can vary the configuration manually).

### A* Pathfinding and Object Removal
- Calculates Sum of Distances (SOD) for each detected object using Manhattan distance.
- Identifies the most isolated object (highest SOD) as the outlier.
- Uses an A* pathfinding algorithm with a dynamically updated occupancy grid to navigate back to the outlier.
- Pushes the object out of bounds while continuously verifying its movement.

### Technical Details
- Language & Tools: MATLAB
- Simulation Environment: 4x4 grid labeled 0–15, no predefined map
- Navigation: Reactive exploration algorithm + visit count tracking
- Path Planning: Custom integration of A* with linear-to-matrix position conversion
- Sensors: Simulated left, front, right object detection

### Simulation Results
- Completed 10 randomized test scenarios, each with different object placements.
- Successfully found and removed the most isolated object in all trials.
- Movement counts ranged from 16 in simple configurations to 85 in complex ones.
- Demonstrated strong adaptability to unseen environments, though efficiency decreased in high-complexity setups.

## Contributors
<a href="https://github.com/Garrison-Gralike/Autonomous-Robot-Line-Tracking/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=Garrison-Gralike/Autonomous-Robot-Line-Tracking" alt="contrib.rocks image" />
</a>

<a href="https://github.com/alpalacioc2">
  <img src="https://images.weserv.nl/?url=avatars.githubusercontent.com/u/172043853?v=4&w=100&h=100&fit=cover&mask=circle" width="65" alt="alpalacioc2"/>
</a>

## Contact
 [LinkedIn](https://www.linkedin.com/in/<garrison-gralike-56164b253>) – <ggralike1@gmail.com>
