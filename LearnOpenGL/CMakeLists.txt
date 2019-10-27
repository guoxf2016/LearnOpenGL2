# CMakeList.txt: LearnOpenGL 的 CMake 项目，在此处包括源代码并定义
# 项目特定的逻辑。
#
cmake_minimum_required (VERSION 3.8)

find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
find_package(glfw3 CONFIG REQUIRED)


# 将源代码添加到此项目的可执行文件。
add_executable (LearnOpenGL "main.cpp" "glad.c" "shader.cpp")
target_link_libraries(LearnOpenGL PRIVATE OpenGL GLUT::GLUT glfw)

# TODO: 如有需要，请添加测试并安装目标。
