cmake_minimum_required(VERSION 2.8.3)
project(gazebo_to_octomap)

find_package(catkin REQUIRED COMPONENTS
  gazebo_ros
  )

catkin_package()

# add_library(ros_interface_plugin SHARED IMPORTED)
# set_target_properties(ros_interface_plugin PROPERTIES IMPORTED_LOCATION ${PROJECT_SOURCE_DIR}/plugins/gazebo_ros_interface_plugin.so)

# add_library(gazebo_octomap SHARED IMPORTED)
# set_target_properties(gazebo_octomap PROPERTIES IMPORTED_LOCATION ${PROJECT_SOURCE_DIR}/plugins/gazebo_to_octomap_plugin.so)


install(DIRECTORY launch models worlds maps rviz
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

