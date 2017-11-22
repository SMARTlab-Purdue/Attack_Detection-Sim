# Attack_Detection-Sim

This repository contains the Matlab source codes (to use in Robotarium platform) of various rendezvous controllers for consensus control in a multi-agent / multi-robot system. We also proposed a new weighted bearing controller using wireless network measurements such as the Received Signal Strength (RSS) and the Direction of Arrival (DOA) of the RSS. 

# Copyrights
All Copyright reserves to Jonathan Sprinkle, Sam Taylor, Alex Warren from Arizona Board of Regents 

# Installation instructions
1. Go to https://cps-vo.org/node/26602 
2. Install ROS Indigo following the ROS Wiki Page http://wiki.ros.org/indigo/Installation/Ubuntu
3. Install the additional following additional packages:
    a) Controller manager
          sudo apt-get install ros-indigo-controller-manager
          sudo apt-get install ros-indigo-ros-control ros-indigo-ros-controllers
          sudo apt-get install ros-indigo-gazebo-ros-control
    b) Velodyne
          sudo apt-get install ros-indigo-velodyne
    c) SICK Laser
          sudo apt-get install ros-indigo-sicktoolbox ros-indigo-sicktoolbox-wrapper
    d) Joystick control
          sudo apt-get install ros-indigo-joystick-drivers
    e) Localization packages
          sudo apt-get install ros-indigo-hector-slam ros-indigo-hector-mapping
4. Create Workspace:
          cd ~
          mkdir -p catvehicle_ws/src
          cd catvehicle_ws/src
          catkin_init_workspace

5. Download the packages
          cd ~/catvehicle_ws/src
          git clone https://github.com/sprinkjm/catvehicle.git
          git clone https://github.com/sprinkjm/obstaclestopper.git
          cd ../
          catkin_make

A video demonstration for installation is also provided and accesssed from the link http://cps-vo.org/node/26625 
          
# Usage instructions

1. 
          
# Explanation of modification:
Few files were modified or created to demonstrate the Attack Detection simulation in urban environment 

1. A new map named Real_world_sim.world is made to create the urban street environment for simuation. 

2. catvehicle_multi.launch file is modified to load the world file Real_world_sim.world and multiple (currently set as 3) catvehicle model. 

3. URDF has been modified to set the desired orientation of catvehicle model in the map and to turn off the camera sensor displayed during simulation.



# Video demonstration

# Contact

# Authors
