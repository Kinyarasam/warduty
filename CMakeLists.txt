cmake_minimum_required(VERSION 3.10)
project(warduty)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 17)

# Find SDL2
find_package(SDL2 REQUIRED)


# Include directories
include_directories(include ${SDL2_INCLUDE_DIRS})

# Source files
file(GLOB SOURCES src/*.cpp src/*/*.cpp)

# Specify the output directory for the executable
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)

# Add the executable
add_executable(warduty ${SOURCES})

# Add SDL2 to the linker
target_link_libraries(warduty ${SDL2_LIBRARIES})
