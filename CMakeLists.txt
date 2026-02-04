cmake_minimum_required(VERSION 3.20)
project(CPP_DS LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# Choose which lab to build (folder name under ./labs)
set(ACTIVE_LAB "Lab01" CACHE STRING "Lab folder under ./labs to build")

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib")
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib")

if (EXISTS "${CMAKE_SOURCE_DIR}/labs/${ACTIVE_LAB}/CMakeLists.txt")
  add_subdirectory("labs/${ACTIVE_LAB}")
else()
  message(FATAL_ERROR "ACTIVE_LAB='${ACTIVE_LAB}' not found. Expected labs/${ACTIVE_LAB}/CMakeLists.txt")
endif()
