cmake_minimum_required(VERSION 3.31.1)
project(learning_opengl VERSION 0.1.0)
cmake_policy(SET CMP0072 NEW)

find_package(OpenGL REQUIRED)

add_executable(learning_opengl src/main.cpp include/glad.c)

target_include_directories(learning_opengl
    PRIVATE
    include
)

target_link_libraries(learning_opengl
    glfw
    OpenGL::GL
)
