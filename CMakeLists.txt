cmake_minimum_required(VERSION 3.5) 
project(demuxingtest)
find_package( OpenCV REQUIRED )
include_directories("/usr/local/include")
LINK_DIRECTORIES("/usr/local/lib")
add_executable( demuxingtest demuxing_decoding.c )
target_link_libraries(demuxingtest ${OpenCV_LIBS} libavutil.so libavcodec.so libavformat.so)

