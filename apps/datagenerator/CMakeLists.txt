#CMakeLists file for datagenerator

lptApplication(Datagenerator)

include_directories("${CMAKE_SOURCE_DIR}/modules/core/include")
include_directories("${CMAKE_SOURCE_DIR}/modules/calib/include")
include_directories("${CMAKE_SOURCE_DIR}/modules/datagen/include")

set (EXTRA_LIBS ${EXTRA_LIBS}
 module-core 
 module-datagen 
 module-calib
 )

add_executable(${PROJECT_NAME} datagenerator.cpp)
target_link_libraries( ${PROJECT_NAME} ${EXTRA_LIBS} )