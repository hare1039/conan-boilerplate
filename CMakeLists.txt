cmake_minimum_required(VERSION 3.5.1)
#avoid cmake adds -Wl,-search_paths_first that makes mac compiled binary segmentation fault
set(HAVE_FLAG_SEARCH_PATHS_FIRST 0)

project(run)

set(CMAKE_CXX_STANDARD 17)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)

#SET(CONAN_LIBS_BOOST boost_program_options boost_system)
conan_basic_setup()

#SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS}")

add_executable(run main.cpp)
target_link_libraries(run ${CONAN_LIBS})

IF ("${CMAKE_SYSTEM_NAME}" MATCHES "Windows")
   target_link_libraries(run ws2_32 wsock32)
ENDIF ()
