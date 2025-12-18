cmake_minimum_required(VERSION 3.10)
project(MyOpenGLProject)

set(CMAKE_CXX_STANDARD 17)

# Include directories
include_directories(include)
include_directories(/usr/include) # for GLFW and GLM

# Source files
set(SOURCES
    src/main.cpp
    libs/glad.c
)

# Find OpenGL
find_package(OpenGL REQUIRED)

# Add executable
add_executable(${PROJECT_NAME} ${SOURCES})

# Link libraries
target_link_libraries(${PROJECT_NAME} glfw GL m)

