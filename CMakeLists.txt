cmake_minimum_required(VERSION 3.10)

# set the project name
project(my_ctest)

# add the executable
add_executable(hello main.c hello.c)

# enable unit tests
include(CTest)
enable_testing()

# add test directory
add_subdirectory(test)
