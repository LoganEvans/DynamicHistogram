cmake_minimum_required(VERSION 3.10)
project(DynamicHistogram)

set(CMAKE_CXX_STANDARD 20)
add_compile_options(-Wthread-safety)

include_directories(src)

add_subdirectory(src)
add_subdirectory(test)

set(BENCHMARK_ENABLE_TESTING OFF CACHE BOOL "Suppressing benchmark's tests" FORCE)
add_subdirectory(lib/benchmark)
add_subdirectory(lib/googletest)
