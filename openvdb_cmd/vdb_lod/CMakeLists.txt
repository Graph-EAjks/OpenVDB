# Copyright Contributors to the OpenVDB Project
# SPDX-License-Identifier: Apache-2.0
#
#[=======================================================================[

  CMake Configuration for VDB LOD

#]=======================================================================]

cmake_minimum_required(VERSION 3.20)
project(VDBLOD LANGUAGES CXX)

include(GNUInstallDirs)

set(SOURCE_FILES main.cc)
add_executable(vdb_lod ${SOURCE_FILES})
target_link_libraries(vdb_lod ${OPENVDB_BINARIES_DEPENDENT_LIBS})

install(TARGETS vdb_lod RUNTIME DESTINATION ${OPENVDB_INSTALL_BINDIR})
