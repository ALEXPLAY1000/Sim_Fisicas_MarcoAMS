cmake_minimum_required(VERSION 3.26)
project(joins_Distancia_Marco)

set(CMAKE_CXX_STANDARD 17)

add_executable(joins_Distancia_Marco rueda_marco.cpp)
find_package(box2d CONFIG REQUIRED)
target_link_libraries(joins_Distancia_Marco PRIVATE box2d::box2d)

find_package(SFML COMPONENTS system window graphics CONFIG REQUIRED)
target_link_libraries(joins_Distancia_Marco PRIVATE sfml-system sfml-network sfml-graphics sfml-window)