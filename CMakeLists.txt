cmake_minimum_required(VERSION 3.17)
project(Ceres_lrn)

set(CMAKE_CXX_STANDARD 14)
include_directories("/usr/include/eigen3")

find_package(Ceres REQUIRED)
include_directories(${CERES_INCLUDE_DIRS})

add_executable(main src/main.cpp)
target_link_libraries(main ${CERES_LIBRARIES})

add_executable(Curve_Fitting src/Curve_Fitting.cpp)
target_link_libraries(Curve_Fitting ${CERES_LIBRARIES})

add_executable(Bundle_Adjustment src/Bundle_Adjustment.cpp)
target_link_libraries(Bundle_Adjustment ${CERES_LIBRARIES})
