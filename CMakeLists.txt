
cmake_minimum_required(VERSION 2.8)
project( dhavni )

file(GLOB DHVANI_SRC
    "src/*.h"
    "src/*.c"
)

# find_package( OpenCV REQUIRED )
add_executable( ${PROJECT_NAME} ${DHVANI_SRC} )
# target_link_libraries( DisplayImage ${OpenCV_LIBS})