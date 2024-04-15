cmake_minimum_required(VERSION 3.20)

project(setup-msvc-examples)

if(NOT WIN32)
  string(ASCII 27 Esc)
  set(ColorReset "${Esc}[m")
  set(BoldRed     "${Esc}[1;31m")
  set(BoldGreen   "${Esc}[1;32m")
endif()

message("==========================================")
message("${BoldGreen}CMake executable path (CMAKE_COMMAND): ${CMAKE_COMMAND}${ColorReset}")
message("${BoldGreen}C compiler path (CMAKE_C_COMPILER): ${CMAKE_C_COMPILER}${ColorReset}")
message("${BoldGreen}C++ compiler path (CMAKE_CXX_COMPILER): ${CMAKE_CXX_COMPILER}${ColorReset}")
message("${BoldGreen}vcpkg root (VCPKG_ROOT): $ENV{VCPKG_ROOT}${ColorReset}")
message("==========================================")
