target_sources(trimesh2
PRIVATE
TriMesh_bounding.cc
TriMesh_connectivity.cc
TriMesh_curvature.cc
TriMesh_io.cc
TriMesh_grid.cc
TriMesh_normals.cc
TriMesh_pointareas.cc
TriMesh_stats.cc
TriMesh_tstrips.cc
GLCamera.cc
GLManager.cc
ICP.cc
KDtree.cc
conn_comps.cc
diffuse.cc
edgeflip.cc
faceflip.cc
filter.cc
make.cc
merge.cc
overlap.cc
remove.cc
reorder_verts.cc
subdiv.cc
umbrella.cc)

target_include_directories(trimesh2 PRIVATE
                           ${TRIMESH_INCLUDE_DIR}
                           INTERFACE
                           ${CMAKE_INSTALL_PREFIX}/include/trimesh2)

set(INSTALL_CONFIGDIR ${CMAKE_INSTALL_LIBDIR}/cmake/Trimesh2)
install(TARGETS trimesh2
        EXPORT Trimesh2Targets
        LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
        ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
        RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
        PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_PREFIX}/include/trimesh2
)

install(EXPORT Trimesh2Targets
    FILE Trimesh2Config.cmake
    NAMESPACE Trimesh2::
    DESTINATION ${INSTALL_CONFIGDIR}
)
#)
