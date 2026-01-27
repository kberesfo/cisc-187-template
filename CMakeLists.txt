cmake_minimum_required(VERSION 3.20)
project(CPP_DS LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# Build the cloned lab repo (expects it has its own CMakeLists.txt)
if (EXISTS "${CMAKE_SOURCE_DIR}/lab/CMakeLists.txt")
  add_subdirectory(lab)
else()
  message(FATAL_ERROR "No lab found. Clone your assignment into ./lab (must contain lab/CMakeLists.txt).")
endif()