cmake_minimum_required(VERSION 3.8)
project(encrypter)

set(CMAKE_C_STANDARD 99)

set(SOURCE_FILES encrypter.c encrypter.h ioctl.c)
add_executable(encrypter ${SOURCE_FILES})
