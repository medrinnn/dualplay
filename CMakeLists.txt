cmake_minimum_required(VERSION 3.10)
project(DualPlay C)

# Find SDL2
find_package(SDL2 REQUIRED)

# Add executable
add_executable(DualPlay main.c)

# Link SDL2
target_include_directories(dualplay PRIVATE ${SDL2_INCLUDE_DIRS})
target_link_libraries(dualplay PRIVATE ${SDL2_LIBRARIES})
