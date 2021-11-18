cmake_minimum_required(VERSION 3.12)

# include($ENV{PICO_SDK_PATH}/external/pico_sdk_import.cmake)

project(pico-lisp 
    LANGUAGES C ASM 
    VERSION 0.1 
    DESCRIPTION "A tiny Lisp interpreter for Raspberry Pi Pico")

set(CMAKE_C_STANDARD 11)

add_executable(pico-lisp
    pico-lisp.c
)
