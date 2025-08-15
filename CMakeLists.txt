cmake_minimum_required(VERSION 3.10)
project(Dualplay C)

# Find SDL2
find_package(SDL2 REQUIRED)

# Add executable
add_executable(DualPlay src/main.c)

# Link SDL2
target_include_directories(DualPlay PRIVATE ${SDL2_INCLUDE_DIRS})
target_link_libraries(DualPlay PRIVATE ${SDL2_LIBRARIES})
