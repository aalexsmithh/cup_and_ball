cmake_minimum_required(VERSION 2.8.3)
project(cup_and_ball)

find_package(catkin REQUIRED COMPONENTS
  xacro
)


###################################
## catkin specific configuration ##
###################################
catkin_package(
   INCLUDE_DIRS urdf 
   CATKIN_DEPENDS xacro
)

#############
## Install ##
#############

## install urdf files
install(DIRECTORY urdf 
    DESTINATION ${CATKIN_PACKAGE_INCLUDE_DESTINATION}
)
install(DIRECTORY meshes 
    DESTINATION ${CATKIN_PACKAGE_INCLUDE_DESTINATION}
)

install(DIRECTORY launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
  FILES_MATCHING PATTERN "*.launch"
)
