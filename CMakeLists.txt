cmake_minimum_required(VERSION 3.15)
project(JPP VERSION 0.1.0)
include_directories(include)

add_library(jpp STATIC include/jpp.hpp include/logger.hpp src/jpp.cpp)

add_executable(test test.cpp)

target_link_libraries(test PRIVATE jpp)
target_include_directories(test PRIVATE
    include
)