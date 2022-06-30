# 3.8 version is required for `cxx_std_11`
cmake_minimum_required(VERSION 3.8 FATAL_ERROR)

if(NOT DEFINED PROJECT_NAME)
    set(BUILD_AS_STANDALONE ON)
else()
    set(BUILD_AS_STANDALONE OFF)
endif()

project(invoke.hpp)

add_library(${PROJECT_NAME} INTERFACE)
add_library(${PROJECT_NAME}::${PROJECT_NAME} ALIAS ${PROJECT_NAME})

target_compile_features(${PROJECT_NAME} INTERFACE cxx_std_11)
target_include_directories(${PROJECT_NAME} INTERFACE headers)

#
# BUILD_AS_STANDALONE
#

if(NOT ${BUILD_AS_STANDALONE})
    return()
endif()

enable_testing()
set_property(GLOBAL PROPERTY USE_FOLDERS ON)
set_property(GLOBAL PROPERTY PREDEFINED_TARGETS_FOLDER "CMake")
list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake")

add_subdirectory(untests)
