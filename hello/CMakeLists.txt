cmake_minimum_required(VERSION 3.16.3)
project(hello)

set(HELLO_SRC ${CMAKE_CURRENT_SOURCE_DIR}/hello.cpp
              ${CMAKE_CURRENT_SOURCE_DIR}/hello1.cpp)

# 生成的库文件存储在build/hello下
add_library(hellolib SHARED ${HELLO_SRC})