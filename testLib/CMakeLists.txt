# file: CMakeLists.txt
# author: Christoph Kolhoff, M.Sc.
# brief: This file contains an example to build a shared object library on linux

cmake_minimum_required(VERSION 3.16.3)
project (testLib)
set(CMAKE_CXX_STANDARD 20)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/inc)
add_library(testLib SHARED src/test.cpp)

install(TARGETS testLib DESTINATION /usr/lib)
install(FILES inc/test.h DESTINATION inc)

# https://surfertas.github.io/cmake/cpp/projecteuler/2019/05/01/cmake.html
