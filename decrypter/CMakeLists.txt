cmake_minimum_required(VERSION 3.8)
project(decrypter)

set(CMAKE_C_STANDARD 99)

set(SOURCE_FILES decrypter.c decrypter.h ioctl.c)
add_executable(decrypter ${SOURCE_FILES})
