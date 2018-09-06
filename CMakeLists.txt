cmake_minimum_required(VERSION 3.6)
project(bsdiff)

set(CMAKE_C_STANDARD 99)

add_subdirectory(libbz)

set(SOURCE_PATCH bspatch.c)
set(SOURCE_DIFF bsdiff.c)

add_library(bspatch STATIC ${SOURCE_PATCH} ${SOURCE_DIFF})
#add_library(bspatch SHARED ${SOURCE_PATCH} ${SOURCE_DIFF})

target_link_libraries(bspatch bz)