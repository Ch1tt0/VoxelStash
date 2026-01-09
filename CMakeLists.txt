cmake_minimum_required(VERSION 4.2.1)
project(VoxelStash VERSION 0.0.1 LANGUAGES CXX)

add_executable(VoxelStash main.cpp)

include(CTest)
enable_testing()

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
