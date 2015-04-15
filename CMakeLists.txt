set(BOOSTFILESYSTEM_INCLUDE_DIRS ${CMAKE_CURRENT_SOURCE_DIR}/include)
set(BOOSTFILESYSTEM_LIBRARIES boostfilesystem)

add_library(${BOOSTFILESYSTEM_LIBRARIES}
    src/codecvt_error_category.cpp
    src/operations.cpp
    src/path.cpp
    src/path_traits.cpp
    src/portability.cpp
    src/unique_path.cpp
    src/utf8_codecvt_facet.cpp
    src/windows_file_codecvt.cpp
    src/windows_file_codecvt.hpp)

target_include_directories(${BOOSTFILESYSTEM_LIBRARIES} PRIVATE
    ${BOOSTFILESYSTEM_INCLUDE_DIRS})

target_link_libraries(${BOOSTFILESYSTEM_LIBRARIES}
    ${BOOSTSYSTEM_LIBRARIES})

set(BOOSTFILESYSTEM_FOUND TRUE PARENT_SCOPE)
set(BOOSTFILESYSTEM_INCLUDE_DIRS ${BOOSTFILESYSTEM_INCLUDE_DIRS} PARENT_SCOPE)
set(BOOSTFILESYSTEM_LIBRARIES ${BOOSTFILESYSTEM_LIBRARIES} PARENT_SCOPE)
