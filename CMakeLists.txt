cmake_minimum_required(VERSION 3.15)

project(magnum)

set(CMAKE_CXX_STANDARD 14)

find_package(Corrade REQUIRED Main)
find_package(Magnum REQUIRED GL Sdl2Application)

set_directory_properties(PROPERTIES CORRADE_USE_PEDANTIC_FLAGS ON)

add_executable(magnum WIN32 MyApplication.cpp)
target_link_libraries(magnum PRIVATE Magnum::Application Magnum::GL
                                     Magnum::Magnum)
