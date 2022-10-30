cmake_minimum_required(VERSION 3.0.2)
project(ros_tutorials)

find_package(catkin REQUIRED COMPONENTS
 rospy
 std_msgs
 )

 catkin_python_setup()

 catkin_package(
  CATKIN_DEPENDS rospy std_msgs
 )

 catkin_install_python(PROGRAMS
  node/ai_node.py
DESTINATIONS ${CATKIN_PACKAGE_BIN_DESTINATION}
)
install(DIRECTORY launch
 DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)