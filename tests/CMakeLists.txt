cmake_minimum_required(VERSION 3.8)

include_directories(../libleaktracer)

aux_source_directory(. main_src)

add_executable(test ${main_src})

add_dependencies(test leaktracer)

target_link_libraries(test PRIVATE leaktracer pthread dl)