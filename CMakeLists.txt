cmake_minimum_required(VERSION 3.12)

include($ENV{PICO_SDK_PATH}/external/pico_sdk_import.cmake)

project(pico-lisp 
    LANGUAGES C ASM 
    VERSION 0.1 
    DESCRIPTION "A tiny Lisp interpreter for Raspberry Pi Pico")

set(CMAKE_C_STANDARD 11)

add_executable(pico-lisp
    pico-lisp.c
)

target_link_libraries(${CMAKE_PROJECT_NAME}
  pico_stdlib
  hardware_i2c
  oled
)

pico_enable_stdio_uart(${CMAKE_PROJECT_NAME} 1)
pico_enable_stdio_usb(${CMAKE_PROJECT_NAME} 0)
pico_add_extra_outputs(${CMAKE_PROJECT_NAME})
