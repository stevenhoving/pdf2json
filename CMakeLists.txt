cmake_minimum_required(VERSION 3.4)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)
set(CMAKE_CONFIGURATION_TYPES Debug Release CACHE TYPE INTERNAL FORCE)



#add_definitions(
#  -D_GNU_SOURCE
#  -DGST_DISABLE_DEPRECATED
#  -DHAVE_CONFIG_H
#  -DGST_EXPORTS
#)

include_directories(
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${CMAKE_CURRENT_BINARY_DIR}
)

if(MSVC)
  add_definitions(
    -D_CRT_SECURE_NO_WARNINGS
  )
endif(MSVC)

add_subdirectory(goo)
add_subdirectory(splash)
add_subdirectory(fofi)
add_subdirectory(xpdf)

project(pdf2json)

#MESSAGE( STATUS "generate gstconfig.h")
#configure_file(
#  ${CMAKE_CURRENT_SOURCE_DIR}/gst/gstconfig.h.in
#  ${CMAKE_CURRENT_BINARY_DIR}/gst/gstconfig.h
#)




add_subdirectory(src)