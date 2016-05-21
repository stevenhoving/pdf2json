add_executable(pdf2json
    XmlFonts.cc
    XmlLinks.cc
    ImgOutPutDev.cc
    pdf2json.cc
)

if(MSVC)
  add_definitions(
    -D_CRT_SECURE_NO_WARNINGS
  )
endif(MSVC)

target_link_libraries(pdf2json
    goo
    xpdf
    fofi
    splash
)




