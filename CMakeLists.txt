cmake_minimum_required(VERSION 3.0.2) #버전 필수 기입
project(ros_tutorials)

find_package(catkin REQUIRED COMPONENTS
 rospy 
 std_msgs #메시지
 )

 catkin_python_setup()

 catkin_package(
  CATKIN_DEPENDS rospy std_msgs
 )

 catkin_install_python(PROGRAMS
  node/ai_node.py  #사용자 지정 파이썬 파일
DESTINATIONS ${CATKIN_PACKAGE_BIN_DESTINATION}
)
install(DIRECTORY launch
 DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
