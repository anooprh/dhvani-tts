
cmake_minimum_required(VERSION 2.8)
project( dhavni )

set(PROJECT_ROOT ${PROJECT_SOURCE_DIR})

file(GLOB DHVANI_SRC
    "src/*.h"
    "src/*.c"
    "*/.h"
)

include_directories(AFTER ${PROJECT_ROOT})

# find_package( OpenCV REQUIRED )
add_executable( ${PROJECT_NAME} ${DHVANI_SRC} )
# target_link_libraries( DisplayImage ${OpenCV_LIBS})