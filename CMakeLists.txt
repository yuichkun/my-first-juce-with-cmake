cmake_minimum_required(VERSION 3.22)

project(AudioPluginStarter)

set(CMAKE_CXX_STANDARD 23)

set(LIB_DIR ${CMAKE_CURRENT_SOURCE_DIR}/libs)
set(CPM_SOURCE_CACHE ${CMAKE_CURRENT_SOURCE_DIR}/libs)
file(
  DOWNLOAD
  https://github.com/cpm-cmake/CPM.cmake/releases/download/v0.38.3/CPM.cmake
  ${CMAKE_CURRENT_BINARY_DIR}/cmake/CPM.cmake
  EXPECTED_HASH SHA256=cc155ce02e7945e7b8967ddfaff0b050e958a723ef7aad3766d368940cb15494
)
include(${CMAKE_CURRENT_BINARY_DIR}/cmake/CPM.cmake)

CPMAddPackage(
  NAME JUCE
  GITHUB_REPOSITORY juce-framework/JUCE
  GIT_TAG 8.0.3
  VERSION 8.0.3
  SOURCE_DIR ${LIB_DIR}/juce
)