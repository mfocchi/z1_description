cmake_minimum_required(VERSION 3.0.2)
project(z1_description)

find_package(catkin REQUIRED COMPONENTS
  urdf
  xacro
)

catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
)


install(DIRECTORY config/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/config
  PATTERN ".svn" EXCLUDE)

install(DIRECTORY launch/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch
  PATTERN ".svn" EXCLUDE)


install(DIRECTORY meshes/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/meshes
  PATTERN ".svn" EXCLUDE)
  
  install(DIRECTORY rviz/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/rviz
  PATTERN ".svn" EXCLUDE)
  
  install(DIRECTORY urdfs/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/urdfs
  PATTERN ".svn" EXCLUDE)
  
  install(DIRECTORY robots/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/robots
  PATTERN ".svn" EXCLUDE)
  
    
  install(DIRECTORY gazebo/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/gazebo
  PATTERN ".svn" EXCLUDE)
  
catkin_install_python(PROGRAMS scripts/go0
    DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})
