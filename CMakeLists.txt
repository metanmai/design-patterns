cmake_minimum_required(VERSION 3.25)
project(design_patterns)

set(CMAKE_CXX_STANDARD 23)

add_executable(design_patterns main.cpp
        stdc++.h
        patterns/creational/builder/desktop.hpp)
