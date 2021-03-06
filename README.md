# RoboND_Project_Where_Am_I

The project discusses Localization using ROS package AMCL to formulate robot motion in a provided map of Gazebo and Rviz simulated environments.
**Note:** See the writeup for theoretical content on Localization and specifics of AMCL with Results.

## Project Content

Several aspects of mobile robot localization utilizing ROS packages are discussed, with focus on the following:

- Building a mobile robot for simulated tasks. The designed robot is a 3 platform robot to carry supplies in real world.

- Creating a ROS package that launches a custom robot model in a Gazebo world and utilizes packages like AMCL and the Navigation Stack.

- Exploring, adding, and tuning specific parameters corresponding to each package to achieve the best possible localization results.

## Installation Dependencies

Following are the installation procedure for specific ROS packages, required in order to complete the project:

``` bash
$ sudo apt-get install ros-kinetic-navigation
$ sudo apt-get install ros-kinetic-map-server
$ sudo apt-get install ros-kinetic-move-base
$ rospack profile
$ sudo apt-get install ros-kinetic-amcl
```

## Project Launch

The project can be launched by running the following commands:

```bash
$ cd ~/catkin_ws
$ catkin_make
$ source devel/setup.bash
$ roslaunch udacity_bot udacity_world.launch
```

And then running the following in *separate* terminals -

``` bash
$ cd ~/catkin_ws
$ source devel/setup.bash
$ rosrun udacity_bot navigation goal
```
**Note:** Change the folder name of catkin_ws in case of testing both the models(benchmark model and custom designed model) together. For e.g., 'Catkin_ws1'for custom designed robot. ```cd ~/catkin_ws1``` Rest all steps will remain same from above.

## Robot Configuration

The Robot Model designed for the project is named as ``Robo-Med Assist``. 

![robot_model](Results/Custom_Designed_Robot/Robot_Gazebo.png)

The Robot localization performance on reaching the Goal can be shown as:

![robot_Goal](Results/Custom_Designed_Robot/Robot_At_Goal_Position.png)

The Robot is designed with an intent of getting used in disaster prone areas where robots can replace humans in order to prevent costing more lives. Get going with the robot localizing itself in the map provided!!
