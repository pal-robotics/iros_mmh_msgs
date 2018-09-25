cmake_minimum_required(VERSION 2.8.3)
project(dock_charge_sm_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  std_msgs
  actionlib
  actionlib_msgs
)

## Generate actions in the 'action' folder
add_action_files(
  FILES
  GoAndDock.action
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
  actionlib_msgs
)

catkin_package(
)

