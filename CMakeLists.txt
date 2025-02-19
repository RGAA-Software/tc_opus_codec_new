set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include_directories(${CMAKE_CURRENT_SOURCE_DIR})
include_directories(${CMAKE_SOURCE_DIR}/tc_message_new)
include_directories(${CMAKE_SOURCE_DIR}/tc_3rdparty/)
include_directories(${CMAKE_SOURCE_DIR}/tc_3rdparty/eventbus/src)

set(OPUS_SRCS opus_codec.cpp)

add_library(tc_opus_codec_new ${OPUS_SRCS} ${EXT_SRCS})
target_link_libraries(tc_opus_codec_new tc_common_new Opus::opus)