cmake_minimum_required(VERSION 3.0.2)
project(message_transformer_cpp)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  message_runtime
  roscpp
  rospy
  std_msgs
  geometry_msgs
)

add_message_files(
  DIRECTORY
    msg
  FILES
    BatteryData.msg
)

generate_messages(
  DEPENDENCIES
    std_msgs
    geometry_msgs
)

catkin_package(
  CATKIN_DEPENDS
    message_runtime
)
