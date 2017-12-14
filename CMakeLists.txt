cmake_minimum_required(VERSION 3.8)
set(PROJECT_NAME arduMuscleControl)

project(${PROJECT_NAME} C CXX)

set(CMAKE_CXX_STANDARD 17)
set(${CMAKE_PROJECT_NAME}_BOARD nano)
set(${CMAKE_PROJECT_NAME}_PORT COM3)
set(${PROJECT_NAME}_SRCS example.cpp)
generate_arduino_firmware(${PROJECT_NAME})

set(TESTING_FILES )
add_executable(${PROJECT_NAME}-testing ${TESTING_FILES} catch.hpp)
