cmake_minimum_required(VERSION 3.15)
project(MetalCppWindow LANGUAGES CXX OBJCXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_OBJCXX_STANDARD 17)
set(CMAKE_OBJCXX_STANDARD_REQUIRED ON)

add_subdirectory(metal-cpp)

add_executable(MetalCppWindow main.cpp)
target_link_libraries(MetalCppWindow PRIVATE 
    metal-cpp
)
target_include_directories(MetalCppWindow PRIVATE
    metal-cpp-extensions
)
