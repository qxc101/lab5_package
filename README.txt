Qi Cheng
qxc101

This is a package for EECS 373 Lab #4. 
The file urdf/robot.xacro is the finished version
the file urdf/robot.urdf is parsed from robot urdf/robot.xacro
the file urdf/origin.urdf is the file before adding the right wheel and the center wheel.

There are three more lidar which are laser_vert_bottom_gaze, laser_vert_top_right_gaze, and laser_vert_top_left_gaze since I dont know if I need to keep
the three original lidar or not so I kept them and included three more. There is one additional lidar called laser_horiz_velodyne since I dont know if
I need to keep the original laser_horiz or not so I kept it and created one more.

To view the robot description, use command:
roslaunch lab4_package display.launch use_xacro:=false gui:=true
This command will launch will run the robot_state_publisher automatically and the joint_state_publisher according to the input of arg gui.
The argument use_xacro is false by default and the argument gui is true by default. 
