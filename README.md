## Quick Setup for Jackal Robot Simulation

### ROS version: Kinetic (Ubuntu 16.04)

#### Gazebo and Rviz without Laser Scanner

$ roslaunch jackal_gazebo jackal_world.launch  
$ roslaunch jackal_viz view_robot.launch  

#### Gazebo and Rviz with Laser Scanner
$ roslaunch jackal_gazebo jackal_world.launch   config:=front_laser  
$ roslaunch jackal_viz view_robot.launch  


