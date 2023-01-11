cmake_minimum_required(VERSION 3.23)
project(cmake_switch_template)

set(CMAKE_C_STANDARD 17)
set(CMAKE_CXX_STANDARD 23)
enable_language(ASM C CXX)

## Project sources
include_directories(${PROJECT_SOURCE_DIR}/include/)
file(GLOB_RECURSE SOURCES_ASM ${PROJECT_SOURCE_DIR}/src/*.s)
file(GLOB_RECURSE SOURCES_C ${PROJECT_SOURCE_DIR}/src/*.c)
file(GLOB_RECURSE SOURCES_CXX ${PROJECT_SOURCE_DIR}/src/*.cpp)

add_executable(cmake_switch_template source/main.cpp)
