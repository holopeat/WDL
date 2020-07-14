cmake_minimum_required(VERSION 3.14)

project(wdl)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(${PROJECT_NAME} "")
target_include_directories(${PROJECT_NAME} PUBLIC WDL)

set(WDL_DSP_SOURCES
    WDL/convoengine.cpp
    WDL/fft.c
    WDL/resample.cpp
)

target_sources(${PROJECT_NAME} PRIVATE ${WDL_DSP_SOURCES})
