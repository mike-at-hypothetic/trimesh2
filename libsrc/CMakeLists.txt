include(GNUInstallDirs)

add_library("trimesh2" 	TriMesh_bounding.cc
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

target_include_directories("trimesh2" PUBLIC ${TRIMESH_INCLUDE_DIR})

install(TARGETS trimesh2
        LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
        ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
        RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)
