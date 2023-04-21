include_directories("/usr/include/eigen3")
include_directories("/home/ubuntu/pcl-1.7.2/thirdparty/boost")
include_directories("/home/ubuntu/pcl-1.7.2/src/common/include")

set(SUBSYS_NAME filters)
set(build TRUE)
if(build)

    set(srcs
        src/voxel_grid.cpp
        )

    set(incs
        "include/pcl/${SUBSYS_NAME}/boost.h"
        "include/pcl/${SUBSYS_NAME}/voxel_grid.h"
        )

    set(impl_incs
        "include/pcl/${SUBSYS_NAME}/impl/voxel_grid.hpp"
        )

    include_directories("${CMAKE_CURRENT_SOURCE_DIR}/include" )


add_library(
${PROJECT_NAME}.filter SHARED 
 ${srcs} ${incs} 
)

target_link_libraries(${PROJECT_NAME}.filter ${PROJECT_NAME}.common)
 
endif(build)
