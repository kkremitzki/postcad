# postcad
# A rock solid project with enforced style, testing and static analysis
# Copyright 2019, Kurt Kremitzki
cmake_minimum_required(VERSION 3.1)
project(postcad C CXX)
set(PROJECT_DESCRIPTION   "A rock solid project with enforced style, testing and static analysis")
set(PROJECT_AUTHOR        "Kurt Kremitzki")
set(PROJECT_URL           "https://github.com/kkremitzki/postcad")
set(PROJECT_VERSION_MAJOR "0")
set(PROJECT_VERSION_MINOR "0")
set(PROJECT_VERSION_PATCH "1")

# Build flags
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O3 -march=native")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra -Werror -pedantic")


# ---------------------------------------------------------
# Features
# ---------------------------------------------------------
add_subdirectory(external)
add_subdirectory(src)

enable_testing()
add_subdirectory(test)
add_subdirectory(doc)
