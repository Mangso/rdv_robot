cmake_minimum_required(VERSION 2.8.3)
project(indy_driver_py)

find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  rospy
  rviz
  tf
  urdf
  xacro
  std_msgs
  message_generation
)

add_service_files(
  FILES
  indy_blend.srv
)

generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
)

