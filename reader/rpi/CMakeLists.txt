cmake_minimum_required(VERSION 2.8.9)
project(reader)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS}")

set(SOURCE_FILES main.cpp rs232.c f_reader_commands.cpp f_reader_commands.h sqlite3.c sqlite3.h)
add_executable(reader ${SOURCE_FILES})

find_package( Threads REQUIRED )
target_link_libraries (reader ${CMAKE_THREAD_LIBS_INIT} ${CMAKE_DL_LIBS})
