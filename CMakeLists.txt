cmake_minimum_required(VERSION 3.10)
project(lab05)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} --coverage -g -O0")
set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} --coverage")

add_subdirectory(banking)
add_subdirectory(tests)

include(FetchContent)
FetchContent_Declare(
  coveralls-cmake
  GIT_REPOSITORY https://github.com/JoakimSoderberg/coveralls-cmake.git
)
FetchContent_MakeAvailable(coveralls-cmake)

setup_target_for_coverage_coveralls(
    NAME coveralls
    EXECUTABLE ctest
)
