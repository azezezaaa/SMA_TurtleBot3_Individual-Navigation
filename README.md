# SMA_TurtleBot3_Individual-Navigation
This repo consists of a ROS package used to launch 3 TurtleBot3s in simulation and operate them independently of each other. This repo was used as lab practical in MIAR.

# Launch 3 turtlebots and operate them independently.
## (1) Install prerequisites:
```
$ cd ~/catkin_ws/src
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3.git
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3_applications.git
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3_applications_msgs.git
$ cd .. && catkin_make
$ source devel/setup.bash
$ cd src/ 
```
## (2) Download the package.
```
$ cd ~/catkin_ws/src
$ git clone https://github.com/azezezaaa/SMA_TurtleBot3_Individual-Navigation
```
## (3) Update the modified content: 
```
$ cd ~/catkin_ws && catkin_make && source devel/setup.bash
$ rospack profile
```
## (4) Launch turtlebots simulation:
```
$ roslaunch SMA_TurtleBot3_Individual-Navigation simulation.launch
```
## (5) Run Teleoperation:
Open another terminal and write: 
1. For robot1
```
ROS_NAMESPACE=robot1 rosrun teleop_twist_keyboard teleop_twist_keyboard.py /cmd_vel:=/robot1/cmd_vel
```
2. For robot2 
```
ROS_NAMESPACE=robot2 rosrun teleop_twist_keyboard teleop_twist_keyboard.py cmd_vel:=/robot2/cmd_vel
```
3. For robot3 
```
ROS_NAMESPACE=robot3 rosrun teleop_twist_keyboard teleop_twist_keyboard.py /cmd_vel:=/robot3/cmd_vel
```
