cmake_minimum_required(VERSION 3.15)
project(MergePath
        VERSION 0.0
        DESCRIPTION "Playing with CUDA using Merge Path algorithm"
        LANGUAGES C CXX CUDA)

if (NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE Release)
endif()

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)

find_package(CUDAToolkit)
set(CMAKE_CUDA_STANDARD 17)
set(CMAKE_CUDA_STANDARD_REQUIRED True)
message(${CMAKE_CUDA_TOOLKIT_INCLUDE_DIRECTORIES})

add_subdirectory(src)
add_subdirectory(exe)