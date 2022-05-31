include(GNUInstallDirs)

set(trimesh_UTIL_PROGS "")
macro(util_prog util_name)
    add_executable(${util_name} ${util_name}.cc)
    target_include_directories(${util_name} PUBLIC ${TRIMESH_INCLUDE_DIR})
    target_link_libraries(${util_name} PUBLIC libtrimesh2)
    list(APPEND trimesh_UTIL_PROGS ${util_name})
endmacro()

util_prog(mesh_cat)
util_prog(mesh_cc)
util_prog(mesh_check)
util_prog(mesh_crunch)
util_prog(mesh_filter)
util_prog(mesh_hf)
util_prog(mesh_info)
util_prog(mesh_make)
util_prog(mesh_shade)
util_prog(grid_subsamp)
util_prog(xf)

install(TARGETS ${trimesh_UTIL_PROGS}
        LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
        ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
        RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)
