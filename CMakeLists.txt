cmake_minimum_required(VERSION 2.8)

set(PROJECT barebone-cocoa)

project(${PROJECT})

find_library(COCOA_LIBRARY Cocoa)
find_library(CARBON_LIBRARY Carbon)

set(SOURCE_FILES
    src/appDelegate.h
    src/appDelegate.m
    src/bareboneApp.h
    src/bareboneApp.m
    src/main.m
    src/windowDelegate.h
    src/windowDelegate.m
)

add_executable(${PROJECT}
    ${SOURCE_FILES}
)

target_link_libraries(${PROJECT}
    ${COCOA_LIBRARY}
    ${CARBON_LIBRARY}
)
