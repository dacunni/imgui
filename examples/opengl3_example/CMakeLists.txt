cmake_minimum_required(VERSION 2.6)

project(opengl3_example)

find_package(PkgConfig REQUIRED)
find_package(glfw3 REQUIRED GLFW)
find_package(OpenGL REQUIRED)

include_directories(/usr/local/include)
include_directories(../..)
include_directories(../libs/gl3w)

add_library(imgui_glfw_gl3 imgui_impl_glfw_gl3.cpp)

link_directories(../libs/gl3w)
add_executable(opengl3_example main.cpp)

set(LIBS
    imgui
    imgui_glfw_gl3
    glfw
    gl3w
    ${OpenGL_LIBRARY})

target_link_libraries(opengl3_example ${LIBS})

