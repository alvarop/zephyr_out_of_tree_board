# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.13.1)
# Re-direct the directory where the 'boards' directory is found from
# $ZEPHYR_BASE to this directory.
set(BOARD_ROOT ${CMAKE_CURRENT_LIST_DIR})

# This sample is only compatible with new_board because it has
# re-directed the 'boards' directory to a directory that only contains
# this board.
set(BOARD new_board)

find_package(Zephyr HINTS $ENV{ZEPHYR_BASE})
project(out_of_tree_board)

target_sources(app PRIVATE src/main.c)
