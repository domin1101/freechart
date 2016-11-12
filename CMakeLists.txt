cmake_minimum_required(VERSION 2.6.4)
project (freechart)

file(GLOB_RECURSE SOURCES src/*.cpp src/*.hpp)
include_directories(include)

set(wxWidgets_CONFIGURATION mswu)
find_package(wxWidgets COMPONENTS core base REQUIRED)
include(${wxWidgets_USE_FILE})

add_library(freechart STATIC ${SOURCES})
