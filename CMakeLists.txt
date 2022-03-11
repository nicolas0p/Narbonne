cmake_minimum_required(VERSION 3.16)

project(Narbonne VERSION 1.0.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_MODULE_PATH "${PROJECT_SOURCE_DIR}/cmake" ${CMAKE_MODULE_PATH})

set(CMAKE_PREFIX_PATH "/home/other/Qt/6.2.3/gcc_64")

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

find_package(Qt6 REQUIRED COMPONENTS Widgets)

add_subdirectory(src)

add_subdirectory(extern)

target_link_libraries(
    Narbonne PRIVATE
    Qt6::Widgets
    asio
)
