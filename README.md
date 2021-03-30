# robot_chase
A robot "the chaser" chases another robot "the runner" and tries to catch it.

## Overview
This project comprises of a C based physics simulator to emulate robot movement and collision resolution, path planning using a recursive tree search, and a graphics generator to display the environment. The aim of the program is for a chaser robot to catch the runner robot which performs a random walk in the map environment.

1. **Collision Detection**: Detects if two polygons interset each other based on the cross-product between pairs of points on two different lines of the polygons.

2. **Path Planning**: For the chaser robot to intelligently decide on its next action in order to catch the chaser robot,  it will search its actions over a horizon , 4 time steps into the future. The trajectory of the chaser robot is forward simulated for different possible actions it could take. Then at the end of the simulated trajectory, a score os computed to represent how good of a place the chaser is in relative to the runner. The action with the best score is taken for the next time step.

3. **Graphics**: Implemented code to draw lines, figures, and fill figures.

## Run the code 
```
./chase
usage: ./chase <time steps> <fast=0|1|2> <initial runner index>
```
fast mode: 
  0: Calls image server to update the image on browser at every time step
  1: Calls image server to update the image once chaser is caught
  2: Does not call the image server at all
  
initial runner idx: map idx where the runner is placed in the beginning


## Results
No matter where in the map the chaser begins, it catches the runner in less than 400 time steps.
<p align="left">
<img src="https://github.com/shreshthabasu/robot_chase/blob/master/img.png", width="720">
</p>


