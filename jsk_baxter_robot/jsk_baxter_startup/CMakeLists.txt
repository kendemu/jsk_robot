cmake_minimum_required(VERSION 2.8.3)
project(jsk_baxter_startup)

find_package(catkin REQUIRED COMPONENTS)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES jsk_baxter_startup
#  CATKIN_DEPENDS baxter_interface baxter_tools openni_launch
#  DEPENDS system_lib
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

install(DIRECTORY config jsk_baxter_joy jsk_baxter_lifelog jsk_baxter_moveit jsk_baxter_sensors
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
  USE_SOURCE_PERMISSIONS)

install(FILES baxter.launch DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})

