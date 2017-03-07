cmake_minimum_required(VERSION 3.6)
project(bsdiff)

set(CMAKE_C_STANDARD 99)

add_subdirectory(libbz)

set(SOURCE_FILES bspatch.c bspatch.c)

#add_executable(bsdiff ${SOURCE_FILES})
add_library(bsdiff SHARED ${SOURCE_FILES})

target_link_libraries(bsdiff bz)