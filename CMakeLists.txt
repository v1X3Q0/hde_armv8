cmake_minimum_required(VERSION 3.15.0)
project(hdeA64 VERSION 0.1.0)

if(NOT DEFINED ANDROID_TOOL_BASE)
    message("no ANDROID_TOOL_BASE, setting to working directory")
    set(ANDROID_TOOL_BASE ${CMAKE_CURRENT_SOURCE_DIR})
endif()

add_library(${PROJECT_NAME} STATIC hdeA64.c)
target_include_directories(${PROJECT_NAME} PRIVATE
    ${ANDROID_TOOL_BASE}/common/local_util)