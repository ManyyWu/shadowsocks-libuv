cmake_minimum_required(VERSION 3.15)

project(ss-libuv)

add_subdirectory(libuv)

set(SRC encrypt.c md5.c server.c tests.c utils.c)
include_directories(libuv/include)

add_executable(ss-libuv ${SRC})
target_link_libraries(ss-libuv uv_a)
