cmake_minimum_required(VERSION 2.8 FATAL_ERROR)
project(robot_common)

find_package(catkin REQUIRED)

catkin_package()

include_directories(${roscpp_INCLUDE_DIRS})
include_directories(${std_msgs_INCLUDE_DIRS})

find_package(catkin REQUIRED COMPONENTS
    geolib2
    code_profiler
    roslib   
    roscpp
    std_msgs
)

# Build our plugin
include_directories(
    include
    3rdparty
    ${catkin_INCLUDE_DIRS}
)
