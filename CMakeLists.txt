CMAKE_MINIMUM_REQUIRED(VERSION 2.6.2)
PROJECT(gpujpeg)

# CUDA
find_package(CUDA REQUIRED)
include_directories(${CUDA_INCLUDE_DIRS})

include_directories("${CMAKE_CURRENT_SOURCE_DIR}") #include libgpujpeg
ADD_SUBDIRECTORY(src)


# Install Rules
install(DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/libgpujpeg/" DESTINATION "libgpujpeg")