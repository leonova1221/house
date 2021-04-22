cmake_minimum_required(VERSION 3.5)

project(house LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(SDL2 REQUIRED)
include_directories(house${SDL2_INCLUDE_DIRS})

add_executable(house main.cpp)
target_link_libraries(house ${SDL2_LIBRARIES})
