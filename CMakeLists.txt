cmake_minimum_required(VERSION 3.10)
project(skeleton_kinect)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_EXTENSIONS OFF)

include_directories(${PROJECT_SOURCE_DIR}/include)

find_package(GLUT REQUIRED)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON CACHE INTERNAL "")
file(GLOB SOURCES "src/*.cpp")

add_executable(skeleton_kinect ${SOURCES})
target_link_libraries(skeleton_kinect GL glut GLU)
