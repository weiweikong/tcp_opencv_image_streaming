cmake_minimum_required(VERSION 2.8)
project( tcp_opencv_transfer )
find_package( OpenCV REQUIRED )
add_executable( server server.cpp )
target_link_libraries( server -lpthread ${OpenCV_LIBS} )
add_executable( client client.cpp )
target_link_libraries( client -lpthread ${OpenCV_LIBS} )