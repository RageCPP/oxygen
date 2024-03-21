cmake_minimum_required(VERSION 3.27)

project(oxygen LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++23 -O3 -Wall -Wextra -Wpedantic -Werror")
option(CMAKE_VERBOSE_MAKEFILE "show compilation process" ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON CACHE INTERNAL "compile_commands.json generate")
set(CMAKE_MODULE_PATH "${PROJECT_SOURCE_DIR}/cmake")

set(CMAKE_INSTALL_PREFIX ${PROJECT_SOURCE_DIR})

set(OXYGEN_INSTALL_INCLUDE_DIR ${PROJECT_SOURCE_DIR}/include)
set(OXYGEN_INSTALL_BIN_DIR ${PROJECT_SOURCE_DIR}/bin)
set(OXYGEN_INSTALL_LIB_DIR ${PROJECT_SOURCE_DIR}/lib)

set(OXYGEN_HEADERS_DIR ${PROJECT_SOURCE_DIR}/src/oxygen)

include_directories(${OXYGEN_HEADERS_DIR})
include_directories(${OXYGEN_INSTALL_INCLUDE_DIR})

add_subdirectory(src)
# add_subdirectory(test)
