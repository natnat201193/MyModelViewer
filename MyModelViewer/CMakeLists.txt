# CMakeList.txt : CMake project for MyModelViewer, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)


# Add source to this project's executable.
add_executable (MyModelViewer MyModelViewer.cpp  MyModelViewer.h)

target_link_libraries(MyModelViewer PRIVATE
	glad
	glfw
	opengl32
	glm)

# TODO: Add tests and install targets if needed.
