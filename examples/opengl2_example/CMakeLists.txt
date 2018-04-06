cmake_minimum_required(VERSION 2.6)

project(opengl2_example)

find_package(PkgConfig REQUIRED)
find_package(glfw3 REQUIRED GLFW)
find_package(OpenGL REQUIRED)

include_directories(/usr/local/include)
include_directories(../..)
include_directories(../libs/gl3w)

add_library(imgui_glfw_gl2 imgui_impl_glfw_gl2.cpp)

link_directories(../libs/gl3w)
add_executable(opengl2_example main.cpp)

set(LIBS
    imgui
    imgui_glfw_gl2
    glfw
    gl3w
    ${OPENGL_gl_LIBRARY})

target_link_libraries(opengl2_example ${LIBS})

