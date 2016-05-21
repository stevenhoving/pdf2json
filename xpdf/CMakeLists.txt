cmake_minimum_required(VERSION 3.3)
project(xpdf)

add_library(xpdf
    Annot.cc
    Array.cc
    BuiltinFont.cc
    BuiltinFontTables.cc
    CMap.cc
    Catalog.cc
    CharCodeToUnicode.cc
    Decrypt.cc
    Dict.cc
    Error.cc
    FontEncodingTables.cc
    Function.cc
    Gfx.cc
    GfxFont.cc
    GfxState.cc
    GlobalParams.cc
    JArithmeticDecoder.cc
    JBIG2Stream.cc
    JPXStream.cc
    Lexer.cc
    Link.cc
    PSTokenizer.cc
    NameToCharCode.cc
    Object.cc
    Outline.cc
    OutputDev.cc
    PDFDoc.cc
    PDFDocEncoding.cc
    PSOutputDev.cc
    PSTokenizer.cc
    Page.cc
    Parser.cc
    PreScanOutputDev.cc
    Stream.cc
    SplashOutputDev.cc
    UnicodeMap.cc
    SecurityHandler.cc
    UnicodeTypeTable.cc
    XRef.cc
)

if(MSVC)
  add_definitions(
    -D_CRT_SECURE_NO_WARNINGS
  )
endif(MSVC)

target_link_libraries(xpdf
    goo
    fofi
    splash
)

target_include_directories(xpdf
    PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}
)

