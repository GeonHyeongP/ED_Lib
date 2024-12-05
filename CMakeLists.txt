cmake_minimum_required(VERSION 3.6)
project(ED_Lib)

set(CMAKE_CXX_STANDARD 11)

find_package(OpenCV)
include_directories(${OpenCV_INCLUDE_DIRS})

add_library(EDLib SHARED
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

target_link_libraries(EDLib ${OpenCV_LIBS})

FILE(GLOB HEADERS *.h)

set(DEPENDENCY_DIR ${CMAKE_CURRENT_BINARY_DIR}/dependencies)
set(DEPENDENCY_INSTALL_DIR ${DEPENDENCY_DIR}/install)

install( TARGETS EDLib DESTINATION lib)
install( FILES ${HEADERS} DESTINATION include/ED_Lib )

#add_executable(test_it test_it.cpp)
#target_link_libraries(test_it ${OpenCV_LIBS} EDLib)

#add_executable(test_ED test_ED.cpp)
#target_link_libraries(test_ED ${OpenCV_LIBS} EDLib)

#add_executable(video_test video_test.cpp)
#target_link_libraries(video_test ${OpenCV_LIBS} EDLib)
