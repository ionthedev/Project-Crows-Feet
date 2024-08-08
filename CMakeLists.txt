cmake_minimum_required(VERSION 3.14)
project(FS-Phantom)

# Set C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Set the build directory for phantom-engine
set(PHANTOM_ENGINE_BUILD_DIR ${CMAKE_SOURCE_DIR}/PhantomEngine/cmake-build-debug)
set(FEAR_THE_CROW_BUILD_DIR ${CMAKE_SOURCE_DIR}/Fear-The-Crow/cmake-build-debug)

# Add the phantom-engine subdirectory
add_subdirectory(PhantomEngine ${PHANTOM_ENGINE_BUILD_DIR})

# Add the Fear-the-Crow subdirectory
add_subdirectory(Fear-The-Crow ${FEAR_THE_CROW_BUILD_DIR})


target_link_libraries(Fear-The-Crow PhantomEngine)