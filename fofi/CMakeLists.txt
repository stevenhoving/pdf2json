cmake_minimum_required(VERSION 3.3)
project(fofi)

add_library(fofi
    FoFiBase.cc
    FoFiEncodings.cc
    FoFiTrueType.cc
    FoFiType1.cc
    FoFiType1C.cc
)

if(MSVC)
  add_definitions(
    -D_CRT_SECURE_NO_WARNINGS
  )
endif(MSVC)

target_link_libraries(fofi
    goo
)

target_include_directories(fofi
    PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}
)

