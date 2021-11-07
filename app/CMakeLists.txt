cmake_minimum_required(VERSION 3.13.1)

#set(CONFIG_APPLICATION_DEFINED_SYSCALL true)
#list(APPEND BOARD_ROOT ${CMAKE_SOURCE_DIR})
#list(APPEND DTS_ROOT ${CMAKE_SOURCE_DIR})

# Add our custom Zephyr module for drivers w/ syscalls, etc.
#list(APPEND DTS_ROOT ${CMAKE_SOURCE_DIR}/drivers/zephyr)

#list(APPEND ZEPHYR_EXTRA_MODULES
#  ${CMAKE_CURRENT_SOURCE_DIR}/drivers
#)

# Find Zephyr. This also loads Zephyr's build system.
find_package(Zephyr REQUIRED HINTS zephyr)
project(philomena-clock-os)
target_include_directories(app PRIVATE include)

target_sources(app PRIVATE src/main.c)
