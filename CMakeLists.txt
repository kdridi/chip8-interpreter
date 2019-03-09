cmake_minimum_required(VERSION 3.11)
project(chip8)

set(CMAKE_CXX_STANDARD 17)

find_package(OpenGL)
find_package(GLUT)

add_executable(${PROJECT_NAME} main.cpp chip8.cpp chip8.h)

target_link_libraries(
        ${PROJECT_NAME}
        ${OPENGL_LIBRARIES}
        ${GLUT_LIBRARIES} )
