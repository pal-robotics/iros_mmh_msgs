cmake_minimum_required(VERSION 2.8.3)
project(laser_pattern_detector_msgs)

find_package(catkin REQUIRED COMPONENTS
  actionlib
  actionlib_msgs
  geometry_msgs
  message_generation
  sensor_msgs
)

## Generate actions in the 'action' folder
add_service_files(
    FILES
    GetLaserImage.srv
    )
add_action_files(
  FILES
  DetectLaserPattern.action
)

generate_messages(
  DEPENDENCIES
  actionlib_msgs
  geometry_msgs
  sensor_msgs
)

catkin_package(
 CATKIN_DEPENDS actionlib_msgs geometry_msgs sensor_msgs actionlib message_runtime
)

