# Set CMake min version
cmake_minimum_required(VERSION 2.8.12)

# Set project name
project(CMakeApp)

# Set compiler version and flags
set(CMAKE_CXX_STANDART 11)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall")

# Generate SHARED library
add_library(SharedLibrary SHARED Library/library.cpp)
target_include_directories(SharedLibrary PUBLIC ${PROJECT_SOURCE_DIR})

# Add all C++ files
file(GLOB CPPS "*.cpp")

# Create executable file
add_executable(${PROJECT_NAME} ${CPPS})

# Link library with binary target
target_link_libraries(${PROJECT_NAME} PRIVATE SharedLibrary)