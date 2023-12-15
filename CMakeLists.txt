cmake_minimum_required(VERSION 3.16)
project(actions-msvc-asan-bug
    LANGUAGES CXX
)
add_executable(repro main.cpp)
target_compile_options(repro PRIVATE -fsanitize=address)
add_custom_target(run-repro COMMAND repro)
