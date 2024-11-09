cmake_minimum_required(VERSION 3.27)

project(musicMan)

set(CMKAE_BUILD_TYPE debug)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
    #I dont think ill ever use Clang, but hey more portable i guess (?)
    add_compile_options(-g -O0 -Wall -Wextra -Wpedantic)
endif()

add_executable(${PROJECT_NAME} main.c)

include_directories(${CMAKE_CURRENT_SOURCE_DIR})

add_subdirectory(src)

target_link_libraries(${PROJECT_NAME} PRIVATE manager)
