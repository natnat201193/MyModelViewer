# CMakeList.txt : Top-level CMake project file, do global configuration
# and include sub-projects here.
#
cmake_minimum_required (VERSION 3.8)

project (MyModelViewer C CXX)

option(GLFW_BUILD_DOCS OFF)
option(GLFW_BUILD_EXAMPLES OFF)
option(GLFW_BUILD_TESTS OFF)
option(GLFW_INSTALL OFF)

# Include sub-projects.
add_subdirectory(MyModelViewer)
add_subdirectory(dependencies/glfw)
include(dependencies/glad/cmake/CMakeLists.txt)
add_subdirectory(dependencies/glm)

# Specify glad settings
glad_add_library(glad REPRODUCIBLE MX MXGLOBAL LANGUAGE C CXX API gl:core=4.6)
