cmake_minimum_required(VERSION 3.12)
project(untitled2 C)

set(CMAKE_C_STANDARD 99)
#首先定义两个变量INC_DIR和LINK_DIR，用来表示头文件路径和库的路径：
set(INC_DIR /usr/local/include)
set(LINK_DIR /usr/local/lib64)
#然后依次设置头文件目录、库目录、要链接的库：
include_directories(${INC_DIR})
link_directories(${LINK_DIR})
link_libraries(libssl.so libcrypto.so)

add_executable(untitled2 main.c)
#使用如下语句完成库的链接操作：
target_link_libraries(untitled2 libssl.so libcrypto.so)