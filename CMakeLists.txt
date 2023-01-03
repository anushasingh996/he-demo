cmake_minimum_required(VERSION 3.23)
project(untitled1 VERSION 1.0)
## Use -std=c++17 as default.
set(CMAKE_CXX_STANDARD 17)
## Disable C++ extensions
set(CMAKE_CXX_EXTENSIONS OFF)
## Require full C++ standard
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(helib_DIR /Users/anusha/helib_install/helib_pack/share/cmake/helib)

include_directories(.)
configure_file(./countries_dataset.csv ./countries_dataset.csv COPYONLY)
add_executable(untitled1 main.cpp)

find_package(helib 2.2.0 EXACT REQUIRED)

target_link_libraries(untitled1 helib)