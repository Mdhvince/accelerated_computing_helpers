cmake_minimum_required(VERSION 3.5)

project(AccComputing VERSION 1.0.0)

add_definitions(-std=c++14)
set(CXX_FLAGS "-Wall")

find_package(OpenCV REQUIRED)
enable_language(CUDA)

set(EXECUTABLE app)
add_executable(${EXECUTABLE} vectorAdd.cu)

target_link_libraries(${EXECUTABLE} PRIVATE ${OpenCV_LIBS})