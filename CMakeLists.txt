cmake_minimum_required(VERSION 3.10)
project(tests)

add_library(hash_lib INTERFACE)
target_include_directories(hash_lib INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)

add_executable(Testing
        src/testing.cpp)

target_link_libraries(Testing hash_lib)

add_executable(EfficiencyTests
        src/efficiency_tests.cpp)
target_link_libraries(EfficiencyTests hash_lib)
