cmake_minimum_required(VERSION "3.0.0")

project("TriMesh2")

set(TRIMESH_INCLUDE_DIR ${CMAKE_SOURCE_DIR}/include)

add_subdirectory(libsrc)
add_subdirectory(utilsrc)
