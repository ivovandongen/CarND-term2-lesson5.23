cmake_minimum_required(VERSION 3.10)
project(CarND-term2-lesson5.23)

set(CMAKE_CXX_STANDARD 14)

include(deps/eigen.cmake)

if (UNIX)
    # Silence warnings in Eigen
    add_compile_options(-Wno-deprecated-register)
endif()



add_executable(RMSE
    ${CMAKE_SOURCE_DIR}/src/main.cpp
)

target_link_libraries(RMSE Eigen)
