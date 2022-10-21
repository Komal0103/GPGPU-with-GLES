cmake_minimum_required(VERSION 3.7)
project(GPGPUGLESMatrixTranspose VERSION 1.0)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

find_package(GPGPU_GLES REQUIRED)

add_executable(GPGPUGLESMatrixTranspose
        ${CMAKE_CURRENT_LIST_DIR}/mat_transpose.c)

target_link_libraries(GPGPUGLESMatrixTranspose PRIVATE GPGPU_GLES::GPGPU_GLES)
