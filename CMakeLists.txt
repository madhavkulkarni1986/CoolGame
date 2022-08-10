cmake_minimum_required(VERSION 3.16.0)
project(coolGame)
enable_testing()

include_directories(include)

add_subdirectory(src)
add_subdirectory(test)
add_subdirectory(lib/googletest)
