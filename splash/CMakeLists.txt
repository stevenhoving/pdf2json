cmake_minimum_required(VERSION 3.3)
project(splash)

add_library(splash
    Splash.cc
    SplashBitmap.cc
    SplashClip.cc
    SplashFTFont.cc
    SplashFTFontEngine.cc
    SplashFTFontFile.cc
    SplashFont.cc
    SplashFontEngine.cc
    SplashFontFile.cc
    SplashFontFileID.cc
    SplashPath.cc
    SplashPattern.cc
    SplashScreen.cc
    SplashState.cc
    SplashT1Font.cc
    SplashT1FontEngine.cc
    SplashT1FontFile.cc
    SplashXPath.cc
    SplashXPathScanner.cc
)

if(MSVC)
  add_definitions(
    -D_CRT_SECURE_NO_WARNINGS
  )
endif(MSVC)

target_link_libraries(splash
    goo
)

target_include_directories(splash
    PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}
)

