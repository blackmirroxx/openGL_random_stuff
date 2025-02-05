cmake_minimum_required(VERSION 3.10)
project(HelloWorldOpenGL)

# Set the OpenGL preference to GLVND
set(OpenGL_GL_PREFERENCE GLVND)

find_package(OpenGL REQUIRED)
find_package(GLEW REQUIRED)
find_package(glfw3 REQUIRED)
find_package(Freetype REQUIRED)

add_executable(HelloWorldOpenGL main.cpp)

target_link_libraries(HelloWorldOpenGL 
	OpenGL::GL
	GLEW::GLEW
	glfw 
	Freetype::Freetype
)
