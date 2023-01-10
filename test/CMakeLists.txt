# add my test executable
add_executable(my_unit_test test.c ${CMAKE_SOURCE_DIR}/hello.h ${CMAKE_SOURCE_DIR}/hello.c)

# add CMAKE_SOURCE_DIR to the target's include directory
target_include_directories(my_unit_test PRIVATE ${CMAKE_SOURCE_DIR})

# add my test to the list of unit tests
add_test(NAME my_unit_test COMMAND my_unit_test)