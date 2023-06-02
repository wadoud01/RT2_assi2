# Research Track 2 - Assignment 2

This repository contains the code and documentation for Research Track 2 - Assignment 2. The assignment focuses on the implementation of the node, which interacts with the user to set target positions and visualize the robot's movements.

## Description

The `action_usr.py` node allows the user to set target positions for the robot. The user is prompted to enter two integers to specify the x and y coordinates of the target position. Additionally, if the user enters 'c', the target position is canceled.

To facilitate the interaction with the node, two slide widgets have been created to set the x and y target positions. Two buttons have also been provided: the first button sends and sets the target positions based on the values selected using the sliders, while the second button cancels the target goal.

The robot's movement is visualized using a plot graph, which subscribes to the `/odom` topic. As the robot moves towards the target position, its movements are displayed on this graph in real-time.

The assignment also includes the creation of another graph to track the reached and canceled goals. Each time the robot successfully reaches a target position, the count is incremented and displayed on the graph. Similarly, when the goal is canceled, the canceled goal count increases. The total section of the graph provides the overall count of reached and canceled target positions.

## Installation

To run the assignment, follow the steps below to install the necessary dependencies:

1. Install Jupyter Notebook:
   ```shell
   pip3 install jupyter bqplot pyyaml ipywidgets
   
## How to Run
To run the assignment, follow these steps:

Open the Jupyter Notebook by executing the following command in the terminal:

shell
Copy code
jupyter notebook --allow-root --ip 0.0.0.0
Click on the assignment_2.ipynb notebook to open it.
In separate terminals, run the following commands to launch the required ROS nodes:
shell
Copy code
roscore
roslaunch assignment_2_2022 assignment_2.launch
Inside the Jupyter Notebook, use the provided widgets and buttons to set the target x and y positions. The "Plot" button allows you to visualize the number of reached and canceled targets.

