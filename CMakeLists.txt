cmake_minimum_required (VERSION 3.8)
project(mapnik_c)

include_directories(${DEPS_ROOT}/include)
include_directories(${DEPS_ROOT}/mapnik/include)


link_directories(${DEPS_ROOT}/lib)


set(SRC ${CMAKE_CURRENT_SOURCE_DIR}/mapnik_c_api.cpp)


add_library(libmapnik_c ${SRC})
target_link_libraries(libmapnik_c libmapnik)