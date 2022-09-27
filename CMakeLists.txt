cmake_minimum_required(VERSION 3.13)
project(example-grpc LANGUAGES CXX)

include(CheckCXXCompilerFlag)
include(FindProtobuf)

set(CMAKE_CXX_FLAGS_RELEASE "-O3")
set(CMAKE_CXX_FLAGS_DEBUG "-Og -g -ggdb")
set(CMAKE_CXX_STANDARD 17)
add_definitions("-Werror")
add_definitions("-Wall")
add_definitions("-Wextra")

set(CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/cmake")

add_subdirectory(client)
add_subdirectory(server)
add_subdirectory(proto)
