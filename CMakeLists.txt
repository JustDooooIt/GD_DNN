cmake_minimum_required(VERSION 3.10.0)
project(gd_tiny_dnn VERSION 0.1.0 LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(tiny_dnn)

add_library(gd_tiny_dnn gd_tiny_dnn.cpp)

target_link_libraries(gd_tiny_dnn PRIVATE tiny_dnn)

target_compile_options(gd_tiny_dnn PRIVATE "-Wa,-mbig-obj")