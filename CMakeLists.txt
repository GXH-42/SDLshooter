#标题
cmake_minimum_required(VERSION 3.10.0)
project(SDLshooter VERSION 0.1.0 LANGUAGES C CXX)

#查找并载入CMAKE预设
find_package(SDL2 REQUIRED)

#设置编译器
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)
#设置编译选项
add_compile_options(/W4)

#设置编译输出目录
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_DEBUG ${CMAKE_SOURCE_DIR})
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_RELEASE ${CMAKE_SOURCE_DIR})


# windows平台下
#if(win32)
#include_directories("E:/Game/Library/SDL2/include")
#link_directories("E:/Game/Library/SDL2/lib/x64")
# linux平台下
#else if(UNIX)
#include_directories("/usr/local/include/SDL2")
#link_directories("/usr/local/lib") 
# mac平台下
#else if(APPLE)
#include_directories("/usr/local/include/SDL2")
#link_directories("/usr/local/lib")
#endif()

#添加可执行文件
add_executable(SDLshooter main.cpp)

#链接库
target_link_libraries(SDLshooter SDL2::SDL2main SDL2::SDL2)
