cmake_minimum_required(VERSION 3.22)
project(ConnectionPool)

set(CMAKE_CXX_STANDARD 14)

file(GLOB SRC_FILES
        "${PROJECT_SOURCE_DIR}/include/*.h"
        "${PROJECT_SOURCE_DIR}/include/*.hpp"
        "${PROJECT_SOURCE_DIR}/src/*.cpp")

include_directories(
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)

add_executable(${CMAKE_PROJECT_NAME} main.cpp ${SRC_FILES})

target_link_libraries(${CMAKE_PROJECT_NAME} mysqlclient)