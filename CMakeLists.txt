cmake_minimum_required(VERSION 3.15)
project(HelloSFML)

set(CMAKE_CXX_STANDARD 14)
add_executable(HelloSFML main.cpp)

include_directories(/usr/local/include)

find_package(SFML 2.5 COMPONENTS system window graphics network audio REQUIRED)
include_directories(${SFML_INCLUDE_DIRS})
target_link_libraries(HelloSFML sfml-system sfml-window sfml-graphics sfml-audio sfml-network)
