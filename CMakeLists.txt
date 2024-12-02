cmake_minimum_required(VERSION 3.6)
project(ED_Lib)

set(CMAKE_CXX_STANDARD 11)

find_package(opencv)

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
