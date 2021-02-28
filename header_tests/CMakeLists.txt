message(STATUS "generating code for header test for libcppy")
get_property(subdirs_list
    DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/.."
    PROPERTY  SUBDIRECTORIES)

header_test(${subdirs_list})
