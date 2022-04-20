cmake_minimum_required(VERSION 3.9)

set(PROJECT_NAME "11_defocus_blur")

project(${PROJECT_NAME})

file(GLOB gpu_source_files "${PROJECT_SOURCE_DIR}/src/*.*")

add_executable(${PROJECT_NAME} ${gpu_source_files})

set_property(DIRECTORY PROPERTY VS_STARTUP_PROJECT ${PROJECT_NAME})