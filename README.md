[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/YH1KUuZ5)

This assignment involved designing and implementing a robot path planning algorithm using the Potential Field Method.

The potential field method simulates the robot as a particle in a field:
- The goal exerts an attractive force, pulling the robot toward it.
- Obstacles exert repulsive forces, pushing the robot away to avoid collisions.
- The robot follows the negative gradient of the combined potential, leading to a planned path that navigates from start to goal while avoiding obstacles.

Code Structure & Key Steps
1. Workspace Initialization
- Defined start point, goal point, and circular obstacles within a 2D grid.
2. Potential Function Construction
- U_att(q): Parabolic attractive potential guiding the robot to the goal.
- U_rep(q): Inverse-distance repulsive potential from obstacles, within influence radius.
- U_total(q): Sum of both potentials.
4. Force Calculation (Gradient of Potential)
- F_total(q): Combines attractive and repulsive gradients to compute direction of movement.
- Normalized gradient descent step used to update position iteratively.
5. Path Planning Loop
- The robot moves step by step under the influence of the combined force field until it either reaches the goal or is trapped in a local minimum.
6. Visualization
- The field and robot's path are visualized using contour plots with overlaid obstacles, start, goal, and planned path.