project(rANS)
cmake_minimum_required(VERSION 3.2)

if(NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE "Release")
endif()

add_executable(rANS main.cpp platform.h rans_byte.h)
add_executable(rANS_64 main64.cpp platform.h rans64.h)
add_executable(rANS_sse41 main_simd.cpp platform.h rans_word_sse41.h)
add_executable(rANS_alias main_alias.cpp platform.h rans_byte.h)
