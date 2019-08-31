## Quick Setup for Jackal Robot Simulation

### ROS version: Kinetic (Ubuntu 16.04)

#### Gazebo and Rviz without Laser Scanner

$ roslaunch jackal_gazebo jackal_world.launch  
$ roslaunch jackal_viz view_robot.launch  

#### Gazebo and Rviz with Laser Scanner
$ roslaunch jackal_gazebo jackal_world.launch config:=front_laser  
$ roslaunch jackal_viz view_robot.launch  

#### Navigation without Map
$ roslaunch jackal_gazebo jackal_world.launch config:=front_laser  
$ roslaunch jackal_drive_indoors odom_navigation_without_map.launch  
$ roslaunch jackal_viz view_robot.launch config:=navigation_without_map  

#### Navigation with Gmapping
$ roslaunch jackal_gazebo jackal_world.launch config:=front_laser  
$ roslaunch jackal_drive_indoors start_mapping.launch  
$ roslaunch jackal_viz view_robot.launch config:=gmapping  
$ roslaunch jackal_drive_indoors start_teleop.launch  
$ roscd jackal_drive_indoors/maps/  
$ rosrun map_server map_saver -f jackal_map  