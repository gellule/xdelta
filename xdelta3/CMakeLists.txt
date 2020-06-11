cmake_minimum_required(VERSION 3.10)

project(Xdelta3)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -DSIZEOF_SIZE_T=8 -DSIZEOF_UNSIGNED_LONG=8 -DSIZEOF_UNSIGNED_LONG_LONG=8")

add_library(libXdelta3 xdelta3.c)
set_target_properties(libXdelta3 PROPERTIES PREFIX "")

add_executable(xdelta3 xdelta3.c)
set_target_properties(xdelta3 PROPERTIES COMPILE_FLAGS "-DXD3_MAIN=1")

