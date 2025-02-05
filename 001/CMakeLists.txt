cmake_minimum_required(VERSION 3.10)
project(HelloWorldOpenGL)

# Set the OpenGL preference to GLVND
set(OpenGL_GL_PREFERENCE GLVND)

find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)
find_package(Freetype REQUIRED)

# manually specify GLEW path 
set(GLEW_INCLUDE_DIRS "/usr/include")
set(GLEW_LIBRARIES "/usr/lib64/libGLEW.so")

set(GLEW_LIBRARIES "/usr/lib64/libGLEW.so")

add_executable(HelloWorldOpenGL main.cpp)

# Include GLEW headers
target_include_directories(HelloWorldOpenGL PRIVATE ${GLEW_INCLUDE_DIRS})

target_link_libraries(HelloWorldOpenGL 
	OpenGL::GL
	${GLEW_LIBRARIES}
	glfw 
	Freetype::Freetype
)
