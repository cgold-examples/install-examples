cmake_minimum_required(VERSION 2.8)
project(foo)

add_library(foo foo.cpp)

install(TARGETS foo DESTINATION lib)
install(FILES README DESTINATION share/foo)

include(CPack)
