cmake_minimum_required(VERSION 3.3 FATAL_ERROR)
project(parametric_plasma_source)

find_package(PugiXML REQUIRED)

include(parametric_plasma_source/CMakeLists.txt)
include(tests/src/CMakeLists.txt)

include_directories(${PUGIXML_INCLUDE_DIRS})
link_directories(${PUGIXML_LIBRARY_DIRS})
target_link_libraries(source_sampling ${PUGIXML_LIBRARIES})

