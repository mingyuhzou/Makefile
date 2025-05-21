cmake_minimum_required(VERSION 3.10)
project(demo VERSION 1.0 LANGUAGES C)

set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED on)

add_library(Mylib src/hello.c)

target_include_directories(Mylib PUBLIC ${PROJECT_SOURCE_DIR}/include)

add_executable(main src/main.c)

target_link_libraries(main Mylib)
