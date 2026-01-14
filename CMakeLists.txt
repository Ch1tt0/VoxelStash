cmake_minimum_required(VERSION 4.1)
project(VoxelStash)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_SCAN_FOR_MODULES OFF)
set(CMAKE_EXPORT_COMPILE_COMMANDS TRUE)

find_package(SDL3 CONFIG REQUIRED)
find_package(imgui CONFIG REQUIRED)

add_executable(VoxelStash src/Main.cpp)
target_link_libraries(VoxelStash PRIVATE SDL3::SDL3 imgui::imgui)
