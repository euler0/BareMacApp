cmake_minimum_required(VERSION 2.8)

set(PROJECT barebone-cocoa)

project(${PROJECT})

find_library(COCOA_LIBRARY Cocoa)

set(SOURCE_FILES
    src/AppDelegate.h
    src/AppDelegate.m
    src/BareboneApp.h
    src/BareboneApp.m
    src/main.m
    src/WindowDelegate.h
    src/WindowDelegate.m
)

add_executable(${PROJECT}
    ${SOURCE_FILES}
)

target_link_libraries(${PROJECT}
    ${COCOA_LIBRARY}
)
