cmake_minimum_required(VERSION 2.6)

project(gl3w)

set(CMAKE_CXX_FLAGS "-Wall -Wformat")

set(SRCS GL/gl3w.c)

include_directories(.)

add_library(gl3w ${SRCS})

