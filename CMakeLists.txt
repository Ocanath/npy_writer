cmake_minimum_required(VERSION 3.22) # Dawn requires CMake >= 3.22
project(npy_writer C CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)


add_library(npy_writer STATIC
    npy_writer.cpp
)

target_include_directories(npy_writer PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
)
