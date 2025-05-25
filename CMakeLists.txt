cmake_minimum_required(VERSION 3.10.0)
project(gd_tiny_dnn VERSION 0.1.0 LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(gd_tiny_dnn gd_tiny_dnn.cpp)

target_include_directories(gd_tiny_dnn SYSTEM INTERFACE ${CMAKE_SOURCE_DIR}/tiny_dnn)
target_include_directories(gd_tiny_dnn SYSTEM INTERFACE ${CMAKE_SOURCE_DIR}/third_party)
target_include_directories(gd_tiny_dnn SYSTEM INTERFACE ${CMAKE_SOURCE_DIR}/cereal)