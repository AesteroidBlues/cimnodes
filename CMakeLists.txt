cmake_minimum_required(VERSION 3.20)
project(cimnodes)

set (CMAKE_CXX_STANDARD 11)

add_definitions(-DIMNODES_NAMESPACE=imnodes)

add_library(cimnodes SHARED
    ../cimgui/imgui/imgui.cpp
    ../cimgui/imgui/imgui_draw.cpp
    ../cimgui/imgui/imgui_demo.cpp
    ../cimgui/imgui/imgui_widgets.cpp
	../cimgui/imgui/imgui_tables.cpp
    cimnodes.cpp
    imnodes/imnodes.cpp)

target_include_directories(cimnodes PUBLIC ../cimgui)
target_include_directories(cimnodes PUBLIC ../cimgui/imgui)
set_target_properties(cimnodes PROPERTIES PREFIX "")