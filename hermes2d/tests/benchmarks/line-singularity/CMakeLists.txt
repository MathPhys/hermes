if(NOT H2D_REAL)
    return()
endif(NOT H2D_REAL)
project(benchmark-line-singularity)

add_executable(${PROJECT_NAME} main.cpp)
include (../../CMake.common)

set(BIN ${PROJECT_BINARY_DIR}/${PROJECT_NAME})
add_test(benchmark-line-singularity ${BIN})
set_tests_properties(benchmark-line-singularity PROPERTIES LABELS slow)
