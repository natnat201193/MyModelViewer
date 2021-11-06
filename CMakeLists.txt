# CMakeList.txt : Top-level CMake project file, do global configuration
# and include sub-projects here.
#
cmake_minimum_required (VERSION 3.8)

project ("MyModelViewer" C CXX)

# Include sub-projects.
add_subdirectory ("MyModelViewer")
add_subdirectory(dependencies/glfw)

# Path to glad directory
set(GLAD_SOURCES_DIR "${PROJECT_SOURCE_DIR}/dependencies/glad")
# Path to glad cmake files
add_subdirectory("${GLAD_SOURCES_DIR}/cmake" glad_cmake)

# Specify glad settings
glad_add_library(glad REPRODUCIBLE API gl:core=4.6)

