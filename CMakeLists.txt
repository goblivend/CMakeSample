cmake_minimum_required(VERSION 3.21.2)

project(libfoo)

add_library(libfoo SHARED)

add_subdirectory(src)
target_include_directories(libfoo PUBLIC include)

add_subdirectory(test)


target_compile_options(libfoo PRIVATE -Wall -Wextra -Werror -pedantic -std=c++20)

set_target_properties(libfoo PROPERTIES 
    CXX_STANDARD 20
    CXX_EXTENSIONS OFF
    OUTPUT_NAME foo
)
