cmake_minimum_required(VERSION 3.9)
project(distort)

set(CMAKE_CXX_STANDARD 11)


# 寻找OpenCV库
find_package( OpenCV REQUIRED )
# 添加头文件
include_directories( ${OpenCV_INCLUDE_DIRS} )


add_executable(distort
        undistort_image.cpp)
target_link_libraries( distort ${OpenCV_LIBS} )