cmake_minimum_required(VERSION 3.4.1)

file(GLOB_RECURSE tensorflow_demo_sources src/main/cpp/*.*)
add_library(tensorflow_demo SHARED ${tensorflow_demo_sources})

target_link_libraries(tensorflow_demo)
