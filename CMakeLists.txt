cmake_minimum_required(VERSION 3.5)

project(opengl_textures LANGUAGES CXX C)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(opengl_textures main.cpp glad.c)

# opengl specific
find_package(glfw3 3.3 REQUIRED)
target_link_libraries(opengl_textures glfw)
find_package(OpenGL REQUIRED)
target_link_libraries(opengl_textures OpenGL::GL)
