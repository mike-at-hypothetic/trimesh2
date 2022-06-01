
set(Trimesh2_HEADERS
Box.h
Color.h
GLCamera.h
GLManager.h
ICP.h
KDtree.h
TriMesh_algo.h
TriMesh.h
Vec.h
XForm.h
bsphere.h
endianutil.h
lineqn.h
mathcompat.h
mathutil.h
noise3d.h
strutil.h
timestamp.h
)

install(FILES ${Trimesh2_HEADERS}
        DESTINATION include/trimesh2)

install(FILES GL/glui.h
        DESTINATION include)