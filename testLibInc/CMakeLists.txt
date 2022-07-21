# file: CMakeLists.txt
# author: Christoph Kolhoff, M.Sc.
# brief: This file contains an example to use a shared object library on linux

cmake_minimum_required(VERSION 3.16.3)
project (testingTestLib)
set(CMAKE_CXX_STANDARD 17)

add_compile_options(-Wall -Wextra -Wpedantic -L/usr/lib/libtestLib.so)

find_library(TEST_LIB libtestLib.so)
message(STATUS ${TEST_LIB})

include_directories(/usr/local/inc/)
include_directories(/usr/lib/)

add_executable(testingTestLib main.cpp)
target_link_libraries(testingTestLib PRIVATE ${TEST_LIB})

# https://surfertas.github.io/cmake/cpp/projecteuler/2019/05/01/cmake.html
