cmake_minimum_required(VERSION 2.8)

project( test )

set (CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -g")

include_directories ("${PROJECT_SOURCE_DIR}/../../detect")
link_directories("${PROJECT_SOURCE_DIR}/../../build/detect")

add_executable( test test.c )
target_link_libraries( test detect ${OpenCV_LIBS} )