cmake_minimum_required(VERSION 3.20)
project(DataStructsLabs LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# Add every lab that has a CMakeLists.txt
file(GLOB children RELATIVE "${CMAKE_SOURCE_DIR}/labs" "${CMAKE_SOURCE_DIR}/labs/*")
foreach(child ${children})
  if (EXISTS "${CMAKE_SOURCE_DIR}/labs/${child}/CMakeLists.txt")
    add_subdirectory("labs/${child}")
  endif()
endforeach()
