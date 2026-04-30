cmake_minimum_required(VERSION 3.10)
project(lab05)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

if(CMAKE_BUILD_TYPE STREQUAL "Debug")
    if(CMAKE_CXX_COMPILER_ID STREQUAL "GNU" OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
        add_compile_options(--coverage)
        add_link_options(--coverage)
    endif()
endif()

add_subdirectory(banking)
add_subdirectory(tests)

