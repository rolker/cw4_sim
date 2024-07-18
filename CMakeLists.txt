cmake_minimum_required(VERSION 2.8.3)
project(cw4_sim)

set(CMAKE_CXX_STANDARD 14)

find_package(catkin REQUIRED COMPONENTS
  asv_msgs
  asv_srvs
  asv_sim
  rosgraph_msgs
  rospy
)

catkin_python_setup()

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES asv_sim
#  CATKIN_DEPENDS asv_msgs asv_srvs rospy
#  DEPENDS system_lib
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)


catkin_install_python(PROGRAMS nodes/cw4_sim_node.py
                      DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})
                      
