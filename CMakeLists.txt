cmake_minimum_required(VERSION 3.0)

project(microsocks)

# source
include_directories(${CMAKE_CURRENT_SOURCE_DIR})
set     (HEADERS
        sblist.h
        )
set     (SOURCES
        sblist.c
        sblist_delete.c
        server.c
        sockssrv.c
        )

# main
add_executable(${PROJECT_NAME}
        ${HEADERS}
        ${SOURCES}
        )

target_link_libraries(${PROJECT_NAME} pthread)