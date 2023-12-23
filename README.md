### Author
Nishant Awdeshkumar Pandey and Rishikesh Jadhav.

This folder consists of the following folders:

Package - Contains another folder named a robot that can be copy pasted in catkin_ws/src. 

robot folder contains multiple folders with the following description:

1. congif - contains .yaml files for controllers.

2. launch - contains .launch files to spawn the bot in Gazebo, RViz.

3. meshes - contains .dae files for various parts of the bot

4. scripts - contains various .py files to move the bot (publisher, subscriber nodes).

5. urdf - contains .xacro file of the bot

6. worlds - .world in which the bot is spawned in Gazebo

There are various scripts as follows:

1. teleop.py - control the movement of the bot using the teleop

2. fk_validation.py - for forward kinematics validation

3. ik_val.py - for inverse kinematics validation

4. diff_control.py - to control the differential drive of the robot and make it stop just before the goal using a closed-loop controller

5. go_home.py - to go back to home position of the bot i.e. origin after pick and place operation.

6. grasp.py - to grasp an object using the gripper

7. arm_control.py - to move the arm above the box and open the gripper. (will not work as the size of the object and friction between the gripper and the object are not right just pick and place operation was done manually in the video.).

8. End_eff_trajectory.py - to obtain the graph of end effector trajectory for Inverse kinematics validation.

To spawn the bot in Gazebo and RViz in the world design the following command works(with rqt_steering) after navigating to the launch folder in the terminal:

```roslaunch 04-diff_drive_robot_arm.launch```

To spawn the bot in RViz with a slider to control the various joints of the robot the following command works after navigating to the launch folder in terminal:

```roslaunch view_demo.launch```
 
To run these codes open in the terminal the scripts folder and run the python3 <name of the script to run> command along with roscore running in the background.

The following sequence of scripts should be run to obtain the pick and place of an object:

```roslaunch 04-diff_drive_robot_arm.launch --> python3 diff_control.py --> python3 arm_control.py --> python3 grasp.py --> go_home.py```

### Report 
[Report](https://github.com/nishantpandey4/Pick_place_mobile_robot/blob/main/Report%20.pdf)
 
### Videos of the Results:

Drive link for all the videos:
https://drive.google.com/drive/folders/1QW7Eak2PbWma0Tb0El4jjWCQnswvXPuF

https://github.com/nishantpandey4/Pick_place_mobile_robot/assets/127569735/30d01b9a-f4ea-4732-a608-fe4c0278345a



