cmake_minimum_required(VERSION 3.10.2)

project(CMAKE_GENERIC)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(src/)

add_executable(main main.cpp)

target_include_directories(main PUBLIC)

target_include_directories(LIB_NAME PUBLIC include)

#after PRIVATE, add libraries you define in your src folder to link them to the main CMake.
target_link_libraries(main PRIVATE LIB_NAME -std=c++0x -pthread)