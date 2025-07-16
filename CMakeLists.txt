# Copyright mzoesch. All rights reserved.

# Update to 4.0 when CLion supports it.
cmake_minimum_required(VERSION      3.30)

project(
    sqlite3_amalgamation
    VERSION         1.0
    LANGUAGES       C
    DESCRIPTION     ""
    HOMEPAGE_URL    "https://github.com/mzoesch/S-Jafg"
    )

add_library(
    jafg_sqlite3_amalgamation
    STATIC
    "Source/Private/sqlite3.c"
    "Source/Public/sqlite3.h"
    )

target_include_directories(
    jafg_sqlite3_amalgamation
    INTERFACE
    "Source/Public"
    )
