cmake_minimum_required(VERSION 3.5.0)
project(hdeA64 VERSION 0.1.0)

if(NOT DEFINED ANDROID_TOOL_BASE)
    message(FATAL_ERROR "need ANDROID_TOOL_BASE")
endif()

add_library(${PROJECT_NAME} SHARED hdeA64.c)
target_include_directories(${PROJECT_NAME} PRIVATE
    ${ANDROID_TOOL_BASE}/common/local_util)