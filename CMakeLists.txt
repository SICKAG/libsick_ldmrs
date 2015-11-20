# Use this as following:
#
#   mkdir build
#   cd build
#   cmake ..
#
# Potentially helpful options to cmake:
#   cmake -DCMAKE_VERBOSE_MAKEFILE=ON -DCMAKE_BUILD_TYPE=Debug ..
#   cmake -DCMAKE_INSTALL_PREFIX=/opt/ibeo -DCMAKE_BUILD_TYPE=Release ..
#
#

project (LDMRS_Example.pc)
CMAKE_MINIMUM_REQUIRED(VERSION 2.4)

# Set compiler flags to be very pedantic
IF (UNIX)
	SET( CMAKE_CXX_FLAGS "-Wall -Werror ${CMAKE_CXX_FLAGS}" )
ENDIF (UNIX)


# Extra cmake macros
INCLUDE (CheckSymbolExists)

###

add_subdirectory (src)


