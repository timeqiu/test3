cmake_minimum_required(VERSION 2.8)
project( DisplayImage )


#if (NOT CMAKE_BUILD_TYPE)
#    message(STATUS "No build type selected, defaulting to Release")
#    set(CMAKE_BUILD_TYPE "Release")
#endif()

#set(OpenCV_STATIC ON)
#set(OpenCV_CUDA OFF)
#set(OpenCV_DIR "${CMAKE_SOURCE_DIR}/../install")

#set(OpenCV_DIR "C:/opencv3/build")
SET("OpenCV_DIR" "C:/opencv30/opencv/build")
find_package(OpenCV REQUIRED)


#include_directories(
#    src
#    ${EIGEN_INCLUDE_DIRS}
#    ${OpenCV_INCLUDE_DIRS}
#)


include_directories(${OpenCV_INCLUDE_DIRS})

#link_directories(${OpenCV_LIB_DIR})

#file(GLOB my_source_files ./src/*)

#add_executable( DisplayImage ${my_source_files})

#target_link_libraries(DisplayImage ${OpenCV_LIBS})
#Just to remind that you should set OpenCV_STATIC and OpenCV_CUDA as well before you invoke OpenCVConfig.cmake.



add_executable( DisplayImage src/DisplayImage.cpp )

target_link_libraries( DisplayImage ${OpenCV_LIBS} )

