# Copyright mzoesch. All rights reserved.

# Update to 4.0 when CLion supports it.
cmake_minimum_required(VERSION      3.30)

# C++23 is required; core Jafg systems will not compile with any other standard.
set(CMAKE_CXX_STANDARD              23)
set(CMAKE_CXX_STANDARD_REQUIRED     ON)
set(CMAKE_CXX_EXTENSIONS            OFF)

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
    PUBLIC
    "Source/Public"
    )
