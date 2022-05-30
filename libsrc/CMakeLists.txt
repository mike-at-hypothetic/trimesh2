add_library("libtrimesh2" 	TriMesh_bounding.cc
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

target_include_directories("libtrimesh2" PUBLIC ${TRIMESH_INCLUDE_DIR})