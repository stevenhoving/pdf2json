cmake_minimum_required(VERSION 3.3)
project(goo)

add_library(goo
    GHash.cc
    GList.cc
    GString.cc
    gmempp.cc
    gfile.cc
    gmem.cc
    parseargs.c
)

if(MSVC)
  add_definitions(
    -D_CRT_SECURE_NO_WARNINGS
  )
endif(MSVC)

target_include_directories(goo
    PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}
)

