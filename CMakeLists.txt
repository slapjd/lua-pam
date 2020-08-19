cmake_minimum_required(VERSION 3.15)
project(lua_pam)

set(CMAKE_CXX_STANDARD 14)
set(SOURCE_DIR src)

include_directories(/usr/include/luajit-2.0)

add_library(lua_pam SHARED ${SOURCE_DIR}/main.cpp)
target_link_libraries(lua_pam luajit-5.1 pam)