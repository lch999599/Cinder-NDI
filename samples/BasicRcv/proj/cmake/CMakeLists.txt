cmake_minimum_required( VERSION 3.0 FATAL_ERROR )
set( CMAKE_VERBOSE_MAKEFILE ON )

project( BasicReceiver )

get_filename_component( CINDER_PATH "${CMAKE_CURRENT_SOURCE_DIR}/../../../../../.." ABSOLUTE )
get_filename_component( SAMPLE_DIR "${CMAKE_CURRENT_SOURCE_DIR}/../.." ABSOLUTE )

include( "${CINDER_PATH}/proj/cmake/modules/cinderMakeApp.cmake" )

set( CINDER_VERBOSE ON )

ci_make_app( 
	SOURCES ${SAMPLE_DIR}/src/BasicReceiverApp.cpp
	CINDER_PATH ${CINDER_PATH}
	BLOCKS Cinder-NDI
)
