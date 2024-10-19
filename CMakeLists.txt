cmake_minimum_required(VERSION 3.22)

project(AudioPluginStarter)

set(CMAKE_CXX_STANDARD 23)

set(CPM_SOURCE_CACHE ${CMAKE_CURRENT_SOURCE_DIR}/libs)
include(cmake/CPM.cmake)
