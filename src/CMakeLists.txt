
project(manager)

set(PROJECT_SOURCES test.c)

add_library(manager STATIC ${PROJECT_SOURCES})

target_include_directories(${PROJECT_NAME} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR})

