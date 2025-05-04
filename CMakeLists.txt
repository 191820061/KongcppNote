cmake_minimum_required(VERSION 3.10)
project(MiniHttpServer VERSION 0.1 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED on)
set(SRC_DIR ${PROJECT_SOURCE_DIR}/src)
set(INC_DIR ${PROJECT_SOURCE_DIR}/include)

add_executable(http_server 
    ${SRC_DIR}/main.cpp
)

target_compile_options(http_server PRIVATE -Wall -O2)
target_include_directories(http_server PRIVATE ${INC_DIR})


