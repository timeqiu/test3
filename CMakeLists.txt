cmake_minimum_required(VERSION 2.8)
project( ChamferMatchingTester )

#SET("OpenCV_DIR" "C:/opencv30/opencv/build")

SET("OpenCV_DIR" "C:/opencv3/build")

find_package(OpenCV REQUIRED)

include_directories(${OpenCV_INCLUDE_DIRS})

add_executable( ChamferMatchingTester src/ChamferMatchingTester.cpp )

target_link_libraries( ChamferMatchingTester ${OpenCV_LIBS} )

