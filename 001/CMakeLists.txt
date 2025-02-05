cmake_minimum_required(VERSION 3.10)
project(HelloWorldOpenGL)

set(CMAKE_CXX_STANDARD 17)

find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)
find_package(Freetype REQUIRED)

add_executable(HelloWorldOpenGL main.cpp)

target_link_libraries(HelloWorldOpenGL OpenGL::GL glfw Freetype::Freetype)
