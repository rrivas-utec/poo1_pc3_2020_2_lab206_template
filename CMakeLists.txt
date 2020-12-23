cmake_minimum_required(VERSION 3.10.2)
project(poo1_pc3_2020_2_lab206)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/${OUTPUT_DEBUG})
if(UNIX AND NOT APPLE)
    set(CMAKE_CXX_FLAGS -pthread)
endif()

add_executable(poo1_pc3_2020_2_lab206
  main.cpp 
  test_1.cpp
  p1.h p1.cpp
  )

configure_file(test_1.in ${CMAKE_RUNTIME_OUTPUT_DIRECTORY} COPYONLY)
