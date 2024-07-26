# The following five lines of boilerplate have to be in your project's
# CMakeLists in this exact order for cmake to work correctly
cmake_minimum_required(VERSION 3.16)

# Get the BINARY_VERSION environment variable, default to "3.1.0" if not set
if(DEFINED ENV{BINARY_VERSION})
  set(PROJECT_VER $ENV{BINARY_VERSION})
else()
  set(PROJECT_VER "0.0.0")
endif()

include($ENV{IDF_PATH}/tools/cmake/project.cmake)
project(blink)