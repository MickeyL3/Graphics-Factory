cmake_minimum_required(VERSION 2.8...3.5)
project(factory VERSION 0.1.0 LANGUAGES C CXX)

add_executable(factory main.cpp)

set(OpenGL_GL_PREFERENCE LEGACY)
find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
include_directories( ${OPENGL_INCLUDE_DIRS}  ${GLUT_INCLUDE_DIRS} )

target_link_libraries( factory ${OPENGL_LIBRARIES} ${GLUT_LIBRARIES} )
