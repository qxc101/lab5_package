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

Lab5:
For this lab, I played back the bag downloaded from the google drive, cloned the map from the case git, and changed the launch file to accept clock, use new xacro given, use new urdf parsed from the given xacro, and change config for rviz. To achieve above changes, I updated lab4_package. I updated and putted the given xacro file in to urdf/ directory and parsed it to form new.urdf for convenience, and also for avoiding some error that might happen when directly using rviz with xacro (there are some mathematical operations that would give errors when directly using xacro file, like {-pi}). I added several args to the launch file. 
If you wish to to view the robot on rviz using original xacro:
roslaunch lab4_package display.launch use_xacro:=true use_new_xacro:=false
If you wish to to view the robot on rviz using original urdf:
roslaunch lab4_package display.launch use_xacro:=false use_new_urdf:=false
If you wish to to view the robot on rviz using the new xacro(for lab5):
roslaunch lab4_package display.launch use_xacro:=true use_new_xacro:=true
If you wish to to view the robot on rviz using new urdf(lab5):
roslaunch lab4_package display.launch use_xacro:=false use_new_urdf:=true
If you wish to to view the robot on rviz using config that is just for viewing the bag msg:
roslaunch lab4_package display.launch config_name:=config2.rviz
Then play the bag.

If you wish to to view the robot on rviz using config that is for viewing the map with robot in it
roslaunch lab4_package display.launch config_name:=config_map_view.rviz
Then run the map server with downloaded map.yaml
Then play the bag
