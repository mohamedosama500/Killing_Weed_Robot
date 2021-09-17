cmake_minimum_required(VERSION 2.8.3)

project(KWR)

find_package(catkin REQUIRED COMPONENTS
rospy
roscpp
tf
nav_msgs
sensor_msgs
robot_localization
controller_manager)

catkin_package()

find_package(roslaunch)

foreach(dir config launch meshes urdf)
	install(DIRECTORY ${dir}/
		DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/${dir})
endforeach(dir)


