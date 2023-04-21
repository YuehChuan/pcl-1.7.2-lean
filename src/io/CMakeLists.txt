include_directories("/usr/include/eigen3")
include_directories("/home/ubuntu/pcl-1.7.2/thirdparty/boost")


set(build TRUE)
if(build)


    set(incs
        "include/pcl/io/boost.h"
        "include/pcl/io/eigen.h"
        "include/pcl/io/file_io.h"
        "include/pcl/io/io.h"
        "include/pcl/io/pcd_io.h"
        )

    set(srcs
        src/pcd_io.cpp
        src/file_io.cpp
        src/io_exception.cpp
        )

set(LIB_NAME "pcl_${SUBSYS_NAME}")

    include_directories("${CMAKE_CURRENT_SOURCE_DIR}/include" "/home/ubuntu/pcl-1.7.2/src/common/include")




add_library(
${PROJECT_NAME}.io SHARED 
 ${srcs} ${incs} ${COMMON_INCLUDES}
)

target_link_libraries(${PROJECT_NAME}.io ${PROJECT_NAME}.common)
 
endif(build)
