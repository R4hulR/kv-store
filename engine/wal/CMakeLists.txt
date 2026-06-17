cmake_minimum_required(VERSION 4.2.3)

project(kv_store_wal)

set(CMAKE_CXX_STANDARD 17)

add_library(wal_lib src/wal.cpp)

target_include_directories(wal_lib PUBLIC include)

add_executable(kv_store_wal src/main.cpp)

target_link_libraries(kv_store_wal PRIVATE wal_lib)