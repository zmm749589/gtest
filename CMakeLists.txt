cmake_minimum_required(VERSION 3.16.3)
project(hello_world)

enable_testing()

add_subdirectory(hello)
add_subdirectory(world)
# add_subdirectory(tests)

add_executable(main ${CMAKE_CURRENT_SOURCE_DIR}/main.cpp)
target_include_directories(main PUBLIC 
   ${CMAKE_CURRENT_SOURCE_DIR}/hello 
   ${CMAKE_CURRENT_SOURCE_DIR}/world
#    ${CMAKE_CURRENT_SOURCE_DIR}/tests
)
# 指定库文件搜索路径
target_link_directories(main PUBLIC
   ${CMAKE_CURRENT_SOURCE_DIR}/build/hello   
   ${CMAKE_CURRENT_SOURCE_DIR}/build/world
   # ${CMAKE_CURRENT_SOURCE_DIR}/build/tests
)
target_link_libraries(main PUBLIC hellolib worldlib)
