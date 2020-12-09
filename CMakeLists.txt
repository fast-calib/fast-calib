# CMakeList.txt : Top-level CMake project file, do global configuration and include sub-projects here.
cmake_minimum_required (VERSION 3.17)

# Define the name of the project, version, description and language
project(
  "fast_calib"
  VERSION "0.0.1"
  DESCRIPTION "Fast, accurate, and deployable Camera Calibration Solution"
  LANGUAGES CXX)

# Set a default build type if none was specified
set(default_build_type "Release")
if(EXISTS "${CMAKE_SOURCE_DIR}/.git")
  set(default_build_type "RelWithDebInfo")
endif()

if(NOT CMAKE_BUILD_TYPE AND NOT CMAKE_CONFIGURATION_TYPES)
  message(STATUS "Setting build type to '${default_build_type}' as none was specified.")
  set(CMAKE_BUILD_TYPE "${default_build_type}" CACHE
      STRING "Choose the type of build." FORCE)
  # Set the possible values of build type for cmake-gui
  set_property(CACHE CMAKE_BUILD_TYPE PROPERTY STRINGS
    "Debug" "Release" "MinSizeRel" "RelWithDebInfo")
endif()

# Set Base compilation flags
set(CMAKE_CXX_FLAGS_INIT "-g -Wall -O3")
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED True)

##################### Eigen3 Package #####################
find_package(Eigen3 REQUIRED)

# Create configuration file
configure_file("apps/fast_calib_config.h.in" "fast_calib_config.h")

# Include main application
add_subdirectory ("apps")

# Include librarues subdirectory
# add_subdirectory("libs")

# Include external libraries subdirectory
add_subdirectory("external")
