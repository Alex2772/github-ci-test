cmake_minimum_required(VERSION 3.16)

project(test)

add_executable(test main.cpp)


# Use AUI.Boot
file(
        DOWNLOAD
        https://raw.githubusercontent.com/aui-framework/aui/feat/aui-boot-precompiled/aui.boot.cmake
        ${CMAKE_CURRENT_BINARY_DIR}/aui.boot.cmake)
include(${CMAKE_CURRENT_BINARY_DIR}/aui.boot.cmake)

install(TARGETS test)

auib_precompiled_binary()