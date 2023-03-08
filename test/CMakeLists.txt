cmake_minimum_required(VERSION 3.21.2)

project(libfoo)


add_executable(test)
add_subdirectory(src)

target_compile_options(test PRIVATE -Wall -Wextra -Werror -pedantic -std=c++20)

target_link_libraries(test PRIVATE libfoo)



set_target_properties(test PROPERTIES 
    CXX_STANDARD 20
    CXX_EXTENSIONS OFF
)
