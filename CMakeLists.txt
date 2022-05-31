cmake_minimum_required(VERSION "3.22.0")

include(GNUInstallDirs)

project(TriMesh2)

set(TRIMESH_INCLUDE_DIR ${CMAKE_SOURCE_DIR}/include)

add_library(trimesh2 "")

add_subdirectory(include)
add_subdirectory(libsrc)
add_subdirectory(utilsrc)
