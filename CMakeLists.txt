
cmake_minimum_required(VERSION 2.8)
project( dhvani )

set(PROJECT_ROOT ${PROJECT_SOURCE_DIR})

add_definitions(-DUSING_CMAKE)
add_definitions(-DVERSION="0.95")

include_directories(AFTER "/usr/include/gstreamer-1.0")
include_directories(AFTER "/usr/include/glib-2.0")
include_directories(AFTER "/usr/lib/glib-2.0/include")

file(GLOB DHVANI_SRC
    "src/*.h"
    "src/*.c"
    "*/.h"
)

include_directories(AFTER ${PROJECT_ROOT})

add_executable( ${PROJECT_NAME} ${DHVANI_SRC} )

target_link_libraries(${PROJECT_NAME} asound)
target_link_libraries(${PROJECT_NAME} gstreamer-1.0)
target_link_libraries(${PROJECT_NAME} gobject-2.0)
target_link_libraries(${PROJECT_NAME} glib-2.0)
target_link_libraries(${PROJECT_NAME} gsm)

target_link_libraries(${PROJECT_NAME} pthread)
target_link_libraries(${PROJECT_NAME} m)