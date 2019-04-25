cmake_minimum_required(VERSION 3.10)
project(GraphBLAS)

set(CMAKE_C_STANDARD 11)

link_directories(/usr/local/lib64)

set(SOURCES
        src/utils.cpp
        src/graphio.cpp)

include_directories(include)
link_libraries(graphblas)

add_executable(lcc src/algorithms/lcc.cpp ${SOURCES})
add_executable(bfs src/algorithms/bfs.cpp ${SOURCES})