project(std-browser CXX)
cmake_minimum_required(VERSION 3.10)

include_directories(include)

add_subdirectory(protocol)
add_subdirectory(html)
add_subdirectory(css)
add_subdirectory(ui)
add_subdirectory(file)
