cmake_minimum_required(VERSION 3.10)  # Adjust version as needed
project(ProjectCrowsFeet)

option(TOP_LEVEL "Build from top" ON)

# Set the C++ standard for the whole project
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Add subdirectories for PhantomEngine and FearTheCrow
add_subdirectory(phantom-engine)
add_subdirectory(Fear-the-Crow)
add_subdirectory(phantom-works)

#target_link_libraries(ProjectCrowsFeet PRIVATE PhantomEngine PhantomWorks FearTheCrow)