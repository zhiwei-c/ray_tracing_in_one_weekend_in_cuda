cmake_minimum_required(VERSION 3.9)

if(NOT DEFINED CMAKE_CUDA_STANDARD)
    set(CMAKE_CUDA_STANDARD 17)
    set(CMAKE_CUDA_STANDARD_REQUIRED ON)
endif()

if(NOT DEFINED CMAKE_CXX_STANDARD)
    set(CMAKE_CXX_STANDARD 17)
    set(CMAKE_CXX_STANDARD_REQUIRED ON)
endif()

if(NOT DEFINED CMAKE_CUDA_ARCHITECTURES)
  set(CMAKE_CUDA_ARCHITECTURES 75)
endif()

project(ray_tracing_in_one_weekend_in_cuda LANGUAGES CUDA CXX)

set(01_output ${PROJECT_SOURCE_DIR}/01_output)
add_subdirectory(01_output)

set(02_vec3 ${PROJECT_SOURCE_DIR}/02_vec3)
add_subdirectory(02_vec3)

set(03_rays ${PROJECT_SOURCE_DIR}/03_rays)
add_subdirectory(03_rays)

set(04_sphere ${PROJECT_SOURCE_DIR}/04_sphere)
add_subdirectory(04_sphere)

set(05_normals ${PROJECT_SOURCE_DIR}/05_normals)
add_subdirectory(05_normals)

set(06_antialiasing ${PROJECT_SOURCE_DIR}/06_antialiasing)
add_subdirectory(06_antialiasing)

set(07_diffuse ${PROJECT_SOURCE_DIR}/07_diffuse)
add_subdirectory(07_diffuse)

set(08_metal ${PROJECT_SOURCE_DIR}/08_metal)
add_subdirectory(08_metal)

set(09_dielectrics ${PROJECT_SOURCE_DIR}/09_dielectrics)
add_subdirectory(09_dielectrics)

set(10_camera ${PROJECT_SOURCE_DIR}/10_camera)
add_subdirectory(10_camera)

set(11_defocus_blur ${PROJECT_SOURCE_DIR}/11_defocus_blur)
add_subdirectory(11_defocus_blur)

set(12_where_next ${PROJECT_SOURCE_DIR}/12_where_next)
add_subdirectory(12_where_next)