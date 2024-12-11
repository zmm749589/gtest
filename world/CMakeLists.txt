cmake_minimum_required(VERSION 3.16.3)
project(world)

set(WORLD_SRC ${CMAKE_CURRENT_SOURCE_DIR}/world.cpp)

# 生成的库文件存储在build/world下
add_library(worldlib SHARED ${WORLD_SRC})