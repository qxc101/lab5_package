Qi Cheng
qxc101

This is a package for EECS 373 Lab #4. 
The file urdf/robot.xacro is the finished version
the file urdf/robot.urdf is parsed from robot urdf/robot.xacro
the file urdf/origin.urdf is the file before adding the right wheel and the center wheel.

To view the robot description, use command:
roslaunch lab4_package display.launch use_xacro:=false gui:=true
This command will launch will run the robot_state_publisher automatically and the joint_state_publisher according to the input of arg gui.
The argument use_xacro is false by default and the argument gui is true by default. 
