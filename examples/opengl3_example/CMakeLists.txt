cmake_minimum_required(VERSION 2.6)

project(opengl3_example)

find_package(PkgConfig REQUIRED)
find_package(glfw3 REQUIRED GLFW)
find_package(OpenGL REQUIRED)

set(CMAKE_CXX_FLAGS "-Wall -Wformat")

set(SRCS
    imgui_impl_glfw_gl3.cpp
    ../../imgui.cpp
    ../../imgui_demo.cpp
    ../../imgui_draw.cpp
    main.cpp)

include_directories(../..)
include_directories(../libs/gl3w)

link_directories(../libs/gl3w)

add_executable(opengl3_example ${SRCS})

set(LIBS
    glfw
    gl3w
    ${OpenGL_LIBRARY})

target_link_libraries(opengl3_example ${LIBS})

