cmake_minimum_required(VERSION 2.8.3)
project(laser_servoing_msgs)

find_package(catkin REQUIRED COMPONENTS
  actionlib
  actionlib_msgs
  geometry_msgs
  message_generation
)

## Generate actions in the 'action' folder
add_action_files(
  FILES
  GoToTarget.action
  Dock.action
  Undock.action
)

generate_messages(
  DEPENDENCIES
  actionlib_msgs
  geometry_msgs
)

catkin_package(
 CATKIN_DEPENDS actionlib_msgs geometry_msgs actionlib
)

