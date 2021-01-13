cmake_minimum_required(VERSION 3.0.2)
project(dynamic_reconfigure_client_sample)


find_package(catkin REQUIRED COMPONENTS
  roscpp
  dynamic_reconfigure
)
include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)
catkin_package()
add_executable(sample src/sample.cpp)

target_link_libraries(sample
  ${catkin_LIBRARIES}
)