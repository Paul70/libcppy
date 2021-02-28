cmake_minimum_required(VERSION 3.1)

# setup project "libcppy"
if(NOT PROJECT_NAME)
    project(libcpy
        VERSION 0.0
        DESCRIPTION "C++ library collection for developing desktop apps with an optional Python interface"
        LANGUAGES C CXX)
endif()

set(CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/CMakeModules)
include(ProjectSettings)
include(HeaderTesting)

option(LIBCPPY_BUILD_HEADER_TEST "Test all libcppy C++ headers using a stand-alone main" ON)
option(LIBCPPY_BUILD_TESTS       "Build libcppy Google Test test suite" ON)

if(LIBCPPY_BUILD_TESTS)
    add_subdirectory(thirdparty/googletest)
endif()
if(LIBCPPY_BUILD_HEADER_TESTS)
    add_subdirectory(header_tests)
endif()
