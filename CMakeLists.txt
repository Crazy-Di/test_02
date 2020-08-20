cmake_minimum_required(VERSION 3.0.0)
project(test_01 VERSION 0.1.0)

include(CTest)
enable_testing()

include_directories(./include)

set(LIBRARY_OUTPUT_PATH ${CMAKE_BINARY_DIR})

add_subdirectory(./src)

add_executable(test_01 main.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

target_link_libraries(test_01 Test)