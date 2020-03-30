# robot_chase
A robot "the chaser" chases another robot "the runner" and tries to catch it.

## Overview
A graphical interface is created to visualize the runner and chaser on a map. The runner performs a random walk whereas the chaser intelligently picks its action at every time step based on the runner's current position using a recursive tree search.
In every simulation, the runner can be placed on any valid point on the map as chosen by user. The simulation ends once the chaser cathces the runner.

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


