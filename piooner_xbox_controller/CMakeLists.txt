cmake_minimum_required(VERSION 2.8.3)
project(piooner_xbox_controller)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  joy
  rosaria
  roscpp
  rospy
  std_msgs
  geometry_msgs
)



################################################
## Declare ROS messages, services and actions ##
################################################


## Generate messages in the 'msg' folder
# add_message_files(
#   FILES
#   Message1.msg
#   Message2.msg
# )

## Generate services in the 'srv' folder
# add_service_files(
#   FILES
#   Service1.srv
#   Service2.srv
# )

## Generate actions in the 'action' folder
# add_action_files(
#   FILES
#   Action1.action
#   Action2.action
# )

## Generate added messages and services with any dependencies listed here
# generate_messages(
#   DEPENDENCIES
#   std_msgs
# )

###################################
## catkin specific configuration ##
###################################

catkin_package(CATKIN_DEPENDS joy rosaria roscpp rospy std_msgs geometry_msgs
)

###########
## Build ##
###########

## Specify additional locations of header files
## Your package locations should be listed before other locations
# include_directories(include)
include_directories(
  ${catkin_INCLUDE_DIRS}
)

## Declare a cpp executable
add_executable(xboxJostick2piooner src/joystick2piooner.cpp)

## Specify libraries to link a library or executable target against
target_link_libraries(xboxJostick2piooner ${catkin_LIBRARIES})

#############
## Install ##
#############


#############
## Testing ##
#############


