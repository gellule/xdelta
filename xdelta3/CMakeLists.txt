cmake_minimum_required(VERSION 3.10)

project(Xdelta3)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -DSIZEOF_SIZE_T=8 -DSIZEOF_UNSIGNED_LONG_LONG=8")

add_library(Xdelta3 xdelta3.c)

