cmake_minimum_required(VERSION 2.8)
project(foo)

add_library(foo foo.cpp)

install(TARGETS foo DESTINATION lib)

# BAD CODE!
file(
    COPY
    "${CMAKE_CURRENT_LIST_DIR}/README"
    DESTINATION
    "${CMAKE_INSTALL_PREFIX}/share/foo"
)

include(CPack)
