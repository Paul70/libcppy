cmake_minimum_required(VERSION 3.1)

# setup project "libcppy"
if(NOT PROJECT_NAME)
    project(libcpy
        VERSION 0.0
        DESCRIPTION "C++ library collection for developing desktop apps with an optional Python interface"
        LANGUAGES C CXX)
endif()

