cmake_minimum_required(VERSION 3.10)
project(lab05)

include_directories(../banking)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
add_executable(check 
    test.cpp 
    ../banking/Account.cpp 
    ../banking/Transaction.cpp
)
target_link_libraries(check gtest gtest_main gmock)
