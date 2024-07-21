# ✨ *Turtlebot3* ✨

## *Part One: Installing the needed packages:* 

![Screenshot_1](https://github.com/user-attachments/assets/419c1cdb-6825-465b-8afe-d45c293f9b34)

![Screenshot_2](https://github.com/user-attachments/assets/14581197-3261-4ac0-93cb-bf3f883f55c3)

![Screenshot_3](https://github.com/user-attachments/assets/06783854-dccc-4224-a0c2-3c02eda30195)

![Screenshot_4](https://github.com/user-attachments/assets/fa7a8229-d30f-4eaf-8cca-2a5c6ce133e4)

![Screenshot_5](https://github.com/user-attachments/assets/db583fe8-7d67-4b52-a700-7200dfea0c57)

![Screenshot_6](https://github.com/user-attachments/assets/37ac44e9-a620-4dd8-9564-574f12f39774)

## *Part Two: Running Gazebo and controlling the robot with keyboard:*

### *Using the following commands:*

```
source ~/catkin_ws/devel/setup.bash

export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_gazebo turtlebot3_world.launch
```

![Screenshot_7](https://github.com/user-attachments/assets/2a4a1e1e-26c0-42ac-ad13-8f2c45d28af5)

### *To move the robot, we can use the teleop key files through the following commands in a new terminal:*

```
source ~/catkin_ws/devel/setup.bash

export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```

![Screenshot_8](https://github.com/user-attachments/assets/ebc1a537-ec64-4ebc-877b-e6277f953f08)

## *Part Three: Creating the map with SLAM:*

### *In a new terminal, write the following commands to run SLAM:* 

```
source ~/catkin_ws/devel/setup.bash

export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
```

![Screenshot_9](https://github.com/user-attachments/assets/c291cc9d-67df-44fc-ab33-cf570336333b)

### *After controlling the robot using the teleop, we complete the map creation*

![Screenshot_10](https://github.com/user-attachments/assets/1f87d143-7cc8-4ab1-ba5d-959a475d7137)

### *To save the created map, open a new terminal and write the following command:*

```
source ~/catkin_ws/devel/setup.bash

rosrun map_server map_saver -f ~/map
```

![Screenshot_11](https://github.com/user-attachments/assets/84cdfb71-992a-46da-a7e7-e13b5891580b)

## *Part Four: Navigating the saved map:*

Note: close all nodes and start gazebo again with the same step as before

### *In a new terminal, run the following command:*

```
export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
```

![Screenshot_12](https://github.com/user-attachments/assets/08fe861a-53b2-4e1e-aee1-da6a358cb464)

### *Now we click on the 2D pose estimate button to estimate the location of the robot:*

![Screenshot_13](https://github.com/user-attachments/assets/dbe255ea-3e15-4649-9730-e0d948c250e2)

### *Then we click on the 2D Nav Goal button to set a goat position that the robot can navigate to:*

![Screenshot_14](https://github.com/user-attachments/assets/b6706a79-dea3-4287-a71f-ed069b00057b)

### *The robot will start navigating to the goal:*

![Screenshot_15](https://github.com/user-attachments/assets/af1d4868-6935-488b-86eb-9c403d7a94d7)

![Screenshot_16](https://github.com/user-attachments/assets/178bf23f-5e09-4717-b08a-4c6168c56e66)

### *And we're done!* 🐻
