cmake_minimum_required(VERSION 2.6)

project(imgui)

set(CMAKE_CXX_FLAGS "-Wall -Wformat")

set(SRCS
    imgui.cpp
    imgui_demo.cpp
    imgui_draw.cpp)

add_library(imgui ${SRCS})

add_subdirectory(examples)

