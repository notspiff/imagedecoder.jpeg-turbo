project(imageencoder.jpeg-turbo)

cmake_minimum_required(VERSION 2.6)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${PROJECT_SOURCE_DIR})

enable_language(CXX)

find_package(kodi REQUIRED)
find_package(JPEG REQUIRED)

include_directories(${KODI_INCLUDE_DIR})

set(JPEGTURBO_SOURCES src/JpegIO.cpp)

set(DEPLIBS ${JPEG_LIBRARIES})

build_addon(imageencoder.jpeg-turbo JPEGTURBO DEPLIBS)

include(CPack)
