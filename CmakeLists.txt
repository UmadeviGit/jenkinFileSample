cmake_minimum_required(VERSION "3.23.0-rc1")

project("HelloWorld")
add_executable("${PROJECT_NAME}" "HelloWorld.cpp")

install(TARGETS "${PROJECT_NAME}" DESTINATION bin)   	#$(CMAKE_INSTALL_PREFIX)/binset(CPACK_PACKAGE_NAME "Autodesk")
set(CMAKE_WIN32_EXECUTABLE "true")
set(CPACK_PACKAGE_VENDOR "WaveAxis")
set(CPACK_PACKAGE_NAME "Autodesk")
set(CPACK_PACKAGE_VERSION_PATCH "0.1")
set(CPACK_PACKAGE_VENDOR "WaveAxis")

set(CPACK_WIX_UPGRADE_GUID "F9AAAAE2-D6AF-4EA4-BF46-B3E265400CC7")
set(CPACK_GENERATOR WIX)
include(CPack)
