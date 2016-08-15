# Top-level CMakeLists.txt

cmake_minimum_required(VERSION 2.8)
project(foo)

set(script "${CMAKE_CURRENT_BINARY_DIR}/script.cmake")
configure_file(script.cmake.in "${script}" @ONLY)

install(SCRIPT "${script}")

include(CPack)
