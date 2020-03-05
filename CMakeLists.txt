cmake_minimum_required(VERSION 3.0.2)
set(CMAKE_INSTALL_PREFIX install)

project(LearnOpenGL)

FILE(GLOB_RECURSE SRC_LIST "${PROJECT_SOURCE_DIR}/src/*.cpp" "${PROJECT_SOURCE_DIR}/src/*.c")
FILE(GLOB_RECURSE LIB_LIST "${PROJECT_SOURCE_DIR}/lib/*.lib")

INCLUDE_DIRECTORIES(include)

add_executable(helloworld ${SRC_LIST})
TARGET_LINK_LIBRARIES(helloworld 
    ${PROJECT_SOURCE_DIR}/lib/glfw3.lib
    ${PROJECT_SOURCE_DIR}/lib/OpenGL32.Lib
)