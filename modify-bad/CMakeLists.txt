cmake_minimum_required(VERSION 2.8)
project(foo)

set(CMAKE_INSTALL_PREFIX "${CMAKE_CURRENT_BINARY_DIR}/3rdParty/root") # BAD CODE!

add_library(foo foo.cpp)

install(TARGETS foo DESTINATION lib)
