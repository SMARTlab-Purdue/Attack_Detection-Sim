# Attack_Detection-Sim
This repository contains the Matlab source code of attack detection algorithm for multi-agent / multi-robot system. Also, the ROS Gazebo simulation environments using multi-catvehicles are included. 

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

# Explanation of modification:
Few files were modified or created to demonstrate the Attack Detection simulation in urban environment 

1. A new map named Real_world_sim.world is made to create the urban street environment for simuation. 
2. catvehicle_multi.launch file is modified to load the world file Real_world_sim.world and multiple (currently set as 3) catvehicle model. 
3. URDF has been modified to set the desired orientation of catvehicle model in the map and to turn off the camera sensor displayed during simulation.
          
# Usage instructions
1. Download the catvehicle_multi.launch to catvehicle_ws/src/catvehicle/launch
2. Download the catvehicle.xacro  catvehicle_left_camera.gazebo  catvehicle_right_camera.gazebo to catvehicle_ws/src/catvehicle/urdf          
3. Download the Real_world_sim.world to catvehicle_ws/src/catvehicle/worlds
4. source the workspace using following command
            source catvehicle_ws/devel/setup.bash
5. launch the simulation environment for multi-vehicle attact detection simulation using following command
            roslaunch catvehicle catvehicle_multi.launch
6. Open Matlab and execute the file (matlab_file_name). If Matlab and ROS are operated at seperate laptop/PC, you must connect Matlab and ROS master first. Instruction on connecting matlab to ROS master can be found at https://www.mathworks.com/help/robotics/examples/connect-to-a-ros-network.html

# Video demonstration

# Contact

# Authors
