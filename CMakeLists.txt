cmake_minimum_required(VERSION 3.2.3 FATAL_ERROR)
project(fltk-test)

add_subdirectory(lib/fltk)

add_executable(fltk-test src/main.cpp)
target_include_directories(fltk-test PUBLIC 
    $<BUILD_INTERFACE:include ${CMAKE_CURRENT_BINARY_DIR}/lib/fltk ${CMAKE_CURRENT_SOURCE_DIR}/lib/fltk>
)
target_link_libraries(fltk-test fltk)
