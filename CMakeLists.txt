find_package(Opus CONFIG REQUIRED)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include_directories(${CMAKE_CURRENT_SOURCE_DIR})
include_directories(${CMAKE_SOURCE_DIR}/deps)

aux_source_directory(. OPUS_SRCS)

add_library(opus_codec ${OPUS_SRCS} ${EXT_SRCS}) 
target_link_libraries(opus_codec common Opus::opus)