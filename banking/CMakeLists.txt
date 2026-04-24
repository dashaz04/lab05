cmake_minimum_required(VERSION 3.10)
project(lab05)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(Account STATIC Account.cpp)
target_include_directories(Account PUBLIC ./)

add_library(Transaction STATIC Transaction.cpp)
target_include_directories(Transaction PUBLIC ./)
