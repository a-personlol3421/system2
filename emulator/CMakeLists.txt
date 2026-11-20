cmake_minimum_required(VERSION 3.25)

project(sy2emulator LANGUAGES C)

set(CMAKE_C_STANDARD 23)
set(CMAKE_C_STANDARD_REQUIRED ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

add_executable(sy2emulator
  src/main.c
  src/cpu.c
)

target_include_directories(sy2emulator PRIVATE src)
target_compile_options(sy2emulator PRIVATE -Wall -Wextra -Wpedantic -Werror)
