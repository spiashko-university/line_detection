cmake_minimum_required(VERSION 3.9)
project(line_detection)

set(CMAKE_CXX_STANDARD 11)

find_package( OpenCV REQUIRED )
set(SOURCE_FILES main.cpp)
add_executable(line_detection ${SOURCE_FILES})
include_directories(${OpenCV_INCLUDE_DIRS})
target_link_libraries( line_detection ${OpenCV_LIBS} )

configure_file(line.jpg line.jpg COPYONLY)