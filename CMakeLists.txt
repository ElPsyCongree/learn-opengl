cmake_minimum_required(VERSION 3.0.2)
set(CMAKE_INSTALL_PREFIX install)

project(LearnOpenGL)

FILE(GLOB_RECURSE SRC_HELLO_WINDOW_LIST "${PROJECT_SOURCE_DIR}/src/HelloWindow/*.cpp" "${PROJECT_SOURCE_DIR}/src/*.c")
FILE(GLOB_RECURSE SRC_HELLO_TRIANGLE_LIST "${PROJECT_SOURCE_DIR}/src/HelloTriangle/*.cpp" "${PROJECT_SOURCE_DIR}/src/*.c")
FILE(GLOB_RECURSE SRC_HELLO_SHADER_LIST "${PROJECT_SOURCE_DIR}/src/HelloShader/*.cpp" "${PROJECT_SOURCE_DIR}/src/*.c")
FILE(GLOB_RECURSE LIB_LIST "${PROJECT_SOURCE_DIR}/lib/*.lib")

INCLUDE_DIRECTORIES(include)

add_executable(hellowindow ${SRC_HELLO_WINDOW_LIST})
TARGET_LINK_LIBRARIES(hellowindow 
    ${PROJECT_SOURCE_DIR}/lib/glfw3.lib
    ${PROJECT_SOURCE_DIR}/lib/OpenGL32.Lib
)

add_executable(hellotriangle ${SRC_HELLO_TRIANGLE_LIST})
TARGET_LINK_LIBRARIES(hellotriangle 
    ${PROJECT_SOURCE_DIR}/lib/glfw3.lib
    ${PROJECT_SOURCE_DIR}/lib/OpenGL32.Lib
)

add_executable(helloshader ${SRC_HELLO_SHADER_LIST})
TARGET_LINK_LIBRARIES(helloshader 
    ${PROJECT_SOURCE_DIR}/lib/glfw3.lib
    ${PROJECT_SOURCE_DIR}/lib/OpenGL32.Lib
)