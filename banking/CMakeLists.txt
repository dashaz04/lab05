cmake_minimum_required(VERSION 3.10)
project(lab05)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(account STATIC account.cpp)
target_include_directories(account PUBLIC ./)

add_library(transaction STATIC transaction.cpp)
target_include_directories(transaction PUBLIC ./)
