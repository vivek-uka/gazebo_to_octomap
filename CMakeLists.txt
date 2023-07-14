cmake_minimum_required(VERSION 2.8.3)
project(gazebo_to_octomap)

find_package(catkin REQUIRED COMPONENTS
  gazebo_ros
  rotors_gazebo_plugins
  )

catkin_package()

#====================================== OCTOMAP PLUGIN ==========================================//

# Conditionally built since it requires Octomap as a dependency
# ASL uses this, PX4 does not


install(DIRECTORY launch models worlds maps rviz
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

