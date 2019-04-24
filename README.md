# Udacity Robotics Software Engineering Nanodegree Program Project 2
# Go-Chase-It

## Introduction
This project includes designing a robot, housing it inside the world you created, and programming it to chase white-colored balls.

## Getting Started

http://gazebosim.org/

http://wiki.ros.org/ROS/Installation

To study with this project, you must install Gazebo and ROS environment on your Linux OS. With this project, you will learn creating a Gazebo model and world-building, Gazebo plugins, URDF files, ROS publishers, subscribers, clients and services.


If you have installed Gazebo and ROS environment on your Linux OS, you can follow the steps below to build and run this study.

Create and initialize ```catkin_ws```

```bash
$ mkdir -p /home/src/catkin_ws/src 
$ cd /home/src/catkin_ws/src
$ catkin_init_workspace
```
Clone or download the repository

```bash
$ git clone https://github.com/apocardi/Go-Chase-It.git
$ cp -R Go-Chase-It/ball_chaser
$ cp -R Go-Chase-It/my_robot
$ rm -rf Go-Chase-It
```

Next, build the project

```bash
$ cd ..
$ catkin_make
```
Open three terminal

In the first teminal, launch ```world.launch```file

```bash
$ cd /home/src/catkin_ws/
$ source devel/setup.bash
$ roslaunch my_robot world.launch
```
In the second one, visualize the robot’s camera images

```bash
$ cd /home/src/catkin_ws/
$ source devel/setup.bash
$ rosrun rqt_image_view rqt_image_view 
```

In the last one, execute ``ball_chaser.launch```
$ cd /home/src/catkin_ws/
$ source devel/setup.bash
$ roslaunch ball_chaser ball_chaser.launch
