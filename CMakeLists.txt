set(BOOSTFILESYSTEM_LIBRARIES boostfilesystem)

include_directories(
    ${BOOST_INCLUDE_DIRS})

add_library(${BOOSTFILESYSTEM_LIBRARIES} STATIC
    src/codecvt_error_category.cpp
    src/operations.cpp
    src/path.cpp
    src/path_traits.cpp
    src/portability.cpp
    src/unique_path.cpp
    src/utf8_codecvt_facet.cpp
    src/windows_file_codecvt.cpp
    src/windows_file_codecvt.hpp)

target_link_libraries(${BOOSTFILESYSTEM_LIBRARIES}
    ${BOOSTSYSTEM_LIBRARIES})

set(BOOSTFILESYSTEM_FOUND TRUE PARENT_SCOPE)
set(BOOSTFILESYSTEM_INCLUDE_DIRS ${BOOST_INCLUDE_DIRS} PARENT_SCOPE)
set(BOOSTFILESYSTEM_LIBRARIES ${BOOSTFILESYSTEM_LIBRARIES} PARENT_SCOPE)
