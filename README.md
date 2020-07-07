# ROS-TurtleBot3-Simulation
we will launch a virtual robot called TurtleBot3. TurtleBot3 is a low-cost, personal robot kit with open-source software.

i lanuch this simulation on Ubuntu 20.04 and ROS Noetic, Follow the instruction to run the simulation
# install the TurtleBot3 simulator
Open a terminal window and install the dependent packages. Enter the following commands:

    * cd ~/catkin_ws/src/

    * git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git

    * git clone https://github.com/ROBOTIS-GIT/turtlebot3.git

    * cd ~/catkin_ws and type catkin_make
    
TurtleBot3 has three models, Burger, Waffle, and Waffle Pi, you need to specify which model you want to use, to declare the model 

    * gedit ~/.bashrc
    
Add this line at the bottom of the file:

    * export TURTLEBOT3_MODEL=burger  (save and close)
    
    * source ~/.bashrc
    
# to download the TurtleBot3 simulation files.

    * cd ~/catkin_ws/src/

    * git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git

    * cd ~/catkin_ws && catkin_make
    
# start simulating TurtleBot3 and move the robot using Keyboard
There are many different environments to simulate the robot in such as empty environment, a house, environment for SLAM testing
i will use the house environment, type:

    * roslaunch turtlebot3_gazebo turtlebot3_house.launch
    
![turtlebot3_house](https://user-images.githubusercontent.com/67188835/86818016-835caf80-c08e-11ea-904a-2c7de93bffb5.png)
  
To move the TurtleBot with your keyboard,open a new terminal and type(make sure it is active while pressing the keys):

    * roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
Control with W A S D X

![ezgif-5-d5138aca1a5f](https://user-images.githubusercontent.com/67188835/86820738-1e0abd80-c092-11ea-97c1-feff283b2b92.gif)

 # run a simulation file : Autonomous Navigation and Obstacle Avoidance
 The goal is to have TurtleBot3 autonomously navigate around a room and avoid colliding into objects.
 Open a new terminal and type, to open SLAM environment:
 
    * roslaunch turtlebot3_gazebo turtlebot3_world.launch
    
 In another terminal window type:

    * roslaunch turtlebot3_gazebo turtlebot3_simulation.launch
You should see TurtleBot3 autonomously moving about the world and avoiding obstacles along the way.
    

    
