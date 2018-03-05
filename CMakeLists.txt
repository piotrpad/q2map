cmake_minimum_required(VERSION 2.8)
project(q2map)

set(SOURCES
 common/bspfile.c
 common/cmdlib.c
 common/inout.c
 common/l3dslib.c
 common/lbmlib.c
 common/mathlib.c
 common/path_init.c
 common/polylib.c
 common/scriplib.c
 common/threads.c
 common/trilib.c
 common/l_net/l_net_berkeley.c
 common/l_net/l_net.c
 q2map/brushbsp.c
 q2map/csg.c
 q2map/faces.c
 q2map/flow.c
 q2map/glfile.c
 q2map/leakfile.c
 q2map/lightmap.c
 q2map/main.c
 q2map/map.c
 q2map/nodraw.c
 q2map/patches.c
 q2map/portals.c
 q2map/prtfile.c
 q2map/qbsp.c
 q2map/qrad.c
 q2map/qvis.c
 q2map/textures.c
 q2map/trace.c
 q2map/tree.c
 q2map/writebsp.c
)
find_package(LibXml2)
include_directories("common" "common/l_net"  "/usr/include/libxml2" "../../include" "../../libs")
add_executable(q2map.bin ${SOURCES})
target_link_libraries(q2map.bin ${LIBXML2_LIBRARIES} pthread m)


