cmake_minimum_required(VERSION 3.19.2)
project(CppDesignPattern)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_BINARY_DIR ${CMAKE_CURRENT_BINARY_DIR}/bin)

ADD_SUBDIRECTORY(BehavioralPattern)
ADD_SUBDIRECTORY(CreationalPattern)
ADD_SUBDIRECTORY(StructuralPattern)