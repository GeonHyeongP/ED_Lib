cmake_minimum_required(VERSION 3.6)
project(ED_Lib)

set(CMAKE_CXX_STANDARD 11)

find_package(OpenCV)
include_directories(${OpenCV_INCLUDE_DIRS})

message(${OpenCV_INCLUDE_DIRS})

add_library(EDLib STATIC
        ED.cpp
        ED.h
        EDCircles.cpp
        EDCircles.h
        EDColor.cpp
        EDColor.h
        EDLib.h
        EDLines.cpp
        EDLines.h
        EDPF.cpp
        EDPF.h
        NFA.cpp
        NFA.h)
