cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

project(libSAR)

find_package( OpenCV REQUIRED )

set(CMAKE_LIBRARY_OUTPUT_DIRECTORY lib)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)

add_library(SAR SHARED src/ImwHelper.cc)

INSTALL_TARGETS(/lib SAR)
install(FILES include/ImwHelper.hh DESTINATION include COMPONENT headers)