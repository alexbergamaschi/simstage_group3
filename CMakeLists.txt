cmake_minimum_required(VERSION 2.8.3)
project(simstage_group3)

find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  nav_msgs
  roscpp
  rospy
  sensor_msgs
  stage_ros
  std_msgs
  tf
)

catkin_package(
)
include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

add_executable(main src/main.cpp src/robot_controller.cpp)
target_link_libraries(main ${catkin_LIBRARIES})
