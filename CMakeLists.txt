project(ETH3DTwoViewEvaluation)
cmake_minimum_required(VERSION 2.8)

set(CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/cmake)

# External dependency: boost filesystem
find_package(Boost COMPONENTS filesystem system REQUIRED)
include_directories(${Boost_INCLUDE_DIRS})
link_directories(${Boost_LIBRARY_DIRS})

# External dependency: libPNG.
find_package(PNG REQUIRED)
include_directories(${PNG_INCLUDE_DIR})

# Settings.
if(NOT CMAKE_BUILD_TYPE)
  message(STATUS "Build type not specified, using RelWithDebInfo")
  set(CMAKE_BUILD_TYPE RelWithDebInfo)
endif()

if(NOT "${CMAKE_CXX_COMPILER_ID}" STREQUAL "MSVC")
    add_definitions("-O2 -msse2 -msse3 -std=c++11")
endif()

include_directories(
    ./src
)

# Evaluation executable.
add_executable(ETH3DTwoViewEvaluation
    src/main.cc
)
target_link_libraries(ETH3DTwoViewEvaluation
    ${PNG_LIBRARY}
    ${Boost_LIBRARIES}
)
