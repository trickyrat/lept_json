cmake_minimum_required(VERSION 3.21)
project(leptjson)
set(CMAKE_C_STANDARD 17)
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -ansi -pedantic -Wall")

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/build/bin)
set(LIBRARY_OUTPUT_PATH  ${PROJECT_SOURCE_DIR}/build/lib)


add_library(leptjson_library src/leptjson.c lib/leptjson.h)
add_executable(leptjson_binary src/test.c)
target_link_libraries(leptjson_binary leptjson_library)